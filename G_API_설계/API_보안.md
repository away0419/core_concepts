# API 보안 기초 (HTTPS, CORS, CSRF 등)

API를 외부에 공개하면 다양한 공격에 노출된다. 기본 보안 수단을 정리한다.

---

## 1. HTTPS/TLS
- 모든 요청을 HTTPS로 강제(HSTS).
- TLS 버전, 암호화 스위트, 인증서 갱신 자동화.
- 중간자 공격 방지를 위한 Certificate Pinning 고려.

## 2. CORS
- `Access-Control-Allow-Origin` 등 헤더를 통해 허용 도메인 제어.
- Credential 필요 여부에 따라 `Allow-Credentials` 설정.
- Preflight 요청 캐시(TTL)로 성능 최적화.

## 3. CSRF 방어
- SameSite=Lax/Strict 쿠키, CSRF 토큰, Double Submit Cookie.
- API에서 쿠키 대신 Bearer Token 사용 시 영향 줄어듬.

## 4. 입력 검증
- SQLi/XSS 등 기본 취약점 차단을 위한 Validation/Sanitization.
- API Gateway/WAF에서 1차 필터링.

## 5. 기타
- Rate Limiting, Bot Detection, IP Allow/Deny 리스트.
- 로깅/모니터링으로 의심스러운 접근 탐지.

---

## 6. 체크리스트
- [ ] HTTPS를 강제하고 TLS 설정을 주기적으로 갱신하는가?
- [ ] CORS 정책을 최소 권한으로 설정했는가?
- [ ] CSRF 방어 전략이 있으며, 테스트를 통해 검증했는가?
- [ ] 입력 검증, Rate Limit, Audit Log 등 추가 방어선을 갖추었는가?

---

## 7. 실습 아이디어
- **실습 1**: HSTS 및 TLS 설정을 적용한 후 Qualys SSL Labs 등으로 점검.
- **실습 2**: CORS 설정을 여러 환경(개발/운영)에 맞게 템플릿화.
- **실습 3**: CSRF 공격을 재현하고 보호 메커니즘이 작동하는지 확인.

