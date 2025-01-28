# Project Setup Instructions

This repository contains an integrated project with two submodules:
- **Frontend**: Built with Angular.
- **Backend**: Built with Django.

Follow the steps below to set up and run the project.

---

## Prerequisites

Ensure the following tools are installed on your system:

1. **Git**
   - Install from: https://git-scm.com/

2. **Node.js** (and npm)
   - Required for Angular.
   - Install from: https://nodejs.org/

3. **Python** (and pip)
   - Required for Django.
   - Install from: https://www.python.org/

4. **Angular CLI**
   - Install globally using npm:
     ```bash
     npm install -g @angular/cli
     ```

5. **Virtual Environment Tool (Optional)**
   - For Python virtual environments:
     ```bash
     pip install virtualenv
     ```

---

## Repository Setup

1. **Clone the Repository:**
   ```bash
   git clone --recurse-submodules https://github.com/tobni-islam/TP_IGL
   cd TP_IGL
   ```

   > Note: The `--recurse-submodules` flag ensures submodules are cloned along with the main repository.

2. **Initialize Submodules (If not cloned with submodules):**
   ```bash
   git submodule init
   git submodule update
   ```

---

## Backend Setup (Django)

1. Navigate to the `backend` directory:
   ```bash
   cd backend
   ```

2. Create and activate a Python virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```

3. Install backend dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Apply database migrations:
   ```bash
   python manage.py migrate
   ```

5. Run the backend server:
   ```bash
   python manage.py runserver
   ```

   The Django development server will start at `http://127.0.0.1:8000/`.

---

## Frontend Setup (Angular)

1. Navigate to the `frontend` directory:
   ```bash
   cd ../frontend
   ```

2. Install frontend dependencies:
   ```bash
   npm install
   ```

3. Run the Angular development server:
   ```bash
   ng serve
   ```

   The Angular development server will start at `http://localhost:4200/`.

---

## Access the Project

- **Frontend**: Open `http://localhost:4200/` in your browser.
- **Backend API**: Access the API at `http://127.0.0.1:8000/`.

---

## Additional Notes

### Synchronizing Submodules
If submodules are updated in the repository, run the following commands to sync them:
```bash
git submodule update --remote
```

### Environment Variables
- For the Django backend, ensure you set up any required environment variables (e.g., database credentials) in a `.env` file. Check `settings.py` for environment variable usage.
- For the Angular frontend, configure environment-specific settings in the `environment.ts` files.

---

