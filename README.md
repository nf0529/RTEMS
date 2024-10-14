# RTEMS 구축 환경
VMware 
Linux 22.04
## 설치 환경

### 내용
sudo apt update
sudo apt install -y git gcc g++ make automake autoconf libtool pkg-config bison>
cd rtems_waf
./waf configure
./waf

#### 오류 해결
1.
python 오류시 심볼릭 링크 생성
sudo ln -s /usr/bin/python3 /usr/bin/python

2.
rtems 빌드시 config.ini오류 -> 1. RTEMS 소스 클론 확인
git clone https://github.com/RTEMS/rtems.git

cd rtems
git submodule init
git submodule update
후 재 빌드

3. RTMES 빌드시
환경 변수 설정
설치 후, PATH 환경 변수에 RTEMS 바이너리 경로를 추가합니다. 예를 들어, 다음 명령을 터미널에 입력하여 RTEMS 바이너리가 포함된 디렉토리를 환경 변수에 추가합니다:

export PATH=$HOME/quick-start/rtems/6/bin:$PATH

How to Run :
rtems-run --rtems-bsps=erc32-sis build/sparc-rtems6-erc32/hello.exe

