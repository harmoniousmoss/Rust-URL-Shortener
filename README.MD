# 🚀 Rust URL Shortener

A simple **URL Shortener** built with **Rust** and **Actix Web**, using in-memory storage (`HashMap`).

## 🌟 Features

✅ Shorten a long URL with a **user-defined short code**  
✅ Retrieve the original URL using a short code  
✅ Redirect users to the original URL  
✅ Prevent duplicate short URLs  
✅ In-memory storage (no database required)  
✅ Simple and lightweight API  

---

## 🔗 API Usage

### **1️⃣ Shorten a URL (User-Defined Short Code)**
**Endpoint:**  
```http
POST /shorten
```

**Request Body (JSON format):**
```
{
    "long_url": "https://www.rust-lang.org",
    "short_url": "rusturlshortener"
}
```

**Example Request (Using Curl):**
```
curl -X POST -H "Content-Type: application/json" \
     -d '{"long_url": "https://www.rust-lang.org", "short_url": "rusturlshortener"}' \
     http://127.0.0.1:8080/shorten
```

**Example Response:**
```
"Shortened URL: http://127.0.0.1:8080/rusturlshortener"
```

### 2️⃣ Redirect to the Original URL
```
GET /{short_code}
```

### 🛠 Technologies Used
* Rust 🦀
* Actix Web (for building web APIs)
* Lazy_static (for global HashMap storage)
* Tokio (for async execution)