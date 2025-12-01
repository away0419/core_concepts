# SQL Injection · XSS · CSRF 방어 체크리스트

가장 흔한 웹 취약점 세 가지와 방어 방법을 정리한다.

---

## 1. SQL Injection
- 원인: 사용자 입력을 검증 없이 쿼리에 삽입.
- 방어: Prepared Statement/ORM, 입력 검증, 최소 권한 DB 계정.
- 테스트: SQLi 스캐너, SAST/DAST, WAF 룰.

## 2. XSS (Cross-Site Scripting)
- Stored/Reflected/DOM 기반.
- 방어: 출력 시 Context-aware 인코딩, CSP(Content Security Policy), 입력 필터링.
- React/Vue 등 프레임워크의 자동 escaping을 활용.

## 3. CSRF
- 피해자 브라우저가 의도치 않은 요청을 보냄.
- 방어: CSRF 토큰, SameSite 쿠키, Referer/Origin 검증.

---

## 4. 체크리스트
- [ ] 모든 입력값을 검증하고, SQL 바인딩을 사용하는가?
- [ ] 출력 시 HTML/JS/CSS 컨텍스트에 맞는 escaping을 적용했는가?
- [ ] CSRF 보호 장치(SameSite, CSRF 토큰)를 활성화했는가?
- [ ] 정기적으로 보안 스캐너/펜테스트를 수행하는가?

---

## 5. 실습 아이디어
- **실습 1**: 취약한 샘플 앱에서 SQLi/XSS/CSRF 공격을 재현하고 패치를 적용.
- **실습 2**: CSP 헤더를 적용해 XSS 공격이 차단되는지 확인.
- **실습 3**: 프론트엔드/백엔드가 함께 동작하는 CSRF 방어 프로세스를 구현.

