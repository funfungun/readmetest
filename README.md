```mermaid
erDiagram
    USER {
        string id PK
        string email
        string password
        string nickname
        string profileImage
        datetime createdAt
    }

    PRODUCT {
        string id PK
        string title
        string description
        int price
        string category
        string image
        string status
        string sellerId FK
        datetime createdAt
    }

    ARTICLE {
        string id PK
        string title
        string content
        string authorId FK
        datetime createdAt
    }

    COMMENT {
        string id PK
        string content
        string authorId FK
        string articleId FK
        datetime createdAt
    }

    USER ||--o{ PRODUCT : "등록"
    USER ||--o{ ARTICLE : "작성"
    USER ||--o{ COMMENT : "작성"
    ARTICLE ||--o{ COMMENT : "댓글"
```
