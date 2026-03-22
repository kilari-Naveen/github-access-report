# GitHub Access Report Service

## 📌 Overview
This project retrieves repository access details from a GitHub organization and generates a report mapping users to repositories.

---

## 🚀 How to Run

1. Clone repository
2. Add your GitHub token in `application.properties`
3. Run:
   mvn spring-boot:run

---

## 🔐 Authentication
Uses GitHub Personal Access Token (PAT)

Steps:
- Go to GitHub → Settings → Developer Settings → Tokens
- Generate token with repo access
- Add in application.properties

---

## 📡 API Endpoint

GET:
http://localhost:8080/api/access-report

---

## ⚙️ Design Decisions

- Used WebClient (non-blocking HTTP)
- Aggregated user → repo mapping
- Simple HashMap for fast lookup
- Handles 100+ repos efficiently

---

## ⚠️ Assumptions

- Token has access to organization repos
- Organization name is valid
- API rate limits are handled externally

---

## 📈 Scalability

- Can be optimized using parallel API calls
- Supports large orgs (100+ repos, 1000+ users)

---

## ✅ Features

✔ GitHub API Integration  
✔ Secure Authentication  
✔ Aggregated Report  
✔ REST API Output  
✔ Clean Architecture  