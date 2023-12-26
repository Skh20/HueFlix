# **Portfolio - Hue Flix**

<details>
  <summary>
    Content
  </summary>


  - [ 개요](#개요)
  - [ 내용](#내용)
  - [ 구현기능](#구현기능)
  - [ 프로젝트중 아쉬웠던 점](#프로젝트중 아쉬웠던 점)
</details>


# **개요**
- 프로젝트 명 : HueFlix

- 일정 : 2023년 12월 4일 ~ 2023년 12월 22일

- 개발 목적: 

  1. 영화를 좋아하는 사용자들에게 다양한 정보를 제공하기 위한 
웹 사이트 제작

  2. API를 활용한 컨텐츠 제작

  3. 학원 수강기간동안 배웠던 기술을 사용하여 최대한 상용서비스와
 비슷하게 구현하도록 노력

- 개발 환경
    - Server : Apache-tomcat-9.0.0

    - Java EE : Eclipse (version 2023-06)

    - Database : Oracle SQL developer

    - Language : Java, Jsp, HTML, CSS, JavaScript, SQL, Spring Legacy, mybatis

    - Framework : Spring Tool suite 3.9.1


# 내용
- 팀원 역할
    - 공통: 웹사이트 UI 기획 및 구현, ERD 설계
    - 신민하: 영화정보 구현(영화 API 활용), 게시판 UI/UX 구현
    - 신수인: 메인 홈페이지 UI 및 로그인/회원가입 구현, 회원정보 수정
       구현, 권한별 기능 구현
    - 임지선: 상영예정작 API를 활용하여 정보 구현, 메인 UI/UX 기능
 구현, 영화상세정보 메뉴 기능 구현
    - 이도민: 공지사항 게시판 CRUD 구현, 댓글 구현, 영화정보 UI 구현
    - 심기훈: 영화정보의 평점 및 댓글 구현, 영화정보 UI/UX 구현,
 공지사항 CRUD 구현
    - 김보성: 영화정보 UI 및 개발, 유지보수, 영화정보 UI/UX 구현
    - 박다진솔: 검색페이지 구현, 검색결과에서 영화 상세정보 이동 구현

- DB ERD 설계
![휴플릭스 프로젝트](https://github.com/Skh20/HueFlix/assets/148019116/c9e9d2e3-d852-4715-8fd1-4c4f36589843)


# 구현기능

### 메인페이지
![메인](https://github.com/Skh20/HueFlix/assets/148019116/d793e717-006e-4cb4-93c6-10656077d9ca)

- 설명
    - 영화를 슬라이드로 배치되어 있는 페이지 
    - DB는 TMDB 사이트의 API를 사용
    - JavaScript의 Ajax 함수를 사용하여 TMDB API에 데이터를 요청
    API에서 반환한 JSON 형식의 데이터를 받아와서 처리

### 회원가입
![회원가입](https://github.com/Skh20/HueFlix/assets/148019116/d3836992-499b-4780-95af-49b3bb8af9d3)

- 회원가입 버튼 활성화시 회원가입 메뉴로 이동


### 로그인
![로그인](https://github.com/Skh20/HueFlix/assets/148019116/01745834-7e76-481c-8447-99a9d30810f1)

- 로그인시 아이디 비밀번호를 DB에서 확인후 무결성검사 진행
- 로그인시 메인페이지로 이동

### 회원정보수정

#### 헤더토글
![헤더토글](https://github.com/Skh20/HueFlix/assets/148019116/2e22ef44-c5fc-4bc3-8d82-d7394f498f83)

- 로그인 후 정보 수정탭을 사용하여 하위 메뉴로 이동

#### 내 정보 수정
![회원정보수정](https://github.com/Skh20/HueFlix/assets/148019116/749a0a9a-653a-4660-8e8e-ff11231a60d6)

- 개인 닉네임 패스워드를 변경할 수 있음

![회원정보수정 비밀번호(틀림)](https://github.com/Skh20/HueFlix/assets/148019116/b98f1d7c-70d4-4479-8f76-5d5ffa0a18a0)

- 비밀번호는 무결성 검사후 변경과 확인이 동일하여야만 수정가능

### 현재 상영작

![현재상영중](https://github.com/Skh20/HueFlix/assets/148019116/2dad1ee8-be22-45d8-90a1-cad03004b9e5)

- API를 실시간으로 받아와 현재시간 기준으로 상영중인 영화를 표기

### 개봉 예정작

![개봉예정](https://github.com/Skh20/HueFlix/assets/148019116/25de0220-1ede-49ea-b9f6-dee9b89c5509)
- 현재시간기준 개봉예정인 작품을 표기

### 게시판
##### 공지사항 메인페이지
![게시판(관리자)](https://github.com/Skh20/HueFlix/assets/148019116/d9b8c8bd-f00b-4989-9c6f-b048f0012ed8)
- 공지사항을 작성하여 영화 관련된 내용을 표기
- 페이지네이션 기능을 구현하여 10개의 글이 넘어가면 
  페이징되게 구현

##### 공지사항 Read
![게시판read(관리자)](https://github.com/Skh20/HueFlix/assets/148019116/5ea6ee87-8772-42d2-880e-65d0e0602f59)
- 관리자 계정으로만 CRUD기능 구현
- 일반계정 로그인시 Read만 가능

### 영화 상세 정보
##### 줄거리
![줄거리](https://github.com/Skh20/HueFlix/assets/148019116/96dc5ac2-c3ca-41a4-bf4b-5b458b096871)
- 영화 포스터 클릭시 줄거리 페이지로 이동
- API를 기반으로 영화 상세 줄거리 내용표기

##### 출연
![출연](https://github.com/Skh20/HueFlix/assets/148019116/316a8e2c-70d2-4823-aa42-ed16416f0bac)
- 영화 주연 및 출연 배우들의 이미지 확인가능

##### 영상/포토
![영상포토](https://github.com/Skh20/HueFlix/assets/148019116/3a8109c6-a727-42ba-9e21-f2291f9208e1)
- 영화 관련 사진 및 광고 영상등 시청가능

##### 평점
![평점댓글](https://github.com/Skh20/HueFlix/assets/148019116/408da72f-e7ac-4b10-ba0f-709d70755621)
- 평점 등록 및 영화 관련 개인 평가 가능
- 로그인계정 닉네임을 받아와 작성자에 표기
- 별점은 Radio 박스로 받아와서 처리

### 검색
![검색창](https://github.com/Skh20/HueFlix/assets/148019116/468e181c-564e-4377-b9ae-70304eaa804a)
- 헤더에 검색창 구현
- 검색후 전체, 영화, 영화인으로 태그 구분 기능 추가

### 프로젝트중 아쉬웠던 점
