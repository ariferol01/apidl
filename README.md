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
