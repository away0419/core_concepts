# CI/CD 파이프라인 · IaC 패턴

DevOps의 핵심은 자동화된 빌드/테스트/배포(CI/CD)와 인프라 코드(IaC) 관리다.

---

## 1. CI/CD 파이프라인
- **CI**: 코드 커밋 → 빌드 → 테스트 → 코드 품질 검사.
- **CD**: 아티팩트 배포(Blue-Green, Canary), 롤백 자동화.
- GitHub Actions, GitLab CI, Jenkins, Argo CD 등 도구 사용.

### 필수 단계
1. Lint/Test/Static Analysis
2. 빌드/이미지 생성
3. 보안 스캔(SCA, Container Scan)
4. 배포 및 Health Check

## 2. Infrastructure as Code
- Terraform, Pulumi, AWS CDK 등으로 인프라를 코드로 선언.
- GitOps: Git 저장소 상태를 실제 인프라와 동기화.
- 모듈화/변수화로 재사용성을 높인다.

---

## 3. 체크리스트
- [ ] CI 파이프라인이 PR/브랜치 전략과 연동되어 있는가?
- [ ] Fail-fast: 어느 단계에서 실패해도 즉시 중단되는가?
- [ ] IaC 코드 리뷰/테스트/State 관리가 체계적인가?
- [ ] 배포 작업이 Runbook 없이도 자동으로 수행되는가?

---

## 4. 실습 아이디어
- **실습 1**: GitHub Actions로 빌드/테스트/배포 파이프라인을 구현.
- **실습 2**: Terraform으로 VPC/DB/서비스를 선언하고 Plan/Apply 과정을 리뷰.
- **실습 3**: Argo CD나 Flux로 GitOps 워크플로우를 구축.

