## Hello MES on k8s
* NCP 의 컨테이너 서비스를 기반으로 작성되었으므로 온프라미스로 구축된 k8s에서는 네트워크 및 이미지 저장소에 대한 수정이 필요할 수 있음

<img src="/git_images/msa_on_k8s.png"/>

## MSA 버전 (msa 폴더)
- msa를 위한 아키텍처들이 포함된 버전
- keycloak 은 별도의 외부 서비스로 구동 중

## POC 버전 (poc 폴더)
- 모놀리스 아키텍처로 구현된 기존 mes 프로젝트를 k8s에서 동작하도록 변경한 버전
- 중간 시연용이며, 같은 이미지를 여러개의 다른 이름의 서비스로 실행함 (msa인 것처럼 보이게) 

## 서비스 명세
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
