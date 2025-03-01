# 📌 JSON Web Token (JWT) and Secure API Design in Python & JavaScript

## 1️⃣ What is JWT?

**JWT (JSON Web Token)** is a compact, URL-safe token format used to securely transmit information between parties as a JSON object. It is commonly used for **authentication and authorization** in web applications.

### 🔹 Structure of a JWT
![](../Pasted%20image%2020250301172059.png)
A JWT consists of three parts:

1. **Header**: Specifies the type of token (`JWT`) and signing algorithm (e.g., `HS256`, `RS256`).
2. **Payload**: Contains claims (user data, expiration, etc.).
3. **Signature**: Ensures integrity and authenticity.

Example:
```JSON
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyX2lkIjoxMjM0NTYsImV4cCI6MTY5OTk5OTk5OX0.GhT9Hxj5Wn0eWFXgKcBx
```

## 2️⃣ When to Use JWT?

✅ **Use JWT for:**

- Stateless authentication (Bearer tokens in APIs)
- Single Sign-On (SSO)
- Secure transmission of claims

❌ **Avoid JWT when:**

- You need real-time revocation (Use OAuth with sessions instead)
- Storing sensitive information (JWTs can be decoded)

---

## 3️⃣ Secure API Design Principles

1. **Use HTTPS** for all API requests (`TLS 1.2+`)
2. **Validate JWTs** properly (issuer, audience, expiration)
3. **Use strong signing algorithms** (`RS256` > `HS256`)
4. **Implement token expiration** and refresh mechanisms
5. **Follow the principle of least privilege** (Scopes & roles)
6. **Prevent JWT-related attacks** (replay attacks, brute force)

---

# 🐍 Implementing JWT in Python (FastAPI + PyJWT)

### 📌 Install Dependencies
``` bash
pip install fastapi uvicorn pyjwt python-dotenv
```

### 📌 Generate and Verify JWT in Python

```python
import jwt
import datetime
from fastapi import FastAPI, Depends, HTTPException
from fastapi.security import OAuth2PasswordBearer
from dotenv import load_dotenv
import os

load_dotenv()
SECRET_KEY = os.getenv("SECRET_KEY", "your_default_secret_key")

app = FastAPI()
oauth2_scheme = OAuth2PasswordBearer(tokenUrl="token")

# Function to create JWT
def create_jwt(data: dict, expires_in: int = 3600):
    payload = data.copy()
    expire = datetime.datetime.utcnow() + datetime.timedelta(seconds=expires_in)
    payload.update({"exp": expire})
    return jwt.encode(payload, SECRET_KEY, algorithm="HS256")

# Function to verify JWT
def verify_jwt(token: str):
    try:
        decoded = jwt.decode(token, SECRET_KEY, algorithms=["HS256"])
        return decoded
    except jwt.ExpiredSignatureError:
        raise HTTPException(status_code=401, detail="Token expired")
    except jwt.InvalidTokenError:
        raise HTTPException(status_code=401, detail="Invalid token")

# Secure API route
@app.get("/protected")
def protected_route(token: str = Depends(oauth2_scheme)):
    return verify_jwt(token)

# Run the server
if __name__ == "__main__":
    import uvicorn
    uvicorn.run(app, host="127.0.0.1", port=8000)

```


### 🔹 Key Security Practices in Python:

- **Use `RS256` for stronger security** (`HS256` uses a shared secret, while `RS256` uses private/public keys)
- **Set short expiration time for JWTs**
- **Implement refresh tokens** (for issuing new tokens without re-authentication)

# 🚀 Implementing JWT in JavaScript (Node.js + Express)

### 📌 Install Dependencies

```bash
npm install express jsonwebtoken dotenv cors
```

### 📌 Generate and Verify JWT in JavaScript


```javascript
require('dotenv').config();
const express = require('express');
const jwt = require('jsonwebtoken');

const app = express();
app.use(express.json());

const SECRET_KEY = process.env.SECRET_KEY || "your_default_secret_key";

// Generate JWT
function createJWT(payload, expiresIn = "1h") {
    return jwt.sign(payload, SECRET_KEY, { expiresIn });
}

// Middleware to verify JWT
function verifyJWT(req, res, next) {
    const token = req.headers["authorization"];
    if (!token) return res.status(403).json({ error: "Token required" });

    jwt.verify(token.split(" ")[1], SECRET_KEY, (err, decoded) => {
        if (err) return res.status(401).json({ error: "Invalid token" });
        req.user = decoded;
        next();
    });
}

// Public Route
app.get("/", (req, res) => {
    res.json({ message: "Welcome to Secure API" });
});

// Protected Route
app.get("/protected", verifyJWT, (req, res) => {
    res.json({ message: "Access granted", user: req.user });
});

// Start Server
app.listen(5000, () => console.log("Server running on port 5000"));

```

### 🔹 Key Security Practices in JavaScript:

- **Use environment variables** to store secrets (`dotenv`)
- **Implement refresh tokens** to issue new JWTs
- **Use `RS256` (asymmetric encryption) for better security**

---

# 🔥 Best Practices for Secure JWT Authentication

|**Practice**|**Why It’s Important?**|
|---|---|
|**Use HTTPS**|Prevents token interception|
|**Short expiration time**|Reduces attack window in case of compromise|
|**Implement refresh tokens**|Allows token renewal without user re-authentication|
|**Use strong secrets**|Protects against brute-force attacks|
|**Whitelist trusted issuers**|Prevents unauthorized token sources|
|**Store JWT securely**|Avoid storing in `localStorage`, use `httpOnly` cookies|
|**Validate claims**|Ensure `exp`, `aud`, `iss` are correct|

---

# 🔑 JWT vs OAuth2: Which One to Use?

|Feature|JWT|OAuth2|
|---|---|---|
|**Type**|Token-based authentication|Authorization framework|
|**Use Case**|API authentication|Delegated access (SSO, third-party)|
|**Security**|Stateless, vulnerable to theft|Secure with refresh tokens|
|**Implementation**|Simple|More complex (requires OAuth server)|

**🔹 When to Use OAuth2?**

- If you need **third-party authentication** (Google, Facebook login)
- If **token revocation** is necessary
- If dealing with **multiple microservices** securely

---

# 🎯 Final Thoughts

✅ **JWT is great for stateless authentication** in APIs, but must be **secured properly**.  
✅ **Use OAuth2** for **complex authorization flows** (SSO, delegated access).  
✅ **Python (FastAPI)** and **JavaScript (Express.js)** both provide **simple yet secure** ways to implement JWT.

🔹 **Next Steps?**

- Implement **refresh tokens** 🔄
- Secure JWTs with **asymmetric encryption (`RS256`)** 🔑
- Store JWTs in **secure httpOnly cookies** instead of `localStorage` 🍪

Want hands-on practice? Try building a **JWT-based authentication system** with **role-based access control (RBAC)**! 🚀

Let me know if you need help with any specific implementation! 💡**