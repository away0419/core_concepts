# 컨테이너 · Kubernetes 기초

컨테이너는 애플리케이션과 실행 환경을 패키징하고, Kubernetes(K8s)는 이를 대규모로 관리하는 플랫폼이다.

---

## 1. 컨테이너 기본
- Dockerfile로 이미지 정의 → Registry에 저장 → 컨테이너 실행.
- 불변 이미지, 계층 구조, 빠른 배포.
- 보안: 최소 권한, Base 이미지 관리, 이미지 스캔.

## 2. Kubernetes 핵심 개념
- **Pod**: 컨테이너의 최소 배포 단위.
- **Deployment**: Pod Replica 관리, 롤링 업데이트.
- **Service**: Stable endpoint, 로드밸런싱.
- **ConfigMap/Secret**: 설정/시크릿 주입.
- **Ingress**: 외부 트래픽 라우팅.

## 3. 운영 체크포인트
- 리소스 요청/제한 설정으로 노드 안정성 유지.
- Liveness/Readiness Probe로 헬스 체크.
- 네임스페이스, RBAC, 네트워크 정책으로 보안 강화.

---

## 4. 체크리스트
- [ ] 이미지 빌드/취약점 스캔 자동화?
- [ ] Pod 리소스/오토스케일링(HPA, VPA)을 설정했는가?
- [ ] Observability(Logs, Metrics, Traces)를 K8s와 통합했는가?
- [ ] 백업/복구(ETCD, PV) 계획이 있는가?

---

## 5. 실습 아이디어
- **실습 1**: Dockerfile을 작성해 CI에서 이미지 빌드/푸시.
- **실습 2**: Minikube/Kind에서 Deployment, Service, Ingress를 구성.
- **실습 3**: Pod 장애를 주입하고 K8s가 자동으로 복구하는지 확인.

