# AgriGrow 🌱

AgriGrow is a comprehensive, AI-driven agricultural assistance platform designed to empower farmers and agricultural enthusiasts with data-driven insights. The system provides intelligent recommendations for crops, fertilizers, yield predictions, and plant disease detection, while also offering real-time weather forecasts and an interactive AI chatbot for personalized farming advice.

## System Architecture
The application is built on a modern microservices-inspired architecture comprising three main layers:

1. **Frontend**: A fast, responsive user interface built with React and Vite.
2. **Backend Gateway (Node.js/Express)**: An orchestration layer handling API routing, external API integration (Weather, Gemini), and file uploads.
3. **AI Service (Python/Flask)**: A dedicated machine learning microservice that serves predictive models using Scikit-Learn and TensorFlow.

## Core Features
* **Crop Recommendation**: Suggests the optimal crop to plant based on soil metrics (N, P, K, pH) and environmental factors (temperature, humidity, rainfall).
* **Fertilizer Recommendation**: Recommends the best fertilizer based on soil type, crop type, and nutrient levels.
* **Crop Yield Prediction**: Estimates agricultural yield (tonnes/hectare) using historical data, season, and area parameters.
* **Plant Disease Detection**: Image-based classification capable of detecting 38 different plant diseases across various species using a trained deep learning model.
* **AgriGrow AI Chatbot**: An intelligent conversational agent powered by Google's Gemini 2.5 Flash, providing expert agricultural advice.
* **Real-time Weather**: Integrates with the Visual Crossing API to provide accurate 24-hour weather forecasts based on the user's location.

## Tech Stack
### Frontend
* **React.js** (v19)
* **Vite** for fast build tooling
* **React Router DOM** for client-side routing
* **Axios** for API requests

### Backend (Node.js)
* **Node.js** & **Express.js**
* `@google/generative-ai` for Gemini Chatbot integration
* `multer` for handling image uploads
* `axios` for internal microservice communication

### AI Service (Python)
* **Flask** & **Flask-CORS**
* **TensorFlow** / **Keras** (Disease Detection)
* **Scikit-Learn** (Random Forest Models)
* **Pandas** & **NumPy** for data manipulation
* **Pillow** for image processing

## Getting Started

### Prerequisites
* Node.js (v18+)
* Python (3.9+)

### Installation

1. **Frontend Setup**
   ```bash
   cd frontend
   npm install
   npm run dev
   ```

2. **Backend Setup**
   ```bash
   cd backend
   npm install
   # Create a .env file and add GEMINI_API_KEY and WEATHER_API_KEY
   node server.js
   ```

3. **AI Service Setup**
   ```bash
   cd ai-service
   pip install -r requirements.txt
   python app.py
   ```

## External APIs Used
- **Google Gemini API**: For the intelligent agricultural chatbot.
- **Visual Crossing Weather API**: For real-time, location-based weather forecasting.
- **Hugging Face Spaces**: Hosting platform for the Python AI Service.
