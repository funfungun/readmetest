# 3팀

https://plum-supernova-9cd.notion.site/1-SEVEN-3-1ac7c057a4ec8003ad43f7721a18d2dc?pvs=4

## 팀원 구성
- **김건** https://github.com/funfungun
- **김한솔** https://github.com/kimhansol2
- **장현태** https://github.com/gusxo999
- **이민호** https://github.com/toomin5

---

## 프로젝트 소개
![이미지 설명](https://github.com/user-attachments/assets/0c9404ce-d7c5-4948-9ed2-303165dfcffe)
- **프로젝트명:** 🏋️‍♀️ SEVEN, 운동 인증 커뮤니티 서비스. 땀 흘린 순간을 기록하고, 함께 성장하는 운동 인증 커뮤니티! 오늘의 운동을 인증하고 사람들과 공유하며 동기부여를 얻어보세요. 당신의 꾸준함이 곧 누군가의 영감이 됩니다! 💪🔥
#운동인증 #함께성장 #SEVEN
- **프로젝트 기간:** 2025.02.25 ~ 2025.03.18

### 기술 스택
- **Backend:** Express.js, PrismaORM
- **Database:** PostgreSQL
- **공통 Tool:** Git & Github, ZEP, Discord, Notion, Figma

---

## 팀원별 구현 기능 상세

### 장현태
![장현태 작업 이미지]
- **그룹 등록 API** 구현
  - 그룹명, 설명, 닉네임, 비밀번호, 사진(한 장), 태그, 목표 횟수, 디스코드 웹훅 URL, 디스코드 서버 초대 URL을 입력하여 그룹을 등록
- **그룹 목록 조회 API** 구현
  - 각 그룹의 그룹명, 닉네임, 사진, 태그, 목표 횟수, 추천수, 참여자수가 표시
  - 페이지네이션 가능
  - 최신순, 추천순, 참여자순으로 정렬
  - 그룹명으로 검색
- **그룹 상세 조회 API** 구현
  - 그룹명, 설명, 닉네임, 사진, 태그, 목표 횟수, 참여자 수, 디스코드 서버 초대 URL을 조회
- **운동 기록 랭킹 조회 API** 구현
  - 운동 기록 많은 순으로 주간, 월간 랭킹 조회가 가능
  - 닉네임, 기록 횟수, 누적 시간 조회가 가능
  - 페이지네이션이 가능

### 김한솔
![김한솔 작업 이미지]
- **그룹 수정 API** 구현
    - 비밀번호를 입력하여 그룹 등록 시 입력했던 비밀번호와 일치할 경우 그룹 수정
- **그룹 삭제 API** 구현
    - 비밀번호를 입력하여 그룹 등록 시 입력했던 비밀번호와 일치할 경우 그룹 삭제
- **그룹 참여 API** 구현
    - 닉네임, 비밀번호를 입력하여 그룹 참여
        - 그룹 내에서 중복된 닉네임 등록 불가
    - 비밀번호 인증을 통해 그룹 참여 취소가 가능하며, 참여를 취소하면 해당 닉네임이 생성한 운동 기록은 모두 삭제

### 김건
![김건 작업 이미지]
- **운동 기록 등록 API** 구현
    - 닉네임, 운동 종류(달리기, 자전거, 수영), 설명, 시간, 거리, 사진(여러장 가능), 비밀번호를 입력하여 운동 기록을 등록
    - 타이머를 통해 측정된 실제 운동한 만큼의 시간만 입력 가능
    - 닉네임, 비밀번호를 확인하여 그룹에 등록된 유저일 때만 기록 등록이 가능
    - 새로운 운동 기록이 등록 되었을 때 그룹에 등록된 디스코드 웹 서버로 알림을 전송
- **운동 기록 목록 조회 API** 구현
    - 그룹 내에 등록된 모든 유저의 운동 기록 조회가 가능
    - 닉네임, 운동 종류, 시간, 거리, 사진이 표시
    - 최신순, 운동시간순으로 정렬 가능
    - 닉네임으로 검색 가능
    - 페이지네이션이 가능
- **운동 기록 상세 조회 API** 구현
    - 운동 종류, 설명, 사진(여러장), 시간, 거리, 닉네임 조회가 가능
- **이미지 파일 업로드 API** 구현

### 이민호
![이민호 작업 이미지]
- **그룹 추천 API** 구현
    - 그룹 추천이 호출될 때마다 추천수가 1씩 증가
- **그룹 추천(좋아요) 취소 API** 구현
- **태그 목록 조회 API** 구현
- **태그 상세 조회 API** 구현
- **그룹 배지 자동 획득 API** 구현
    - 참여자 10명 이상
    - 운동 기록 100개 이상
    - 추천수 100 이상

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
https://one-seven-3.onrender.com

## 프로젝트 회고록
[발표자료 링크 또는 첨부파일]

