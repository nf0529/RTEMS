# RTEMS 구축 환경
VMware 
Linux 22.04
## 설치 환경
git clone 형식
### 내용

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