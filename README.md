# 36기 1차 프로젝트 'BODYLIKE' 
![스크린샷 2022-08-26 오후 4 28 45](https://user-images.githubusercontent.com/107386533/186849064-278872a7-fc09-4ac6-bb1f-77d3d01f0958.png)

- 바디 용품 커머스 사이트 '바디럽'을 클론하였습니다. 
- 외부 라이브러리 사용 없이, React CRA 툴을 사용하여 구현하였습니다. 

## 개발 기간
- 2022년 8월 16일 ~ 2022년 8월 25일 10일

## 팀 코너 
- 프론트엔드 개발자 : 최규선, 조은지, 조민재
- 벡엔드 개발자 : 이지현, 백민석

## 사용 기술 
- 프론트엔드 : JavaScript, React.js, Sass
- 백엔드 : Node.js, MySQL 8.0, Postman, Express 
- 협업 툴 : Trello, Slack

## 구현 기능 
- 최규선 : 메인 페이지, 페이지네이션, 리뷰 페이지 
- 조은지 : 로그인/회원가입 페이지, 상품 상세 페이지
- 조민재 : 내비게이션 바/푸터, 상품 검색 기능, 장바구니 페이지

<br />

#### 로그인/회원가입 
![로그인](https://blog.kakaocdn.net/dn/btGJ8L/btrKGp2I5Pl/do5RvatE0KIkYPpOWQ93y0/img.gif)
- 로그인창에서 회원가입 버튼 누를시 회원가입 창으로 넘어감
- 회원가입창/ 로그인창에서 아이디 창 '@', 5글자 && 비밀번호 창 5글자 이상 입력시 회원가입 버튼 활성화 (비밀번호 영문 소대문자 없을 시 알림창 뜸)
- 로그인창에서 id, pw 기입 후 로그인 버튼 누를 시 서버와 통신 후 로컬 스토리지에 토큰 발급, 메인창으로 넘어감
- 왼측 상단 로고 클릭시 메인으로 이동

<br />

#### 내비게이션 바 

- 검색창을 통한 검색 기능
- 각 카테고리별 상품 리스트 확인 가능한 카테고리 메뉴 바 구현 
- 장바구니에 상품 담기 시 상품 수량에 따라 카운트되는 뱃지 구현
- 로그인/로그아웃 상태 전환 시 텍스트 전환 기능 

<br />

#### 메인
<<u><strong>무한케러셀</strong></u>>
- 매 3초마다 우측으로 슬라이드
- 마지막 페이지에서 우측으로 슬라이드 시 첫번째 슬라이드를 불러옴
- 좌 우 이동 버튼

<img src="https://img.shields.io/badge/react-61DAFB?style=for-the-badge&logo=react&logoColor=black">


![carousel](https://user-images.githubusercontent.com/73376092/186857763-75f04bc4-44d0-4d3a-bdf3-ef63435fd1ff.gif)


<<u><strong>페이지네이션</strong></u>>


- 이전/다음 및 숫자 페이지 버튼 
- 페이지 클릭 시 쿼리스트링으로 요청을 보내 서버에서 해당 페이지에 부합하는 상품들을 출력

<br />

#### 카테고리별 상품 목록
<img width="1080" alt="스크린샷 2022-08-27 오후 2 01 44" src="https://user-images.githubusercontent.com/107386533/187016786-dbded25d-333e-48ed-8b48-f896a5c0dff4.png">

- 각 카테고리 탭 클릭 시 해당하는 상품만 조회할 수 있도록 구현

<br />

#### 검색 기능
![-9102736838140524926________________________________2022-08-26_________________12 24 19 (2)](https://user-images.githubusercontent.com/107386533/187016677-183cd9bd-2d99-4894-9fd8-95d0fbe01132.gif)

- 검색창에 검색어 입력 시 검색어를 포함한 상품만 조회할 수 있도록 구현

<br />

#### 상품 상세

![상세](https://blog.kakaocdn.net/dn/Gn5Xk/btrKGRDLagS/NbKK2AwoV19ixffDPoDqR0/img.gif)
![상세2](https://blog.kakaocdn.net/dn/dltnVp/btrKGOf9axq/4l3PCVMFlp4R9Y3MfMnBbk/img.gif)


- 상품 정보 옆 리뷰 버튼 누르면 하단 리뷰로 슬라이드
- 상품 카운트 음수로 내려갈 시, 재고 이상 누를 시 알림창 뜸
- 상품 카운트 누른 후 장바구니 클릭 시 로그인 되어 있을 시 모달창 뜨면서 장바구니/쇼핑하기 버튼 뜸, 로그인 안 되어 있을 시 알람창 뜨며 로그인 창으로 이동
- 모달 창에서 장바구니 가기 클릭시 제품이 장바구니에 담기며 장바구니로 이동 

<br />

#### 리뷰 
<img src="https://img.shields.io/badge/react-61DAFB?style=for-the-badge&logo=react&logoColor=black">


<<strong>리뷰기입창</strong>>


![product review](https://user-images.githubusercontent.com/73376092/187031637-34d3ee2d-dde0-4f0c-8d6d-aa2aad67d3f5.gif)


- 기존 상품평 리스트 출력
- 기존 상품평 리스트 부재 시 "상품평작성" 버튼이 있는 섹션 출력
- 상품평 버튼 클릭 시 유효성 검사 후 기입창 열림
- 상품평 기입 후 등록하기 버튼 클릭 시 새 리뷰를 포함한 리뷰리스트 출력
- 내 리뷰보기 클릭 시 사용자 토큰에 부합하는 리뷰들을 출력
- 개별 리뷰 삭제 기능

<br />

#### 장바구니 

![-9102736838140524926________________________________2022-08-26_________________12 24 19 (1)](https://user-images.githubusercontent.com/107386533/187016608-1fd0168e-333a-449f-8935-a9acac7f4c21.gif)

- 유저 정보 확인 후 유저가 담은 상품 조회
- 장바구니 내 상품 수량 조절 및 가격 실시간 반영
- 상품 개별 삭제 기능
- 장바구니 비우기(상품 전제 삭제) 기능

<br />

# Reference
- 이 프로젝트는 바디럽 사이트를 참조하여 학습목적으로 만들었습니다.
- 실무수준의 프로젝트이지만 학습용으로 만들었기 때문에 이 코드를 활용하여 이득을 취하거나 무단 배포할 경우 법적으로 문제될 수 있습니다.
- 이 프로젝트에서 사용하고 있는 사진 대부분은 위코드에서 구매한 것이므로 해당 프로젝트 외부인이 사용할 수 없습니다.
