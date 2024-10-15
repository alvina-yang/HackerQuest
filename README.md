
# HackerQuest

HackerQuest is an AI-powered interview interface with a pair programming feature and a live behavioral question format. It allows technical and behavioral interviews to be conducted via a responsive web interface, leveraging AI to assess code, provide feedback, and manage interviews.

## Features

- **Code Interview Interface**: A pair programming environment with support for dynamic questions and live code review.
- **Behavioral Interview Interface**: A behavioral interview interface with real-time audio visualizers.
- **AI Feedback**: Automated feedback for code reviews and behavioral interviews, including grading across key performance metrics.
- **Backend Services**: APIs to handle behavioral and technical questions, along with PDF document analysis for interview documentation.
  
## Repository Structure

The project is organized into several subdirectories, each containing important components of the system:

- `EmotionAI`: Handles emotion detection for interviews.
- `backend`: Contains the core backend server (Flask-based), which provides APIs for fetching coding problems and evaluating code and behavioral interviews.
- `bot`: AI chatbot-related code and configurations for integration.
- `frontend`: React-based frontend that contains the behavioral and code interview interfaces.

## How to Run Locally

### Prerequisites

1. **Python 3.x** and **Node.js** installed on your machine.
2. Install **Docker** if using containerized deployment.

### Backend Setup (Flask API)

1. Clone the repository:
   ```bash
   git clone https://github.com/alvina-yang/HackerQuest.git
   cd HackerQuest
   ```

2. Navigate to the backend directory:
   ```bash
   cd backend
   ```

3. Install the required Python packages:
   ```bash
   pip install -r requirements.txt
   ```

4. Set up environment variables: Create a `.env` file in the backend directory and add your API keys (such as for Cohere AI).

5. Run the Flask server:
   ```bash
   python app.py
   ```

   The backend will be available at `http://localhost:5678`.

### Frontend Setup

1. Navigate to the frontend directory:
   ```bash
   cd frontend
   ```

2. Install the dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm run dev
   ```

   The frontend will be available at `http://localhost:3000`.

## Running the AI-Powered Interview Interfaces

- **Behavioral Interview**: Open `http://localhost:3000/behavioural-interview` to start a behavioral interview session.
- **Code Interview**: Open `http://localhost:3000/code-interview` to begin a live coding session.

## API Endpoints

The backend provides several API endpoints:

- `/api/review_code`: Submits code for review during technical interviews.
- `/api/evaluate_behavioral`: Evaluates performance during behavioral interviews.
- `/api/upload_pdf`: Uploads a PDF document for analysis.
- `/api/find_lc_question`: Finds a coding problem by querying a LeetCode-style database.

