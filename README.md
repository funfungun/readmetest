# 3팀

https://plum-supernova-9cd.notion.site/1-SEVEN-3-1ac7c057a4ec8003ad43f7721a18d2dc?pvs=4

## 팀원 구성
- **김건** https://github.com/funfungun
- **김한솔** https://github.com/kimhansol2
- **장현태** https://github.com/gusxo999
- **이민호** https://github.com/toomin5

---

## 프로젝트 소개
- **프로젝트명:** SEVEN, 운동 인증 커뮤니티 서비스
- 땀 흘린 순간을 기록하고, 함께 성장하는 운동 인증 커뮤니티! 오늘의 운동을 인증하고 사람들과 공유하며 동기부여를 얻어보세요. 당신의 꾸준함이 곧 누군가의 영감이 됩니다! 💪🔥
#운동인증 #함께성장 #SEVEN
- **프로젝트 기간:** 2024.08.13 ~ 2024.09.03

### 기술 스택
- **Backend:** Express.js, PrismaORM
- **Database:** MongoDB
- **공통 Tool:** Git & Github, Discord

---

## 팀원별 구현 기능 상세

### 웨인
![웨인 작업 이미지]
- **소셜 로그인 API**
  - 구글 소셜 로그인 API를 활용하여 소셜 로그인 기능을 구현
  - 로그인 후 추가 정보 입력을 위한 API 엔드포인트 개발
- **회원 추가 정보 입력 API**
  - 회원 유형(관리자, 학생)에 따른 조건부 입력 처리 API 구현

### 제이든
![제이든 작업 이미지]
- **회원별 권한 관리**
  - 사용자의 역할에 따라 권한을 설정하는 API 구현
  - 관리자 페이지와 일반 사용자 페이지를 위한 조건부 라우팅 기능 개발
- **반응형 레이아웃 API**
  - 클라이언트에서 전달된 요청에 맞춰 반응형 레이아웃을 위한 API 엔드포인트 구현

### 마크
![마크 작업 이미지]
- **수강생 정보 관리 API**
  - `fetch(GET)`을 사용하여 학생의 수강 정보를 조회하는 API 엔드포인트 개발
  - 수강 정보의 반응형 UI 구성
- **공용 Button API**
  - 공통으로 사용할 버튼 기능을 처리하는 API 구현

### 데이지
![데이지 작업 이미지]
- **관리자 API**
  - Path Parameter를 활용한 동적 라우팅 기능 구현
  - `fetch(PATCH, DELETE)`를 사용하여 학생 정보를 수정하고 탈퇴하는 API 엔드포인트 개발
- **CRUD 기능**
  - 학생 정보 CRUD 기능을 제공하는 API 구현
- **회원관리 슬라이더**
  - 학생별 정보 목록을 carousel 방식으로 보여주는 API 개발

### 제이
![제이 작업 이미지]
- **학생 시간 정보 관리 API**
  - 학생별 시간 정보를 조회하는 API 구현
  - `fetch(GET)`을 통해 실시간 접속 현황을 관리
- **수정 및 탈퇴 API**
  - `fetch(PATCH, DELETE)`을 사용하여 수강생의 개인정보 수정 및 탈퇴 처리
- **공용 Modal API**
  - 공통 Modal 컴포넌트를 처리하는 API 구현

---

## 파일 구조
```
src
 ┣ client
 ┃ ┣ __mocks__
 ┃ ┃ ┣ courses.json
 ┃ ┃ ┗ index.ts
 ┃ ┣ features
 ┃ ┃ ┣ Layout
 ┃ ┃ ┃ ┣ images
 ┃ ┃ ┃ ┃ ┗ codeit-logo-purple.svg
 ┃ ┃ ┃ ┣ Layout.module.scss
 ┃ ┃ ┃ ┣ Layout.stories.tsx
 ┃ ┃ ┃ ┣ Layout.tsx
 ┃ ┃ ┃ ┗ index.ts
 ┃ ┃ ┗ LessonSearch
 ┃ ┃ ┃ ┣ components
 ┃ ┃ ┃ ┃ ┣ CourseResult
 ┃ ┃ ┃ ┃ ┃ ┣ CourseResult.module.scss
 ┃ ┃ ┃ ┃ ┃ ┗ CourseResult.tsx
 ┃ ┃ ┃ ┗ EmptyResult
 ┃ ┃ ┃ ┃ ┣ EmptyResult.module.scss
 ┃ ┃ ┃ ┃ ┣ EmptyResult.tsx
 ┃ ┃ ┃ ┃ ┗ index.ts
 ┃ ┃ ┣ LessonSearch.module.scss
 ┃ ┃ ┣ LessonSearch.stories.tsx
 ┃ ┃ ┣ LessonSearch.tsx
 ┃ ┃ ┗ index.ts
 ┃ ┣ models
 ┃ ┃ ┣ course.d.ts
 ┃ ┃ ┗ react.d.ts
 ┃ ┣ shared
 ┃ ┃ ┣ api
 ┃ ┃ ┃ ┣ base.ts
 ┃ ┃ ┃ ┗ course.ts
 ┃ ┃ ┣ components
 ┃ ┃ ┃ ┣ Button
 ┃ ┃ ┃ ┃ ┣ Button.module.scss
 ┃ ┃ ┃ ┃ ┣ Button.tsx
 ┃ ┃ ┃ ┃ ┗ index.ts
 ┃ ┃ ┃ ┣ CourseInfo
 ┃ ┃ ┃ ┃ ┣ CourseInfo.module.scss
 ┃ ┃ ┃ ┃ ┣ CourseInfo.stories.tsx
 ┃ ┃ ┃ ┃ ┗ CourseInfo.tsx
 ┃ ┃ ┃ ┣ Input
 ┃ ┃ ┃ ┃ ┣ Input.module.scss
 ┃ ┃ ┃ ┃ ┣ Input.stories.tsx
 ┃ ┃ ┃ ┃ ┣ Input.tsx
 ┃ ┃ ┃ ┃ ┗ index.ts
 ┃ ┃ ┃ ┗ Select
 ┃ ┃ ┃ ┃ ┣ images
 ┃ ┃ ┃ ┃ ┃ ┗ triangle-dark.svg
 ┃ ┃ ┃ ┃ ┣ Select.module.scss
 ┃ ┃ ┃ ┃ ┣ Select.stories.tsx
 ┃ ┃ ┃ ┃ ┣ Select.tsx
 ┃ ┃ ┃ ┃ ┗ index.ts
 ┃ ┃ ┗ helpers
 ┃ ┃ ┃ ┣ api
 ┃ ┃ ┃ ┃ ┣ __tests__
 ┃ ┃ ┃ ┃ ┃ ┣ base.test.ts
 ┃ ┃ ┃ ┃ ┃ ┣ helpers.test.ts
 ┃ ┃ ┃ ┃ ┃ ┗ wrapper.test.ts
 ┃ ┃ ┃ ┃ ┣ wrapper
 ┃ ┃ ┃ ┃ ┃ ┣ fetch.ts
 ┃ ┃ ┃ ┃ ┃ ┗ index.ts
 ┃ ┃ ┃ ┣ base.ts
 ┃ ┃ ┃ ┣ error.ts
 ┃ ┃ ┃ ┣ helpers.ts
 ┃ ┃ ┃ ┣ index.ts
 ┃ ┃ ┃ ┗ type.ts
 ┃ ┃ ┗ react-query.ts
 ┣ server
 ┃ ┣ controllers
 ┃ ┃ ┣ authController.ts
 ┃ ┃ ┗ userController.ts
 ┃ ┣ models
 ┃ ┃ ┣ userModel.ts
 ┃ ┃ ┗ courseModel.ts
 ┃ ┣ routes
 ┃ ┃ ┣ authRoutes.ts
 ┃ ┃ ┗ userRoutes.ts
 ┃ ┣ middleware
 ┃ ┃ ┣ authMiddleware.ts
 ┃ ┃ ┗ errorHandler.ts
 ┃ ┣ app.ts
 ┃ ┗ server.ts
 ┣ App.tsx
 ┣ _mixin.scss
 ┣ common.scss
 ┣ index.tsx
 ┣ react-app-env.d.ts
 ┣ reportWebVitals.js
 ┗ setupTests.js
```

---

## 구현 홈페이지
[개발한 홈페이지 링크](https://www.codeit.kr/)

## 프로젝트 회고록
[발표자료 링크 또는 첨부파일]

