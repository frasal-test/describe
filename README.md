### ✅ Updated `README.md`

```markdown
# Describe Monorepo

This repository serves as the umbrella project for **Describe**, combining:

- [`describe-client`](https://github.com/frasal-test/describe-client) — Frontend application built with **Gradio**
- [`describe-server`](https://github.com/frasal-test/describe-server) — Backend API server built with **Transformers** + **FastAPI**

Both client and server are included as **Git submodules** to keep their development clean and decoupled.

---

## 🗂️ Repository Structure

```

describe/
├── client/   # Frontend (submodule)
├── server/   # Backend  (submodule)
└── README.md # You're here

````

---

## 🧰 Prerequisites

- Git (with submodule support)
- Python 3.9+
- pip / virtualenv (for the server)
- [Gradio](https://gradio.app/) dependencies (see client README)
- Client can be a simple VM (I run a 1 OCPU - 16GB RAM - 50 GB HD on Oracle Cloud)
- Backend must be a GPU instance (I run an A10 - 100 GB HD on Oracle Cloud)
- Networking is up to you. Client and Backend must be able to communicate. Client must be visible from the internet.
- Files are stored in Oracle Cloud Storage. Authentication is up to you. I used Instance Principal Authentication.


---

## 🚀 Getting Started

### 1. Clone the monorepo **with submodules**

```bash
git clone --recurse-submodules https://github.com/frasal-test/describe.git
cd describe
````

If you've already cloned it without `--recurse-submodules`, run:

```bash
git submodule update --init --recursive
```

---

### 2. Setup and run each module separately

Refer to the `README.md` files inside each submodule for detailed instructions:

* [`client/README.md`](https://github.com/frasal-test/describe-client/blob/main/README.md)
* [`server/README.md`](https://github.com/frasal-test/describe-server/blob/main/README.md)

> Example default frontend URL: `http://<your-client-ip>:3000`

---

## 🔁 Keeping Submodules Updated

To fetch the latest commits from each submodule’s main branch:

```bash
git submodule update --remote
```

To commit the updated references:

```bash
git add client server
git commit -m "Update submodules"
git push
```

---

## 📝 License

MIT License — See individual repos for license details.

---

## 👤 Author

**Francesco Salerno**
[GitHub Profile](https://github.com/frasal-test)

