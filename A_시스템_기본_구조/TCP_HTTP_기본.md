# TCP / HTTP 기본 구조

네트워크의 기초는 결국 TCP와 HTTP다. 아래 내용을 차례대로 학습하면 “클라이언트가 서버와 어떻게 대화하는지”를 명확히 이해할 수 있다.

---

## 1. TCP를 이해해야 하는 이유

- **3-way Handshake**: SYN → SYN/ACK → ACK으로 연결을 맺는다. RTT가 길수록 느린 이유가 여기 있다.
- **세션 종료(4-way FIN)**: FIN/ACK 왕복 두 번, TIME_WAIT 상태를 지나며 자원을 완전히 반환한다.
- **흐름/혼잡 제어**: 윈도우 크기와 혼잡 제어 알고리즘(Slow Start, Congestion Avoidance)이 전송 속도를 결정한다.
- **튜닝 요소**:
  - `SYN backlog`, `TIME_WAIT`, `KeepAlive`, `Nagle`, `TCP Fast Open`.
  - 모바일/국제 서비스에서 RTT가 크면 초기 혼잡 윈도우 조정, Fast Open이 효과적이다.

---

## 2. HTTP 버전 비교

| 항목      | HTTP/1.1                   | HTTP/2                             | HTTP/3(QUIC)                   |
| --------- | -------------------------- | ---------------------------------- | ------------------------------ |
| 전송 기반 | TCP                        | TCP                                | UDP(QUIC)                      |
| 특징      | Keep-Alive, 파이프라이닝   | 멀티플렉싱, 헤더 압축, Server Push | HOLB 제거, 0-RTT, 모바일 친화  |
| 사용 예   | 전통 REST API, 단순 서비스 | gRPC, GraphQL BFF, 고병렬 API      | 글로벌/모바일 서비스, 스트리밍 |
| 주의      | 연결 수 폭증, HOLB         | 프록시/방화벽 호환성               | 네트워크 장비·보안 정책 호환성 |

요청/응답은 항상 **Method/URL/Header/Body** 구조를 갖고, 상태 코드와 캐시 헤더로 의미를 전달한다.

---

## 3. 실제 적용 시나리오

- **gRPC/GraphQL**: HTTP/2 기반의 멀티플렉싱과 스트리밍이 필수.
- **대용량 다운로드/스트리밍**: HTTP/1.1 vs HTTP/2를 PoC로 비교해 성능을 측정.
- **모바일/글로벌 서비스**: HTTP/3(QUIC)로 지연을 줄이되, TLS 오프로딩/방화벽 호환성을 미리 검증.

---

## 4. 학습/실습 아이디어

- `curl -v --http1.1`, `curl -v --http2`로 같은 API를 호출하며 헤더·연결 차이를 비교한다.
- 브라우저 개발자 도구(Network 탭)에서 Protocol(H2/H3)과 RTT, TLS Handshake 시간을 확인한다.
- 서버 설정에서 `keepalive_timeout`, `max_connections`, `initial_window_size` 등을 조정하며 성능 변화를 측정한다.

---

## 5. 체크리스트

- [ ] 서비스가 사용하는 HTTP 버전과 서버/클라이언트 라이브러리 지원 현황을 파악했는가?
- [ ] TCP 튜닝 파라미터(SYN backlog, TIME_WAIT, KeepAlive Interval)를 운영 표준으로 문서화했는가?
- [ ] TLS/HTTPS 적용 시 Cipher Suite, 인증서 자동 갱신, HSTS 정책을 갖추었는가?
- [ ] 상태 코드/에러 응답 규약, Correlation-ID, Cache-Control, ETag 등 헤더를 표준화했는가?
- [ ] 네트워크 모니터링(연결 수, RTT, Retransmission, TLS Handshake 시간)을 시각화했는가?
- [ ] HTTP/2/3 도입 전, 네트워크·보안 장비 호환성과 Fallback 전략을 PoC로 검증했는가?
