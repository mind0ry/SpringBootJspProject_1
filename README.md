25-12-07 일요일<br>
우분투 설치 후 우분투에서 스프링 실행<br>


<img width="600" height="400" alt="스크린샷 2025-12-07 오후 7 22 15" src="https://github.com/user-attachments/assets/945ffd22-8709-4b22-8e5e-7219ca36cc93" />
<br><br>



mkdir source-folder       # 작업용 폴더 생성
cd source-folder          # 폴더 이동

sudo apt-get update       # 우분투 패키지 목록 업데이트
sudo apt-get install git  # Git 설치

java -version             # 자바 설치 확인 (없으면 openjdk 설치)
sudo apt-get install openjdk-17-jdk

git config --global user.name "깃닉네임"       # Git 사용자 이름 설정
git config --global user.email "깃이메일"       # Git 이메일 설정
git config --global user.password "깃토큰"      # Git 토큰(필요 시)

git clone "깃URL"         # GitHub 프로젝트 다운로드
cd 프로젝트폴더명          # 프로젝트 디렉토리 이동

chmod +x ./gradlew        # gradlew 실행 권한 부여
./gradlew build           # build/libs/에 WAR 파일 생성

cd build/libs             # WAR 파일 위치로 이동
sudo java -jar 파일이름.war   # 스프링 부트 실행
