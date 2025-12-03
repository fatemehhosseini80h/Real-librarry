```mermaid
erDiagram
    USER {
        int user_id PK
        string first_name
        string last_name
        string email
    }
    BOOK {
        int book_id PK
        string isbn
        string title
        string author
        string status
    }
    LOAN {
        int loan_id PK
        date date_borrow
        date date_return
    }

    USER ||--o{ LOAN : "borrows"
    BOOK ||--o{ LOAN : "is loaned"
### 🔎 توضیح
- موجودیت‌ها: USER، BOOK، LOAN  
- ارتباط‌ها:  
  - هر کاربر می‌تونه چند کتاب امانت بگیره.  
  - هر کتاب می‌تونه در چند امانت ثبت بشه.  

وقتی این کد رو داخل README.md یا هر فایل .md بذاری، گیت‌هاب خودش دیاگرام رو رندر می‌کنه.  

---

می‌خوای برات یک فلوچارت هم طراحی کنم که جریان کار (ثبت کاربر → انتخاب کتاب → ثبت امانت → بازگرداندن) رو نشون بده؟
