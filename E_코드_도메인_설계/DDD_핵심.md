# DDD 핵심 개념

Domain-Driven Design은 비즈니스 도메인을 중심으로 소프트웨어를 설계하는 방법론이다. 핵심 개념을 한 번에 정리한다.

---

## 1. 유비쿼터스 언어
- 개발자, 기획자, 도메인 전문가가 공유하는 동일한 용어.
- 모델(코드)과 문서, 회의에서 같은 단어를 사용해 혼선을 줄인다.

## 2. 레이어드 아키텍처
- **Presentation → Application → Domain → Infrastructure** 계층.
- 도메인 계층은 비즈니스 규칙만, 인프라는 외부 시스템 연동만 담당.

## 3. Bounded Context
- 도메인 전체를 작은 컨텍스트로 나눠 각자 역할/용어를 유지.
- 컨텍스트 간 통합 관계(Context Map)를 명시한다.

## 4. Building Blocks
- Entity, Value Object, Aggregate, Domain Service, Repository, Factory, Domain Event.

---

## 5. 체크리스트
- [ ] 핵심 도메인(Core Domain)과 일반화/지원 서브도메인을 구분했는가?
- [ ] 유비쿼터스 언어를 문서화하고 코드에 반영했는가?
- [ ] Bounded Context마다 모델/데이터 저장소를 분리했는가?
- [ ] 컨텍스트 간 통합 방식을 Context Map으로 표현했는가?

---

## 6. 실습 아이디어
- **실습 1**: 도메인 전문가와 협업해 용어 사전을 작성하고 코드에 반영.
- **실습 2**: 모놀리식 코드에서 Bounded Context 후보를 찾아 분리.
- **실습 3**: Context Map을 그려 컨텍스트 간 관계(Shared Kernel, Anti-corruption Layer 등)를 정의.

