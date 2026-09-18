# 📚 Bookshelf RESTful API

[![Node.js](https://img.shields.io/badge/Node.js-18%2B-green?style=flat&logo=node.js)](https://nodejs.org/)
[![Hapi](https://img.shields.io/badge/@hapi/hapi-21.3-orange?style=flat&logo=hapi)](https://hapi.dev/)
[![ESLint](https://img.shields.io/badge/Code%20Style-Airbnb-red?style=flat&logo=eslint)](https://airbnb.io/javascript/)

A robust RESTful API service for managing digital bookshelf collections. Built using **Node.js** and the **@hapi/hapi** framework, strictly conforming to the **Airbnb JavaScript Style Guide**.

---

## ⚡ API Specification

The API conforms to standard HTTP verbs and status codes:

| Method | Endpoint | Description |
|---|---|---|
| `POST` | `/books` | Store a new book |
| `GET` | `/books` | Retrieve all books (supports `name`, `reading`, `finished` query filters) |
| `GET` | `/books/{bookId}` | Retrieve detail of a specific book |
| `PUT` | `/books/{bookId}` | Update an existing book's metadata |
| `DELETE` | `/books/{bookId}` | Remove a book from the collection |

### Validation Rules
- **Name Validation:** Rejects requests if `name` property is missing with `400 Bad Request`.
- **Page Logic:** Rejects creation/update if `readPage > pageCount` with `400 Bad Request`.
- **Automatic Status:** Automatically computes `finished: true` when `pageCount === readPage`.

---

## 🚀 Getting Started

### 1. Installation

```bash
git clone https://github.com/Akarptra/Bookshelf-api.git
cd Bookshelf-api
npm install
```

### 2. Linting & Validation

```bash
npm run lint
```

### 3. Run Server

```bash
npm start
# Server will run on http://localhost:9000
```

---

## 👤 Author

- **Raka Putra Pratidina** — [GitHub (@Akarptra)](https://github.com/Akarptra)
