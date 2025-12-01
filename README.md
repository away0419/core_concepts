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

- [x] [트랜잭션 ACID 특성 및 사례](C_데이터베이스_설계_운영/트랜잭션_ACID.md)
- [x] [Lock 유형과 Deadlock 감지·해결 전략](C_데이터베이스_설계_운영/락_데드락.md)
- [x] [정규화 vs 비정규화 적용 기준](C_데이터베이스_설계_운영/정규화_비정규화.md)
- [x] [인덱스 동작 원리(B-Tree, Hash 등)](C_데이터베이스_설계_운영/인덱스_동작원리.md)
- [x] [Sharding / Replication 개념과 운영 이슈](C_데이터베이스_설계_운영/샤딩_리플리케이션.md)
- [x] [트랜잭션 격리 수준(Isolation Level) 비교](C_데이터베이스_설계_운영/격리수준.md)
- [x] [관계형 vs NoSQL 선택 기준, 마이그레이션/백업·복구·일관성 전략](C_데이터베이스_설계_운영/RDB_vs_NoSQL.md)

## 📌 D. 시스템 설계 & 분산 시스템 개념

- [x] [단일 장애점(SPOF) 제거 전략](D_시스템_설계_분산/SPOF_제거.md)
- [x] [마이크로서비스 기본 개념과 단점/트레이드오프](D_시스템_설계_분산/마이크로서비스_기본.md)
- [x] [회복탄력성 패턴(Circuit Breaker / Retry / Timeout / Bulkhead)](D_시스템_설계_분산/회복탄력성_패턴.md)
- [x] [Consistent Hashing 개념과 사용처](D_시스템_설계_분산/Consistent_Hashing.md)
- [x] [분산 락(Distributed Lock) 구현 방식 비교](D_시스템_설계_분산/분산락.md)
- [x] [CAP 정리와 시스템 설계 적용 예시](D_시스템_설계_분산/CAP_정리.md)
- [x] [Eventual Consistency 모델 이해](D_시스템_설계_분산/Eventual_Consistency.md)
- [x] [분산 트랜잭션, 리더 선출, 분산 ID, 이벤트 소싱, 메시지 큐/분산 캐시/서비스 디스커버리/레이트 리미팅 점검](D_시스템_설계_분산/분산시스템_핵심메커니즘.md)

## 📌 E. 코드·도메인 설계 개념

- [x] [SOLID 5원칙 정리 및 코드 예시 첨부](E_코드_도메인_설계/SOLID.md)
- [x] [객체지향 설계 원칙(추상화, 캡슐화 등) 체계화](E_코드_도메인_설계/객체지향_설계원칙.md)
- [x] [주요 디자인 패턴(Factory, Strategy, Template, Builder, Proxy, Observer)](E_코드_도메인_설계/디자인패턴_핵심.md)
- [x] [DDD 핵심 개념(유비쿼터스 언어, 계층) 이해](E_코드_도메인_설계/DDD_핵심.md)
- [x] [Aggregate 경계 정의 연습](E_코드_도메인_설계/애그리게이트.md)
- [x] [Entity / Value Object 차이 정리](E_코드_도메인_설계/엔티티_ValueObject.md)
- [x] [Domain Event 설계 및 처리 흐름](E_코드_도메인_설계/도메인_이벤트.md)
- [x] [Bounded Context 식별 기준](E_코드_도메인_설계/바운디드컨텍스트.md)
- [x] [Repository, Adapter, Facade 등 추가 패턴 적용 근거 문서화](E_코드_도메인_설계/추가패턴_Repository_Adapter_Facade.md)

## 📌 F. 모니터링 / Observability 개념

- [x] [로그 / 메트릭 / 트레이싱(분산 추적) 역할 구분](F_모니터링_관찰성/로그_메트릭_트레이싱.md)
- [x] [APM 도구(NewRelic, Datadog, Pinpoint) 사용 목적](F_모니터링_관찰성/APM_도구.md)
- [x] [Prometheus · Grafana가 담당하는 영역 이해](F_모니터링_관찰성/Prometheus_Grafana.md)
- [x] [Alerting 구조 설계(임계값, 에스컬레이션 플로우)](F_모니터링_관찰성/Alerting_구조.md)
- [x] [로깅 전략(구조화/레벨), 대시보드 설계, SLI/SLO/SLA 정의](F_모니터링_관찰성/로깅_대시보드_SLI.md)

## 📌 G. API 설계

- [x] [REST 원칙 및 상태 코드 활용, 버저닝 전략](G_API_설계/REST_기본.md)
- [x] [페이징·필터링·에러 응답 규약](G_API_설계/페이징_필터링_에러.md)
- [x] [OpenAPI/Swagger 기반 문서화 및 계약 테스트](G_API_설계/OpenAPI_문서화.md)
- [x] [GraphQL·gRPC 도입 기준과 장단점](G_API_설계/GraphQL_gRPC.md)
- [x] [OAuth2, JWT 등 인증/인가 방식 비교](G_API_설계/인증_인가.md)
- [x] [HTTPS, CORS, CSRF 등 API 보안 항목](G_API_설계/API_보안.md)

## 📌 H. 보안 핵심 개념

- [x] [인증(Authentication) vs 인가(Authorization) 분리](H_보안/인증_vs_인가.md)
- [x] [데이터 암호화·해싱·시크릿 관리 전략](H_보안/암호화_시크릿관리.md)
- [x] [SQL Injection, XSS, CSRF 방어 체크리스트](H_보안/웹취약점_SQLi_XSS_CSRF.md)
- [x] [입력 검증·Sanitization 가이드](H_보안/입력검증_Sanitization.md)
- [x] [보안 로그 및 감사 트레일 설계](H_보안/보안로그_감사.md)

## 📌 I. DevOps · 인프라 · 실무 적용

- [x] [컨테이너(Docker) 기본, Kubernetes 오케스트레이션 이해](I_DevOps_인프라/컨테이너_Kubernetes.md)
- [x] [CI/CD 파이프라인 및 IaC(Infrastructure as Code) 패턴](I_DevOps_인프라/CI_CD_IaC.md)
- [x] [클라우드 서비스(AWS/GCP/Azure) 핵심 제품 비교](I_DevOps_인프라/클라우드_핵심서비스.md)
- [x] [배포 전략(Blue-Green, Canary, Rolling) 적용 기준](I_DevOps_인프라/배포전략.md)
- [x] [시스템 장애 대응·재발 방지, 성능 병목 분석 경험 정리](I_DevOps_인프라/장애대응_성능분석.md)
- [x] [대용량 트래픽 처리, 코드 리뷰·기술 문서·레거시 개선 사례 기록](I_DevOps_인프라/실무_경험정리.md)
