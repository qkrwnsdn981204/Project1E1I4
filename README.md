# 😀 박준우 프로젝트

- - -

### 🛒쇼핑몰 & 관리자 모드 기반 ChatBot 구현

#### **● 프로젝트 명** : E 1 I 4

#### **● 프로젝트 설명** : 원데이 클래스 강의 쇼핑몰 사이트

- **Preview**<br>
    - 회원가입
      <br>
      <img src="https://github.com/qkrwnsdn981204/ParkJunwooProjects/assets/154858222/e55fd7e0-d012-4bad-a690-24fd955b4027" width="800" height="400"/>
      <br>
      <br>
    - 일반 회원 로그인
      <br>
      <img src="https://github.com/qkrwnsdn981204/ParkJunwooProjects/assets/154858222/2639b847-c487-497e-822b-29450975ac48" width="800" height="400"/>
      <br>
      <br>
    - Oauth2 로그인
      <br>
      <img src="https://github.com/qkrwnsdn981204/ParkJunwooProjects/assets/154858222/457c367a-a333-46bc-85f6-1cbbefa7cd10" width="800" height="400"/>
      <br>
      <br>
    - 수정, 삭제
      <br>
      <img src="https://github.com/qkrwnsdn981204/ParkJunwooProjects/assets/154858222/792b889d-2f97-4a45-ac20-472404dfc9f1" width="800" height="400"/>


#### **● 프로젝트 소개**

> 사용자에게 참신하고 편리한 서비스를 제공하기 위해 사용자 경험을 중심으로 한 웹사이트 디자인,
> 사용자와 관리자 간의 원활한 커뮤니케이션을 가능하게 하는 챗봇 시스템 등
> 더 투명하고 신뢰할 수 있는 정보를 제공하여 적극적인 참여를 유도하였다.

#### **● 팀원**

> 박준우 (팀장) : DB설계, 회원 CRUD, Oauth2, Security, CI/CD

> 손** (팀원) : 관리자페이지, ChatBot, 강사소개 페이지, 메뉴바, INDEX 애니메이션 기능

> 심** (팀원) : 게시판 CRUD, Naver API

> 이** (팀원) : 상품 CRUD, Cart 담당

> 조** (팀원) : INDEX 페이지, 1:1 문의내역, Naver API

<details>

<summary> 기술 스택 </summary>

| 카테고리       | 요소                                                                                                                  |
|------------|---------------------------------------------------------------------------------------------------------------------|
| 프로그래밍 언어   | JAVA                                                                                                                |
| 개발 툴       | IntelliJ                                                                                                            |
| 프레임워크      | Spring Boot 2.7.11                                                                                                  |
| 라이브러리 및 DI | Spring WEB(MVC), Thymeleaf, Spring Data JPA, Lombok, SpringSecurity5 <br/>, websocket, validation, OAuth2, security |
| 데이터베이스     | MySql8                                                                                                              |
| ORM        | Spring Data JPA (JAVA(SQL))                                                                                         |
| 템플릿 엔진     | Thymeleaf (HTML + Data)                                                                                             |
| Frontend   | css, javaScript, html, ajax                                                                                         |
| 설정         | application.yml, application-oauth2.yml                                                                             |

</details>

<details>

<summary> 프로젝트 일정 </summary>

![img.png](../images/Project1/project1plan.png)

</details>

<details>

<summary> ER 다이어그램 </summary>

![img.png](../images/Project1/project1ERD.png)

</details>

<details>
<summary>기능 구현</summary>

### DB 설계

| **No** | **주요 Entity** | **상세 Entity**                                           |
|--------|---------------|---------------------------------------------------------|
| 1      | member        | member, memberFile                                      |
| 2      | shop          | shop, cart, cartShopList, shopFile, shopReply, shopLike |
| 3      | board         | board, boardReply, boardFile                            |

### 회원 CRUD

| **No** | **기능**  | **설명**                                                                            |
|--------|---------|-----------------------------------------------------------------------------------|
| 1      | 회원가입    | 강사와 수강생으로 나누어 회원가입 <br> 비밀번호 확인 기능 <br> 전화번호 자동 하이픈(-) <br> 프로필 사진 추가 <br> 유효성 검사 |
| 2      | 회원정보 조회 | 회원 개인 정보 조회 <br> 간이 장바구니 기능                                                       |
| 3      | 회원수정    | 프로필사진, 개인정보, 비밀번호 수정                                                              |
| 4      | 회원삭제    | 회원 탈퇴 기능                                                                          |

### 로그인

| **No** | **기능**     | **설명**                                                                |
|--------|------------|-----------------------------------------------------------------------|
| 1      | 일반 회원 로그인  | Security를 통해 회원가입한 아이디로 로그인                                           |
| 2      | Oauth2 로그인 | Oauth2를 이용하여 google, kakao, naver 아이디로 로그인 <br> 로그인시 아이디가 없으면 자동 회원가입 |

### CI/CD

| **No** | **설명**                           |
|--------|----------------------------------|
| 1      | 배포할 파일 github push               |
| 2      | git actions 실행                   |
| 3      | 빌드한 프로젝트 압축                      |
| 4      | 압축된 파일 S3 복사                     |
| 5      | S3에 있는 파일을 CodeDeploy를 통해 EC2 배포 |
| 6      | EC2에서 jar 파일 실행                  |

</details>


**[⬆ 위로 가기](#쇼핑몰--관리자-모드-기반-ChatBot-구현)**
