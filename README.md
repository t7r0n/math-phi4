
# Tutor AI 

This project is a full-stack chatbot application powered by **FastAPI** for the backend and **React + TypeScript** for the frontend. The chatbot uses a **fine-tuned Qwen2.5-3B-Instruct** model to generate responses.

## 📂 Project Structure

- `/frontend`   # React + TypeScript (User Interface)
- `/backend`    # FastAPI + SQLite (API and ML Inference)

---

## 🚀 Getting Started

### 1️⃣ Prerequisites

Ensure you have the following installed:

- **Node.js** (Recommended: `>=18.x`)
- **Yarn** (`npm install -g yarn`)
- **Python 3.12**
- **Virtual Environment (venv)**
- **SQLite** (comes bundled with Python)
- **CUDA** (for GPU acceleration, optional)
- **Unsloth** (Fine Tuning)

---
Download the saved LoRA Weights from GDRIVE -
https://drive.google.com/file/d/1j4ex9NN1GxO9vnAHAJ_gtqgodO6HuBtB/view?usp=sharing

Video Link to see the project in action -
https://drive.google.com/file/d/1u1crR5D5IuxLSjk0TrCCPvbiexRfYPeZ/view?usp=sharing

For Environment details please go through the 'environment.yml' file.
Main Libraries used are -

- Unsloth
- Pytorch

---

---

## 🔧 Backend Setup (FastAPI + SQLite)

1. Navigate to the backend folder:

   ```bash
   cd backend
   ```

2. Create a virtual environment:

   ```bash
   python3 -m venv venv
   source venv/bin/activate  # MacOS/Linux
   venv\Scriptsctivate     # Windows
   ```

3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

5. Start the FastAPI server:

   ```bash
   uvicorn app.main:app
   ```

6. Open Swagger Docs:
   - API Docs: [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)

---

## 🌐 Frontend Setup (React + TypeScript)

1. Navigate to the frontend folder:

   ```bash
   cd ../frontend
   ```

2. Install dependencies:

   ```bash
   yarn install
   ```

3. Start the development server:

   ```bash
   yarn start
   ```

4. Open the browser and go to:
   - [http://localhost:3000](http://localhost:3000)

---

## 📡 API Endpoints

### User Authentication

| Method | Endpoint        | Description                          |
|--------|-----------------|--------------------------------------|
| POST   | `/users/signup` | Register a new user                 |
| POST   | `/users/login`  | Authenticate and receive a token    |
| GET    | `/users/me`     | Fetch logged-in user details        |

### Chat API

| Method | Endpoint           | Description                            |
|--------|--------------------|----------------------------------------|
| POST   | `/chats/`          | Ask a question, receive AI-generated response |
| GET    | `/chats/history`   | Fetch last 15 questions & answers     |

---

## 🛠 Deployment

### Backend (FastAPI)

- Use Gunicorn or Uvicorn for production:

   ```bash
   uvicorn app.main:app --host 0.0.0.0 --port 8000
   ```

- Deploy via Docker, AWS Lambda, or GCP Cloud Run.

### Frontend (React)

- Build for production:

   ```bash
   yarn build
   ```

- Deploy to Vercel, Netlify, or GitHub Pages.

- Sample Sceenshots:

  Sign Up Page -
  ![Screenshot from 2025-03-24 15-24-58](https://github.com/user-attachments/assets/d46c6887-48ed-4fb7-bd8c-3fb15bae45d7)


  ![Screenshot from 2025-03-24 15-24-46](https://github.com/user-attachments/assets/9d8ed472-73bb-4703-ae8c-925709210f85)


  Sign In Page
  ![Screenshot from 2025-03-24 15-21-42](https://github.com/user-attachments/assets/e6f12486-2dfd-495e-a914-80cf3df7e144)


  Chat Window
  ![Screenshot from 2025-03-24 15-22-00](https://github.com/user-attachments/assets/88c6ae76-9249-4682-94a9-2b5e7a0432b6)


---

## 🏗 Future Improvements

- OAuth authentication (Google, GitHub)
- Persistent chat history with PostgreSQL
- Streaming AI responses
- Frontend UI enhancements
