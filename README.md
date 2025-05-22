# Vue.js + Flask Application

A web application with Vue.js frontend and Flask backend.

## Project Structure
- `client/`: Vue.js frontend
- `server/`: Flask backend

## Setup Instructions

### Backend (Flask)
1. Navigate to the server directory:
   ```
   cd server
   ```

2. Create a virtual environment:
   ```
   python -m venv venv
   ```

3. Activate the virtual environment:
   - Windows:
     ```
     .\venv\Scripts\activate
     ```
   - macOS/Linux:
     ```
     source venv/bin/activate
     ```

4. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

5. Run the Flask server:
   ```
   python app.py
   ```
   The server will start at http://localhost:5000

### Frontend (Vue.js)
1. Navigate to the client directory:
   ```
   cd client
   ```

2. Install dependencies:
   ```
   npm install
   ```

3. Run the development server:
   ```
   npm run dev
   ```
   The application will be available at http://localhost:5173

## API Endpoints
- `GET /api/hello`: Returns a greeting message from the Flask backend

## Features
- Modern Vue 3 with Composition API and TypeScript
- Flask backend with CORS enabled
- Real-time communication between frontend and backend 