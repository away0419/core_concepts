# Entity vs Value Object

DDD에서 Entity와 Value Object를 구분하면 모델이 훨씬 명확해진다.

---

## 1. Entity
- 고유 식별자(ID)로 구분.
- 라이프사이클 동안 상태가 바뀔 수 있다.
- 예: 주문(Order), 사용자(User).

## 2. Value Object
- 식별자가 없고 값 자체로 동등성 판단.
- 불변(immutable)이 이상적.
- 예: 주소(Address), 기간(Period), 금액(Money).

---

## 3. 설계 가이드
- 값의 의미나 단위를 분명히 하려면 Value Object로 감싼다.
- Entity 내부에서 Value Object를 조합해 불변 조건을 유지.
- 값 비교/계산 로직을 Value Object에 넣어 응집도를 올린다.

---

## 4. 체크리스트
- [ ] 식별자가 필요한 도메인 개념인가? (필요 없다면 VO)
- [ ] Value Object를 불변으로 만들고 있는가?
- [ ] 동일성을 비교할 때 ID(엔티티) vs 값(VO)을 명확히 구분했는가?
- [ ] 데이터베이스 매핑(JPA, ORM 등)에서 VO를 Embeddable 등으로 표현했는가?

---

## 5. 실습 아이디어
- **실습 1**: 금액/주소 같은 Primitive Obsession을 Value Object로 리팩터링.
- **실습 2**: Entity-VO 간 변환 로직을 테스트로 검증.
- **실습 3**: Value Object를 불변으로 유지하면서 계산 메서드를 추가.

