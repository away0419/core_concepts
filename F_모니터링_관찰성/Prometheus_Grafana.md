# Prometheus · Grafana 역할

Prometheus는 시계열 메트릭 수집/저장, Grafana는 시각화/대시보드 도구로, 함께 사용하는 경우가 많다.

---

## 1. Prometheus
- Pull 기반 스크레이핑: 대상 서비스가 `/metrics`를 제공.
- PromQL로 강력한 쿼리/알림 작성 가능.
- Alertmanager와 연동해 Slack/PagerDuty 등으로 알림 전송.

## 2. Grafana
- 여러 데이터 소스(Prometheus, Loki, Elastic, CloudWatch 등)를 한 곳에서 시각화.
- 대시보드 템플릿, 변수, 경보(Alerting) 기능 제공.

---

## 3. 운영 팁
- 스크레이프 간격, 보존 기간을 트래픽/스토리지에 맞게 조정.
- Exporter(Node, DB, 큐 등)를 활용해 인프라 전반을 모니터링.
- 다중 Prometheus(HA) 또는 Remote Write로 백업/장기 저장.

---

## 4. 체크리스트
- [ ] 핵심 서비스마다 `/metrics` 엔드포인트를 제공하는가?
- [ ] PromQL 쿼리/대시보드를 코드/Repo로 관리(IaC)하는가?
- [ ] Alertmanager 라우팅/사일런스를 정의했는가?
- [ ] Grafana 대시보드에 SLO, 에러 버짓을 반영했는가?

---

## 5. 실습 아이디어
- **실습 1**: 애플리케이션에 Prometheus 클라이언트를 붙여 사용자 정의 메트릭을 노출.
- **실습 2**: Grafana 대시보드를 만들어 P95 지연, 에러율, 시스템 지표를 한 화면에 배치.
- **실습 3**: Alertmanager를 설정해 임계치 초과 시 Slack에 Alert 전송.

