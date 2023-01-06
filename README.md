* hello MES on k8s
* NCP 의 컨테이너 서비스를 기반으로 작성되었으므로 온프라미스로 구축된 k8s에서는 네트워크 및 이미지 저장소에 대한 수정이 필요할 수 있음

### 서비스 명세
- config-svc 
  - 서버 설정 관리 서비스
  - image : impix.kr.ncr.ntruss.com/config-svc:latest

- eureka-svc
  - Endpoint 관리 서비스
  - image : impix.kr.ncr.ntruss.com/eureka-svc:latest

- gateway-svc
  - API 라우팅 서비스
  - image : impix.kr.ncr.ntruss.com/gateway-svc:latest

- base-svc
  - mes 포털 서비스
  - image : impix.kr.ncr.ntruss.com/base-svc:latest

- util-svc
  - 공통 기능 관리 서비스
  - image : impix.kr.ncr.ntruss.com/uilt-svc:latest
