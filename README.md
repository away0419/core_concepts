# 서비스 개발 학습 리스트

## 📌 A. 시스템 기본 구조 개념

- [x] [클라이언트–서버 구조 이해 및 요청 흐름 정리](A_시스템_기본_구조/클라이언트_서버_구조.md)
- [x] [Sync vs Async 처리 모델 비교](A_시스템_기본_구조/Sync_Async_처리모델.md)
- [x] [Blocking / Non-blocking I/O 차이와 적용 사례](A_시스템_기본_구조/Blocking_Nonblocking_IO.md)
- [x] [웹 요청 생명주기(브라우저 → 서버 → 응답) 정리](A_시스템_기본_구조/웹_요청_생명주기.md)
- [x] [TCP / HTTP 기본 구조 및 헤더 핵심 정리](A_시스템_기본_구조/TCP_HTTP_기본.md)
- [x] [로드 밸런싱 개념과 L4/L7 비교](A_시스템_기본_구조/로드_밸런싱_L4_L7.md)
- [x] [확장성·가용성·일관성·내구성·성능·보안 원칙 점검](A_시스템_기본_구조/시스템_품질_원칙.md)
- [x] [모놀리식·MSA·이벤트 기반·CQRS·Gateway·Service Mesh 비교](A_시스템_기본_구조/아키텍처_패턴_비교.md)

## 📌 B. 대규모 트래픽 / 성능 핵심 개념

- [x] [병목(Bottleneck) 분석 원리 및 대표 도구 파악](B_대규모_트래픽_성능/병목_분석.md)
- [x] [Scale-up / Scale-out 차이와 의사결정 기준](B_대규모_트래픽_성능/스케일전략.md)
- [x] [캐싱 전략(Cache-aside / Write-through / Write-back) 장단점](B_대규모_트래픽_성능/캐싱_전략.md)
- [x] [CDN 개념과 캐시 무효화 전략](B_대규모_트래픽_성능/CDN_전략.md)
- [x] [CQRS 구조와 읽기/쓰기 분리 사례](B_대규모_트래픽_성능/CQRS_개념.md)
- [x] [이벤트 기반 아키텍처(Event-driven Architecture) 적용 포인트](B_대규모_트래픽_성능/이벤트_기반_아키텍처.md)
- [x] [Backpressure & Queueing Theory 기초 개념](B_대규모_트래픽_성능/Backpressure_Queueing.md)
- [x] [데이터베이스 쿼리 최적화, 비동기/배치 처리, 커넥션 풀, 메모리·GC 튜닝 점검](B_대규모_트래픽_성능/전반적_퍼포먼스_튜닝.md)

## 📌 C. 데이터베이스 설계·운영 개념

- [ ] 트랜잭션 ACID 특성 및 사례
- [ ] Lock 유형과 Deadlock 감지·해결 전략
- [ ] 정규화 vs 비정규화 적용 기준
- [ ] 인덱스 동작 원리(B-Tree, Hash 등)
- [ ] Sharding / Replication 개념과 운영 이슈
- [ ] 트랜잭션 격리 수준(Isolation Level) 비교
- [ ] 관계형 vs NoSQL 선택 기준, 마이그레이션/백업·복구·일관성 전략

## 📌 D. 시스템 설계 & 분산 시스템 개념

- [ ] 단일 장애점(SPOF) 제거 전략
- [ ] 마이크로서비스 기본 개념과 단점/트레이드오프
- [ ] 회복탄력성 패턴(Circuit Breaker / Retry / Timeout / Bulkhead)
- [ ] Consistent Hashing 개념과 사용처
- [ ] 분산 락(Distributed Lock) 구현 방식 비교
- [ ] CAP 정리와 시스템 설계 적용 예시
- [ ] Eventual Consistency 모델 이해
- [ ] 분산 트랜잭션, 리더 선출, 분산 ID, 이벤트 소싱, 메시지 큐/분산 캐시/서비스 디스커버리/레이트 리미팅 점검

## 📌 E. 코드·도메인 설계 개념

- [ ] SOLID 5원칙 정리 및 코드 예시 첨부
- [ ] 객체지향 설계 원칙(추상화, 캡슐화 등) 체계화
- [ ] 주요 디자인 패턴(Factory, Strategy, Template, Builder, Proxy, Observer)
- [ ] DDD 핵심 개념(유비쿼터스 언어, 계층) 이해
- [ ] Aggregate 경계 정의 연습
- [ ] Entity / Value Object 차이 정리
- [ ] Domain Event 설계 및 처리 흐름
- [ ] Bounded Context 식별 기준
- [ ] Repository, Adapter, Facade 등 추가 패턴 적용 근거 문서화

## 📌 F. 모니터링 / Observability 개념

- [ ] 로그 / 메트릭 / 트레이싱(분산 추적) 역할 구분
- [ ] APM 도구(NewRelic, Datadog, Pinpoint) 사용 목적
- [ ] Prometheus · Grafana가 담당하는 영역 이해
- [ ] Alerting 구조 설계(임계값, 에스컬레이션 플로우)
- [ ] 로깅 전략(구조화/레벨), 대시보드 설계, SLI/SLO/SLA 정의

## 📌 G. API 설계

- [ ] REST 원칙 및 상태 코드 활용, 버저닝 전략
- [ ] 페이징·필터링·에러 응답 규약
- [ ] OpenAPI/Swagger 기반 문서화 및 계약 테스트
- [ ] GraphQL·gRPC 도입 기준과 장단점
- [ ] OAuth2, JWT 등 인증/인가 방식 비교
- [ ] HTTPS, CORS, CSRF 등 API 보안 항목

## 📌 H. 보안 핵심 개념

- [ ] 인증(Authentication) vs 인가(Authorization) 분리
- [ ] 데이터 암호화·해싱·시크릿 관리 전략
- [ ] SQL Injection, XSS, CSRF 방어 체크리스트
- [ ] 입력 검증·Sanitization 가이드
- [ ] 보안 로그 및 감사 트레일 설계

## 📌 I. DevOps · 인프라 · 실무 적용

- [ ] 컨테이너(Docker) 기본, Kubernetes 오케스트레이션 이해
- [ ] CI/CD 파이프라인 및 IaC(Infrastructure as Code) 패턴
- [ ] 클라우드 서비스(AWS/GCP/Azure) 핵심 제품 비교
- [ ] 배포 전략(Blue-Green, Canary, Rolling) 적용 기준
- [ ] 시스템 장애 대응·재발 방지, 성능 병목 분석 경험 정리
- [ ] 대용량 트래픽 처리, 코드 리뷰·기술 문서·레거시 개선 사례 기록
