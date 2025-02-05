## 요구사항

### 기본
- [x] `class` 키워드를 이용하여 `Product` 및 `ElectronicProduct` 클래스를 생성
  - `Product` 클래스의 속성: `name`, `description`, `price`, `tags`, `images`, `favoriteCount`
  - `Product` 클래스의 메서드: `favorite()` (호출 시 `favoriteCount` 증가)
  - `ElectronicProduct` 클래스는 `Product`를 상속하며 `manufacturer` 속성 추가
- [x] `class` 키워드를 이용하여 `Article` 클래스 생성
  - `Article` 클래스의 속성: `title`, `content`, `writer`, `likeCount`
  - `Article` 클래스의 메서드: `like()` (호출 시 `likeCount` 증가)
- [x] 각 클래스에 `constructor` 작성
- [x] 추상화/캡슐화/상속/다형성을 고려하여 코드 작성

- [x] `Article API`를 이용하여 다음 함수 구현:
  - `getArticleList()`: `GET` 요청 (`page`, `pageSize`, `keyword` 쿼리 파라미터 포함)
  - `getArticle()`: `GET` 요청
  - `createArticle()`: `POST` 요청 (`title`, `content`, `image` 포함)
  - `patchArticle()`: `PATCH` 요청
  - `deleteArticle()`: `DELETE` 요청
- [x] `fetch` 또는 `axios` 사용
  - 응답 상태 코드가 `2XX`가 아닐 경우 콘솔에 에러 메시지 출력
  - `.then()`, `.catch()`를 활용하여 비동기 처리

- [x] `Product API`를 이용하여 다음 함수 구현:
  - `getProductList()`: `GET` 요청 (`page`, `pageSize`, `keyword` 쿼리 파라미터 포함)
  - `getProduct()`: `GET` 요청
  - `createProduct()`: `POST` 요청 (`name`, `description`, `price`, `tags`, `images` 포함)
  - `patchProduct()`: `PATCH` 요청
  - `deleteProduct()`: `DELETE` 요청
- [x] `async/await`을 활용하여 비동기 처리
  - `try/catch`를 이용한 오류 처리

- [x] `getProductList()`를 통해 받아온 상품 리스트를 `products` 배열에 저장
  - `tags`에 `"전자제품"`이 포함된 상품은 `ElectronicProduct` 클래스로 생성
  - 나머지 상품은 `Product` 클래스로 생성
- [x] `getArticleList()`를 통해 받아온 아티클 리스트를 `articles` 배열에 저장
  - `Article` 클래스로 생성

- [x] API 관련 함수 분리:
  - `ProductService.js` → `Product API` 관련 함수
  - `ArticleService.js` → `Article API` 관련 함수
- [x] 기타 코드는 `main.js`에 작성
  - `import`를 활용하여 함수 호출 및 동작 확인

### 심화
- [x] `Article` 클래스에 `createdAt` 속성 추가 (`constructor` 호출 시 현재 시간 저장)

## 주요 변경사항
- `class` 기반 설계 적용
- API 호출 로직 구현 (`fetch`/`axios`)
- 데이터에 맞는 인스턴스 생성 및 관리
- 모듈화 (`ProductService.js`, `ArticleService.js`, `main.js`)

## 스크린샷

## 멘토에게
- 따끔한 리뷰 부탁드립니다..
- 
