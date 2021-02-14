version 확인
node -v
현재 버전 :: v12.16.3

npm -v
현재 버전 :: 6.14.4

vue -V
현재 버전 :: 4.5.6

npm install
npm install -g @vue/cli
npm install -g @vue/cli@3.x.x
npm install -g @vue/cli@3.0.0

Vue CLI 설치 :: 설치 되는 위치 C://Users/사용자/AppData/Roaming/npm/node_modules

CLI 3.X 버전 부터 프로젝트생성 방법
vue create vue-example
하면, vue-example 프로젝트가 생성된다.

프로젝트 생성이 되지 않는 경우1
다음과 같은 Error가 나오는 경우 방법


vue : 이 시스템에서 스크립트를 실행할 수 없으므로 C:\Users\사용자\AppData\Roaming\npm\vue.ps1 파일을 로드할 수 없습니다.


powershell을 bash로 놓고 다시 프로젝트 만들기
방법 1로 해결이 안될 때는 terminal에서 power shell로 실행하지 않고 bash로 놓고 명령문을 다시 쳐보자.


powershell을 bash로 변경방법은?
powershell 이라고 되어있는 부분에서 화살표를 눌러보면, Select Default Shell 이라고 나온다. :)
그걸 누르면 선택창이 하나 뜨고, 거기서 bash.exe 선택하면 끝!

프로젝트 실행
생성한 프로젝트 폴더로 이동한 후

cd 생성한 프로젝트
실행 명령문 작성

npm run serve
npm i axios
CLI 업데이트
npm i -g @vue/cli
