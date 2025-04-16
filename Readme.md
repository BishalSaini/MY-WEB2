# 📘 Glossary API

A simple ASP.NET Core Web API to manage glossary terms with operations to **create**, **read**, **update**, and **delete** (CRUD).

---

## 🚀 Project Structure

- `GlossaryItem.cs`: Defines the model for glossary terms.
- `GlossaryController.cs`: Contains API endpoints for CRUD operations.
- Runs on: `https://localhost:7103`

---


## 🔧 Test API with CURL (Command Prompt)

> ❗ Use `--insecure` for `https://localhost` to bypass SSL verification.

### 📥 Get All Glossary Items
```bash
curl --insecure https://localhost:7103/api/glossary
```

### 📥 Get a Single Item (e.g., `MVC`)
```bash
curl --insecure https://localhost:7103/api/glossary/MVC
```

### ➕ Create a New Item
```bash
curl --insecure -X POST -d "{\"term\": \"MFA\", \"definition\":\"An authentication process.\"}" -H "Content-Type: application/json" https://localhost:7103/api/glossary
```

### 🔁 Update an Existing Item
```bash
curl --insecure -X PUT -d "{\"term\": \"MVC\", \"definition\":\"Modified record of Model View Controller.\"}" -H "Content-Type: application/json" https://localhost:7103/api/glossary/MVC
```

### ❌ Delete an Item (e.g., `OpenID`)
```bash
curl --insecure --request DELETE https://localhost:7103/api/glossary/OpenID
```

---

## 🧪 Test API with Postman

### Step 1: Disable SSL Verification
- Go to **Settings (⚙️)** → **General**
- Turn **SSL Certificate Verification** to **OFF**

### Step 2: Use These API Requests

#### 📥 Get All Items
- Method: `GET`  
- URL: `https://localhost:7103/api/glossary`

#### 📥 Get Single Item
- Method: `GET`  
- URL: `https://localhost:7103/api/glossary/MVC`

#### ➕ Create New Item
- Method: `POST`  
- URL: `https://localhost:7103/api/glossary`
- Headers: `Content-Type: application/json`
- Body (raw → JSON):
```json
{
  "term": "MFA",
  "definition": "An authentication process."
}
```

#### 🔁 Update Existing Item
- Method: `PUT`  
- URL: `https://localhost:7103/api/glossary`
- Headers: `Content-Type: application/json`
- Body (raw → JSON):
```json
{
  "term": "MVC",
  "definition": "Modified record of Model View Controller."
}
```

#### ❌ Delete Item
- Method: `DELETE`  
- URL: `https://localhost:7103/api/glossary/OpenID`

---

## ✅ You're Ready!

You can now manage glossary terms through **Postman** or **CURL** — your API is ready for action! 🎯