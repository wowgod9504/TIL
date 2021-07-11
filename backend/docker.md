## Docker ?

IT 소프트웨어인 "Docker”는 Linux 컨테이너를 만들고 사용할 수 있도록 하는 컨테이너화 기술입니다.

Docker는 코드를 실행하는 표준 방식을 제공합니다. Docker는 컨테이너를 위한 운영 체제입니다.  
가상 머신이 서버 하드웨어를 가상화하는 방식과 비슷하게(직접 관리해야 하는 필요성 제거) 컨테이너는 서버 운영 체제를 가상화합니다.  
Docker는 각 서버에 설치되며 컨테이너를 구축, 시작 또는 중단하는 데 사용할 수 있는 간단한 명령을 제공합니다.
## < Docker 컨테이너의 이점 > 
### 모듈성
- Docker의 컨테이너화 접근 방식은 전체 애플리케이션을 분해할 필요 없이 애플리케이션의 일부를 분해하고,  
업데이트 또는 복구하는 능력에 집중되어 있습니다. 사용자는 이 마이크로서비스 기반 접근 방식 외에도 SOA  (service-oriented architecture)의
작동 방식과 동일하게 멀티플 애플리케이션 사이에서 프로세스를 공유할 수 있습니다.
### 계층 및 이미지 버전 제어
- 각 Docker 이미지 파일은 일련의 계층으로 이루어져 있으며 이 계층들은 단일 이미지로 결합됩니다. 이미지가 변경될 때 계층이 생성되고, 사용자가 실행 또는 복사와 같은 명령을 지정할 때마다 새 계층이 생성됩니다.

Docker는 새로운 컨테이너를 구축할 때 이러한 계층을 재사용하므로 구축 프로세스가 훨씬 더 빨라집니다. 중간 변경 사항이 이미지 사이에서 공유되므로 속도, 규모, 효율성이 더 개선됩니다. 계층화에는 버전 관리가 내재되어 있으며 새로운 변경 사항이 발생할 때마다 내장 변경 로그가 기본적으로 적용되므로 컨테이너 이미지를 완전히 제어할 수 있습니다.

### 롤백
계층화에서 가장 유용한 부분은 아마도 롤백 기능일 것입니다. 모든 이미지에는 계층이 있으며, 현재의 이미지 반복이 적절하지 않은 경우 이전 버전으로 롤백하면 됩니다. 이 기능은 애자일(agile) 개발 접근 방식을 지원하며 툴 관점에서 실제로 지속적인 통합 및 연속 배포(Continuous Integration and Deployment, CI/CD)를 수행하는 데 도움을 줍니다.

### 신속한 배포
새로운 하드웨어를 준비하고, 실행하고, 프로비저닝하고, 사용할 수 있게 하려면 일반적으로 며칠이 소요되었습니다. 많은 노력과 부가적인 업무가 필요하므로 부담도 상당했습니다. Docker 기반 컨테이너는 배포 시간을 몇 초로 단축할 수 있습니다. 각 프로세스에 대한 컨테이너를 생성함으로써 사용자는 유사한 프로세스를 새 앱과 빠르게 공유할 수 있습니다. 또한, 컨테이너를 추가하거나 이동하기 위해 OS를 부팅할 필요가 없으므로 배포 시간이 크게 단축됩니다. 이뿐만 아니라 배포 속도가 빨라 컨테이너에서 생성된 데이터를 비용 효율적으로 쉽게 생성하고 삭제할 수 있고 사용자는 우려를 할 필요가 없습니다.

즉, Docker 기술은 효율성을 중시하며 더 세분화되고 제어 가능한 마이크로서비스 기반 접근 방식입니다.