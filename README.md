
<img src="https://github.com/ariferol01/apidl/blob/main/logo.svg" alt="Açıklama" height="50">

---
# APIDL – API Directive Language & AI Prompt Integration Definition Language

**APIDL** is a lightweight, AI-native DSL (Domain Specific Language) for describing API workflows in a readable, prompt-friendly format. It allows AI models, backend systems, or automation layers to describe and execute multi-step API logic using a minimal and extensible syntax.

---

## ✨ What is APIDL?

APIDL is a declarative way to describe how APIs should be called, in what order, and how to handle the data between them. It removes the need for complex code, and provides a layer that can be interpreted by compilers or middleware in any language.

---

## 🧩 Example: Basic Flow

```apidl
SET userId = 123

GET https://api.example.com/users/{userId}
USE data.name TO username

HOOK cleanName FROM username TO final_name

HEADER Authorization = "Bearer {token}"

POST https://api.example.com/logs
BODY {"user": "{final_name}", "action": "login"}

````
---

## 🧪 Example: Chain API Requests

```apidl
GET https://api.example.com/users/123
USE data.username TO my_username

GET https://api.example.com/posts?author={my_username}
```
>Fetch user info, extract ```username```, and use it in a second request.

---

## 🔍 Syntax Overview

| **Keyword** | **Description** |
|-------------|-----------------|
| `SET`       | Define a variable (`SET id = 5`) |
| `GET`       | Perform a GET request |
| `POST`      | Perform a POST request |
| `PUT`       | Perform a PUT request |
| `DELETE`    | Perform a DELETE request |
| `USE`       | Extract data from a response (`USE data.key TO var`) |
| `BODY`      | Define a JSON request body |
| `HEADER`    | Add custom headers (`HEADER Authorization = "Bearer ..."`) |
| `HOOK`      | Call external function/provider for processing |

🔗 Full syntax: [SYNTAX.md](#)

---
## 🛠️ Compilers

| **Language**  | **Compiler Repo**         | **Status** |
|---------------|----------------------------|------------|
| PHP           | [apidl-php](#)             | WIP        |
| Python        | *(coming soon)*            | Planned    |
| JavaScript    | *(coming soon)*            | Planned    |
| Golang        | *(coming soon)*            | Planned    |
| Rust          | *(coming soon)*            | Planned    |
| C#            | *(coming soon)*            | Planned    |


Want to build one? See the [Compiler Guide](#)

---

## 💡 Use Cases

- AI agents executing dynamic, multi-step API tasks  
- Middleware for prompt-based API orchestration  
- Lightweight automation across services  
- Pluggable backend API layers  

---

## 🔐 Authentication Support

You can include bearer tokens using `HEADER`:

```apidl
HEADER Authorization = "Bearer {access_token}"
```
---
![AI PAXO](https://github.com/ariferol01/apidl/blob/main/ai-paxo-bottom-banner.jpg)
