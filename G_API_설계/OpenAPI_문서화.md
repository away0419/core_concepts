# OpenAPI/Swagger 문서화 & 계약 테스트

API 문서를 코드와 동기화하면 협업/테스트 품질이 올라간다.

---

## 1. OpenAPI 스펙
- YAML/JSON으로 엔드포인트, 요청/응답, 인증 방식을 정의.
- Swagger UI, ReDoc 등으로 자동 문서화.
- 코드 자동 생성(Client/Server Stub) 가능.

## 2. 문서 관리 전략
- Git에 스펙 파일을 저장하고 PR로 리뷰.
- CI에서 스키마 유효성 검사(openapi-cli, spectral).
- 버전 태그(`info.version`)로 호환성 추적.

## 3. 계약 테스트
- 스펙을 신뢰할 수 있는 단일 소스로 사용.
- Consumer-Driven Contract(Pact) 테스트로 호환성 검증.
- Postman/Newman, Dredd 등 도구로 스펙 기반 테스트 자동화.

---

## 4. 체크리스트
- [ ] 모든 API 변화가 OpenAPI 스펙에 반영되는가?
- [ ] 문서/코드/테스트가 같은 저장소/파이프라인에서 관리되는가?
- [ ] 계약 테스트 실패 시 배포를 막는가?
- [ ] 사용자/파트너가 접근할 수 있는 문서 포털을 운영하는가?

---

## 5. 실습 아이디어
- **실습 1**: 기존 API를 OpenAPI 3.0 스펙으로 문서화하고 Swagger UI로 제공.
- **실습 2**: Pact를 사용해 소비자 계약 테스트를 작성.
- **실습 3**: CI에서 스펙 검증 + Dredd를 실행해 문서와 구현 차이를 자동 검출.

