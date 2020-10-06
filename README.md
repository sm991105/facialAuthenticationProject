세팅 방법: 
1. 2차 인증을 진행할 컴퓨터에 가상환경을 세팅해야 한다. (windows 10 기준)

2. 원하는 곳에 프로젝트를 진행할 폴더를 생성한다. 해당 폴더의 주소를 복사해둔다. 

3. windows powershell을 open하고
   1) cd (프로젝트 폴더 주소)
   2) pip install virtualenv
   3) python -m pip install --upgrade pip
   4) virtualenv venv
   5) cd venv/bin
   6) .\activate => 가상환경 venv가 실행된다.

4. github에 있는 소스를 그대로 다운받아 해당 프로젝트 폴더에 압축을 풀어주고, face_recognition 모듈을 설치해줍니다.
   1) cd (프로젝트 폴더 주소)
   2) git clone 
   2) pip install cmake
   3) git clone https://github.com/ageitgey/face_recognition.git
   4) cd face_recognition
   5) python setup.py install
   => dlib, numpy, face_recognition 까지 설치가 끝납니다.

6. 마지막으로 필요한 모듈들을 모두 설치해 줍니다. 
 1) cd ..
 2) pip install --upgrade pip
 3) pip install -r requirements.txt

7. 메인 코드를 실행해줌으로써 서버 구동은 끝납니다. 
  python main,py => 서버 컴퓨터에서 컴퓨터가 실행됩니다.

8. 마지막으로 외부에서도 접속할 수 있도록 도메인을 만들어주기 위해 ngrok이라는 
프로그램을 다운받습니다.
  1) ngrok 다운로드 (https://ngrok.com/download)
  2) 명령 프롬프트 cmd로(powershell 아님) 들어갑니다.
  3) cd (ngrok파일 저장된 주소)
  4) ngrok http 9000
   9000번 포트를 열어준 다음에 서버 주소(https://(ngrok주소))을 이용해 접속하면 완성.