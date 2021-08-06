# 프로그램 설명

현재 있는 이미지들을 이용해서 심리테스트를 만드는 페이지

# 화면

## 공통(Common)

- ✅로그인, 회원 가입 버튼 : 목적에 맞는 페이지로 이동하기 위한 버튼 by Na
- ✅로고 : 홈 화면으로 이동 by Tommy

## 메인화면 by Na

- ✅심리테스트 카드 : 심리테스트 페이지로 이동하기 위한 카드
- ✅검색 버튼 : **캐릭터 검색** 과 **심리테스트 검색**, **전체 검색** 세 가지 중 하나를 검색하는 버튼을 만든다.

## 심리테스트 시작 전 화면 by Tommy

- ✅심리테스트 제목
- ✅심리테스트 시나리오 작가
- ✅심리테스트 설명
- ✅시작하기 버튼 : 버튼 Click 시, 시작 시간을 Session에 저장하고, 서버에서 필요한 문제의 정보를 받는다.
- 공유하기 버튼 : 심리 테스트의 링크 공유

## 심리테스트 화면 by Na

- ✅심리테스트 지문
- ✅심리테스트 선택지
- ✅결과보기 버튼 : 버튼 Click 시, [시작시간, 종료시간, 결과값, 테스트ID]

## 결과화면 by Na

- ✅결과 제목
- 결과 설명
- 정확도 버튼 : 설문 조사를 한 사람에게만 보이며, 정확도를 평가하여 응답해주면 해당 결과를 서버로 송신한다. (미응답 시, 무시)
- 공유하기 버튼 : 설문 조사를 한 사람에게만 보이며, 링크를 ClipBoard에 저장한다.
- 나도하기 버튼 : 설문 조사를 하지 않은 사람에게만 보이며, 심리 테스트 시작 전 화면으로 이동한다.
- (+)심리테스트 작가 구경 버튼 : CBTI의 작가의 소개 페이지로 이동

## 심리테스트 시나리오 등록 화면 by Na

### 등록 화면 (1)

- ✅심리테스트 제목 설정
- ✅심리테스트 태그 설정
- ✅다음 / 취소 버튼

### 등록 화면 (2)

- 지문 [+]/[-] 버튼 : 지문 추가/삭제
- 선택지 [+]/[-] 버튼 : 선택지 추가/삭제
- 중복 검사 / 취소 버튼 : 중복 검사 완료 시 등록 화면(3)으로 이동

### 등록 화면 (3)

- 심리테스트 검수하기 / 취소 버튼 : 심리테스트를 검수를 맡기며, 검수자(혹은 관리자)에게 검수 메일을 송신한다.

## 회원 가입 화면 by Tommy

- ✅아이디
- 아이디 중복 체크 : 아이디가 중복되는지 서버에 데이터 송신
- ✅닉네임
- 닉네임 중복 체크 : 닉네임이 중복되는지 서버에 데이터 송신
- ✅이름
- ✅전화번호
- ✅패스워드
- ✅패스워드 확인
- ✅Email :
- 주소 : [카카오 주소 API](https://developers.kakao.com/docs/latest/ko/local/common)를 사용하기 위함
- ✅가입 완료 / 취소 버튼 : 가입 완료 버튼 Click 시, 빈칸 있는지 확인 후 이메일 중복 확인 후 회원 가입 완료한다.

## 로그인 화면 by Na

- ✅아이디
- ✅패스워드
- ✅아이디 찾기
- ✅비밀번호 찾기
- ✅구글 로그인 버튼 : [생활코딩 예제](https://opentutorials.org/course/3424)
- ✅페이스북 로그인 버튼 : [생활코딩 예제](https://opentutorials.org/course/3423)

## 아이디 찾기 화면 by Na

- ✅이메일
- ✅찾기 / 취소 버튼 : 찾기 시, 서버에 동일한 이메일 찾기
- ✅이메일이 존재하면, 아이디를 이메일로 전송한다.

## 비밀번호 찾기 화면 by Na

- ✅이메일
- ✅아이디
- ✅찾기 / 취소 버튼 : 찾기 시, 서버에 동일한 ID, 이메일 찾기
- ✅ID, 이메일이 같은 튜플에 존재하면, 이메일로 비밀번호 변경 사이트를 전송한다.

## 비밀번호 변경 화면 (?) by Tommy

: 해당 페이지는 변경해야하는 ID가 있을 경우, 전송한 이메일 url을 통해 들어오면 변경해야 하는 ID의 세션을 가지며,  
1시간 뒤 또는 비밀번호 변경하기 완료 시, 해당 페이지를 url로 들어오지 못하도록 한다.

- 변경할 비밀번호
- 변경할 비밀번호 확인
- 변경하기 / 취소 버튼 : 변경하기 버튼 click 시, 서버에 비밀번호를 변경하도록 하고, 해당 페이지로 아무도 들어올 수 없게 한다.

## 통계 화면 by Na

- 작가가 게시한 심리테스트의 수 및 조회수
- 작가가 게시한 캐릭터가 사용된 심리테스트 수 및 조회수
- 총 조회수

---

## [DB]

### 1. 회원정보(ID, PassWord, Name, NickName, Address, Group)

- ID(PK), PassWord : 로그인하기 위한 정보
- Name : 개인정보
- NickName : 카페에서 사용할 닉네임
- Phone: 연락 수단
- Address : 택배 보낼 수도 있음
- Group : 관리자 / 유저

### 2. 심리테스트(TestNo, Desc, OpenTime, StarTime)

- TestNo(PK) : Test 식별자
- TestHead : 심리테스트 제목
- TestProblemInfo : 문제 전체를 담음 (아래에 변경사항 - 지문관리)
- Desc : 테스트 설명
- uploadTime: 심리테스트를 올린 시간
- isPost : 게시 가능 여부

### 3. 심리테스트\_History (HistID, IP, Device, Result, Satisfaction, StartTime, EndTime, TestNo, ID)

- HistID : 년+월+일+초+IP로 아이디 생성
- IP, Device: 조회수 사기를 막기 위함
- Result : 심리테스트 결과
- Satisfaction : 만족도
- StartTime, EndTime : 평균 완료시간
- TestID : 심리테스트 식별자 (FK)
- ID : 회원 확인 (FK)

---

# 변경 사항

## 지문관리

심리테스트의 지문을 DB에서 저장하되, 한 심리테스트의 지문에 문제마다 구분자(ex: \)를 추가하여 지문 전체를 한 셀에 저장한다. 문제들은 프로그래밍적으로 문제를 분리하여 배열로 재정의한다. 이로써 DB에서 불필요한 컬럼 생성을 막고자 한다. 예시는 **"심리테스트 문제 정보"**의 내용에 대한 예시이다.

예시) let a = "1.나는 파댕이인가? \1)맞다 \2)아니다 \\ 2. 나는 파공햇인가? 1) 맞다 2) 아니다 \\ 3. 나는 씨인가? 1)맞다 2)아니다"

let aryA = a.split("\\");
for( itemInfo of aryA) {
items = itemInfo .split("\");
const subject = items[0]; // 제목(문제)
const seletItem = items.slice(1); // 선택지
}

[심리테스트 종류 테이블]
심리테스트 코드,
심리테스트 이름,
심리테스트 문제 정보,
심리테스트 종류,
심리테스트 문제방식,
심리테스트 문제 코드

---

# 문서 버전

- 2021.06.04 v1220
- 2021.07.11 v1280
- 2021.07.24 v1290
- 2021.07.25 v1300 [최근 문서]
