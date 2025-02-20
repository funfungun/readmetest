## 요구사항

### 기본
- [x] PostgreSQL을 이용하여 데이터베이스 구성
- [x] 데이터 모델 간의 관계를 고려하여 `onDelete` 설정
- [x] 데이터베이스 시딩 코드 작성
- [x] 모든 API에 적절한 에러 처리 적용
- [x] 각 API 응답에 적절한 상태 코드 반환

### 중고마켓
- [x] `Product` 스키마 작성
  - 필드: `id`, `name`, `description`, `price`, `tags`, `createdAt`, `updatedAt`
  - 관계 설정 및 필요한 추가 필드 설정
- [x] `Product API` 구현
  - `POST /products`: 상품 등록 API (`name`, `description`, `price`, `tags` 입력)
  - `GET /products/:id`: 상품 상세 조회 API (`id`, `name`, `description`, `price`, `tags`, `createdAt` 조회)
  - `PATCH /products/:id`: 상품 수정 API
  - `DELETE /products/:id`: 상품 삭제 API
  - `GET /products`: 상품 목록 조회 API (`id`, `name`, `price`, `createdAt` 조회)
    - 최신순 정렬, `name`과 `description`에 포함된 단어로 검색, offset 방식 페이지네이션 기능 포함

### 자유게시판
- [x] `Article` 스키마 작성
  - 필드: `id`, `title`, `content`, `createdAt`, `updatedAt`
- [x] `Article API` 구현
  - `POST /articles`: 게시글 등록 API (`title`, `content` 입력)
  - `GET /articles/:id`: 게시글 상세 조회 API (`id`, `title`, `content`, `createdAt` 조회)
  - `PATCH /articles/:id`: 게시글 수정 API
  - `DELETE /articles/:id`: 게시글 삭제 API
  - `GET /articles`: 게시글 목록 조회 API (`id`, `title`, `content`, `createdAt` 조회)
    - 최신순 정렬, `title`과 `content`에 포함된 단어로 검색, offset 방식 페이지네이션 기능 포함

### 댓글
- [x] `Comment` API 구현
  - 중고마켓 댓글
    - `POST /products/:productId/comments`: 댓글 등록 API
    - `GET /products/:productId/comments`: 댓글 목록 조회 API (`cursor` 방식 페이지네이션 포함)
  - 자유게시판 댓글
    - `POST /articles/:articleId/comments`: 댓글 등록 API
    - `GET /articles/:articleId/comments`: 댓글 목록 조회 API (`cursor` 방식 페이지네이션 포함)
  - `PATCH /comments/:id`: 댓글 수정 API
  - `DELETE /comments/:id`: 댓글 삭제 API

### 유효성 검증
- [x] 상품 등록 시 필드(`name`, `description`, `price` 등) 유효성 검증 미들웨어 구현
- [x] 게시글 등록 시 필드(`title`, `content`) 유효성 검증 미들웨어 구현

### 이미지 업로드
- [x] `multer` 미들웨어를 사용하여 이미지 업로드 API 구현
  - 업로드된 이미지를 서버에 저장하고, 이미지 경로를 응답 객체에 포함하여 반환

### 에러 처리
- [x] 모든 예외 상황을 처리할 수 있는 에러 핸들러 미들웨어 구현
  - 서버 오류(`500`), 사용자 입력 오류(`400` 시리즈), 리소스 찾을 수 없음(`404`) 등 상황에 맞는 상태값 반환

### 라우트 중복 제거
- [x] `app.route()`로 중복 라우트 경로 제거
- [x] `express.Router()`를 활용하여 중고마켓/자유게시판 관련 라우트를 별도 모듈로 구분

### 배포
- [x] `.env` 파일을 사용하여 환경 변수 설정
- [x] CORS 설정
- [x] `render.com`으로 배포

## 주요 변경사항
- 데이터베이스 스키마 및 관계 설정
- 각 기능에 대한 API 구현
- 유효성 검증 및 에러 핸들러 적용
- 이미지 업로드 API 구현
- 라우트 모듈화 및 코드 정리
- 배포 환경 설정 및 배포

## 스크린샷

## 멘토에게
- 리뷰 부탁드립니다. 감사합니다!
