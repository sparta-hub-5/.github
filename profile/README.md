# bangbang-hub 프로젝트

## BangBangHub

전통적인 물류 운영에서 발생하는 복잡한 수작업 절차(업체 확인, 배송 배정, 이동 경로 관리, 권한 관리)를
클라우드 기반 MSA 아키텍처로 재설계하여 확장성과 안정성을 확보했습니다.

## 문제 정의
국내 물류 산업은 허브 기반 복잡한 구조를 가지며, 다음 문제들이 존재합니다:

### 주요 문제
- 허브 간 경로 및 이동 절차가 복잡하고 수작업 의존도가 높음
- 배송 배정·라우팅 비효율로 운영 비용 증가
- 업체/주문 정보가 분산되어 전체 흐름 파악이 어려움
- 권한 관리가 복잡하여 통합 접근 제어가 어려움
- 실시간 추적 및 오류 대응 체계 부족
- 단일 시스템 의존 시 확장성과 장애 대응력 저하

이를 해결하기 위해 MSA 기반 구조로 재설계가 필요합니다.

## 주요 기술 스택
| 영역                               | 기술                             |
| -------------------------------- | ------------------------------ |
| **Backend**                      | Spring Boot 3.x                |
| **Database**                     | PostgreSQL (서비스별 독립 스키마 구조)    |
| **Service Discovery**            | Spring Cloud Eureka            |
| **API Gateway**                  | Spring Cloud Gateway           |
| **Configuration Management**     | **Spring Cloud Config Server** |
| **Authentication/Authorization** | Keycloak + JWT, RBAC 기반        |
| **Asynchronous Messaging**       | **Apache Kafka**               |
| **Distributed Tracing**          | Zipkin                         |
| **AI/ML**                        | Spring AI + Gemini API         |
| **Documentation**                | Swagger / SpringDoc            |
| **Monitoring**                   | **Prometheus + Grafana**       |
| **Log Collection / Aggregation** | **Grafana Loki**               |
| **Containerization**             | Docker & Docker Compose        |
| **Caching**                  | Redis (허브 정보·경로 캐싱 용도)         |

### 1. Spring Cloud Eureka (Service Discovery)
- 서비스 위치 자동 등록/조회
- 확장성 있는 서비스 통신 지원

### 2. Spring Cloud Gateway
- 단일 진입점(API Gateway)
- 인증/로그/필터/Rate Limit 관리

### 3. Spring Cloud Config Server
- 공통 설정 중앙 관리
- 환경별 설정 분리 및 버전 관리

### 4. Keycloak + JWT
- RBAC 기반 인증/인가
- OAuth2/OpenID 표준 지원

### 5. Apache Kafka
- 비동기 이벤트 기반 서비스 통신
- 대량 트래픽 안정 처리

### 6. Prometheus
- 서비스 지표 모니터링
- Actuator 연동 기반 자동 수집

### 7. Grafana
- 실시간 지표 시각화
- 알람 기반 장애 대응

### 8. Loki
- 로그 중앙화 및 추적
- Grafana와 자연스러운 연동

### 9. Docker
- 환경 표준화 및 빠른 배포 구성

  ## 프로젝트 아키텍처
  <img width="1036" height="735" alt="image" src="" />
