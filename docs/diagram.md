`mermaid
erDiagram
    USER {
        int user_id PK
        string name
        string email
    }
    BOOK {
        int book_id PK
        string title
        string author
        string status
    }
    LOAN {
        int loan_id PK
        date borrow_date
        date return_date
    }

    USER ||--o{ LOAN : "borrows"
    BOOK ||--o{ LOAN : "is loaned"
