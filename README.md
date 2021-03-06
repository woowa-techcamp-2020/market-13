# 전수현, 최해랑의 우아한테크캠프 3기 배민상회 회원가입/로그인 레포지토리입니다.


## 🎁 heroku 배포 프로젝트 주소 🎁
> [https://market-13.herokuapp.com/](https://market-13.herokuapp.com/)

- 시뮬레이션 화면 🎉

![시뮬화면](./public/images/simulation.gif)

## 프로젝트 개요🧸

- 이번에 우아한테크캠프 3기 첫 페어프로그래밍 프로젝트로 배민상회 로그인/회원가입 구현 프로젝트를 진행했습니다

## 구현한 내용

- express-session으로 쿠키 세션을 이용하여 회원가입과 로그인을 구현
- crypto모듈로 비밀번호를 해시화해서 사용
- 데이터베이스는 클래스 객체를 이용해서 user를 생성하고 json데이터 형태로 사용자 추가, 삭제, 조회 기능을 수행함
- view 템플릿 엔진으로 pug를 사용했습니다


## 회원가입 페이지 🎊 

### 1. 입력창 유효성 검사
- 입력창에 foucs out하는 시점에서, `올바른 조건이 아닌 경우 빨간색 테두리와 에러메시지`를 보여줍니다 (아이디, 비밀번호, 비밀번호 확인 유효성 검사)

- 이메일 뒷자리는 이메일선택에 의해서 동작하며, ‘직접입력'을 선택하면 직접 작성할 수 있습니다 
- 가입완료 버튼을 선택했을때, 현재 오류가 있는 영역이 있다면 해당 input 창으로 포커스를 이동합니다


### 2. 휴대폰 인증받기

- 휴대폰 인증받기는 ‘인증받기' 버튼을 눌러 진행할 수 있는데 모달 창이 띄워지며 랜덤한 인증번호 6자리와 함꼐 ‘인증번호를 확인해주세요' 라는 메시지를 보여줍니다.

- 모달창은 닫기 버튼이나 배경을 선택하여 끌 수 있습니다

- 모달창을 끄면 인증번호 6자리 입력을 할 수 있는 input 창이 휴대폰 입력창 아래 새롭게 노출됩니다
- `인증받기` 버튼을 누른 후 `2분` 카운트다운이 화면에  노출된다.
2분안에 입력을 하지 못한 경우 ‘입력시간을 초과하였습니다' 라고 메시지를 노출한다. 

### 3. 주소찾기 

- 주소는  선택정보를 체크해야 입력 가능한 상태가 됩니다
- 카카오 주소찾기 API를 연결해 우편번호와 주소를 입력할 수 있습니다.

### 4. 약관

- 전체약관을 누르면 나머지 하위 항목이 자동체크된다.
필수항목, 광고성수신동의를 체크하면 전체약관이 자동체크된다.

- 내용을 클릭하면 약관 내용을 볼 수 있습니다. 

## 로그인 페이지 🏮

- 로그인 과정에서의 오류체크는 회원가입에서 진행했던 것처럼 유효성 검사를 합니다.
- 로컬 스토리지로 아이디 저장 기능을 수행합니다. 



## 우테캠 첫 프로젝트 진행 1주간의 `회고` 📝

###  좋았던 점
- 수현: 조원들이 베이스 지식을 어느 정도 가지고 있어서 어떻게 구현할 지 논의하는 것이 수월했다
- 해랑: 기존에 구현할 수 있었던 지식을 실제로 개발하면서 활용해볼 수 있었고 추가적인 지식을 습득해서 실력을 쌓을 수 있었다


### 아쉬웠던 점 
- 해랑: 구현하고자 했던 것을 대부분 하긴했는데 완벽하게 마무리할 수 있는 시간이 부족해서 아쉬웠다
- 수현: 초반부터 페어 프로그래밍을 진행할 때 분업이 되어버려서 서로 코드를 작성했던 것에서 놓치는 부분들 혹은 잘 이해하지 못한 부분들이 있어서 아쉬웠음. 
  - pull request에 의존했던 부분이 있음
- 해랑: 초반에 서로의 코딩 스타일이 달라서 맞춰가는 과정에서 많이 배웠지만 초반에는 맞춰가는 것에 어려움을 느꼈다 (분업과 협업의 충돌, 코드 방식 정하기 등)   
- 수현: 코드 리뷰에 좀 더 적극적으로 참여해서 수용하지만 말고 같이 개선해나가자 (함수 변수 이름, 정의 방식등도 논의하고 싶다)


## 앞으로 하고 싶은 것 💖
- 앞으로 프로젝트를 진행할 때는 협업을 어떻게 할 지 다시 한번 깊게 생각해보고 논의한 후에 진행하고 싶다 
- 프로젝트를 완성하는 것에 급급해하지 말고 `분업`이 아닌 `협업`을 할 수 있도록 노력하자
