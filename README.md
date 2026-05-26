# 🌾 AI Farm Intelligence System

An AI-powered agricultural decision support system that leverages machine learning to help farmers make data-driven decisions for improved crop yields and farm management.

## 🎯 Features

- **🌱 Crop Recommendation**: Get intelligent crop suggestions based on soil conditions, climate, and historical data
- **📊 Yield Prediction**: Predict crop yields to optimize planning and resource allocation
- **🔍 Disease Detection**: AI-powered plant disease detection using image recognition
- **🌦️ Weather Advisory**: Real-time weather insights and agricultural recommendations
- **🧠 Explainable AI**: Understand model predictions with detailed explanations and visualizations

## 🏗️ Architecture

The system is built with a modern full-stack approach:

```
AI-Farm-Intelligence-System/
├── frontend/                 # React + Vite + Tailwind CSS
│   ├── src/
│   │   ├── pages/           # Page components (Dashboard, Crop, Yield, Disease, Weather, etc.)
│   │   ├── styles/          # CSS styling with Tailwind
│   │   └── App.jsx          # Main application component
│   └── package.json
├── backend/                  # Python FastAPI server
│   ├── main.py              # FastAPI application entry point
│   ├── routes/              # API route handlers
│   │   ├── crop.py
│   │   ├── yield_pred.py
│   │   ├── disease.py
│   │   ├── weather.py
│   │   └── explain.py
│   ├── models/              # ML model files
│   └── requirements.txt      # Python dependencies
```

## 🛠️ Tech Stack

### Frontend (67.4% JavaScript)
- **React** 18.3 - UI library
- **Vite** - Fast build tool with Tailwind CSS
- **Tailwind CSS** 3.4 - Utility-first CSS framework
- **React Router** 6.23 - Client-side routing
- **Framer Motion** 12.38 - Animation library
- **Chart.js & Plotly.js** - Data visualization
- **Lucide React** - Icon library
- **Axios** - HTTP client

### Backend (30.1% Python)
- **FastAPI** - Modern Python web framework
- **PyTorch** & **TorchVision** - Deep learning for disease detection
- **Scikit-learn** - Machine learning algorithms
- **Pandas & NumPy** - Data processing
- **SHAP** - Model explainability
- **HTTPx** - Weather API integration

### Other (2.5%)
- CSS styling and configuration files

## 🚀 Getting Started

### Prerequisites
- Node.js 14+ and npm/yarn
- Python 3.8+
- pip (Python package manager)

### Frontend Setup

```bash
cd ai-farm-intelligence-system-main/frontend

# Install dependencies
npm install

# Start development server (runs on http://localhost:3000)
npm start

# Build for production
npm build
```

The frontend is configured to proxy API requests to `http://localhost:8000` during development.

### Backend Setup

```bash
cd ai-farm-intelligence-system-main/backend

# Create virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Start the server (runs on http://localhost:8000)
python main.py
```

**Note**: Models are preloaded at startup for faster first request performance.

### Environment Variables

Create a `.env` file in the backend directory:

```env
FRONTEND_URL=http://localhost:3000
```

For production deployments, update `FRONTEND_URL` to your deployed frontend URL.

## 📡 API Endpoints

The backend provides comprehensive RESTful APIs:

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/api/crop` | POST | Get crop recommendations |
| `/api/yield` | POST | Predict crop yield |
| `/api/disease` | POST | Detect plant diseases from images |
| `/api/weather` | GET | Get weather advisory |
| `/api/explain` | POST | Get model prediction explanations |
| `/health` | GET | Health check endpoint |
| `/docs` | GET | Interactive API documentation (Swagger) |

Full API documentation available at `http://localhost:8000/docs` when the backend is running.

## 🎨 Frontend Pages

- **Dashboard** - Overview of all system capabilities
- **Crop Recommendation** - Input soil and climate data for crop suggestions
- **Yield Prediction** - Predict yields based on farm parameters
- **Disease Detection** - Upload plant images for disease identification
- **Weather Advisory** - View weather insights and recommendations
- **Explain AI** - Understand model decisions with visualizations

## 🤖 Machine Learning Models

### Crop Recommendation
- Multi-class classification model trained on agricultural datasets
- Considers: N, P, K ratios, temperature, humidity, pH, rainfall

### Yield Prediction
- Regression model for predicting crop production
- Features: fertilizer usage, pesticide usage, temperature, humidity, rainfall

### Disease Detection
- Deep learning model (PyTorch) for plant disease classification
- Processes plant leaf images to identify diseases

### Model Explainability
- SHAP (SHapley Additive exPlanations) integration
- Feature importance analysis with visualizations
- Decision explanations for each prediction

## 🌐 Deployment

### Frontend (Vercel)
The frontend is configured for deployment on Vercel:
```
https://ai-farm-frontend.vercel.app
```

### Backend (FastAPI)
The backend can be deployed on:
- Heroku
- Railway
- DigitalOcean
- AWS (EC2, Lambda with API Gateway)
- Google Cloud Run

**CORS Configuration**: The backend accepts requests from:
- Local development: `http://localhost:3000`, `http://localhost:3001`
- Production: Configured via `FRONTEND_URL` environment variable
- Vercel preview deployments: All URLs matching `*.vercel.app`

## 📊 Language Composition

- **JavaScript**: 67.4% (Frontend with React)
- **Python**: 30.1% (Backend with FastAPI & ML models)
- **CSS**: 2.2% (Styling with Tailwind)
- **Other**: 0.3%

## 🔒 CORS & Security

CORS is configured to allow:
- Development environments (localhost on multiple ports)
- Production deployments via environment variable
- Vercel preview URLs (for preview deployments)

## 📝 License

This project is open source and available under the MIT License.

## 👨‍💻 Author

**Neeraj-NP**

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📧 Support

For issues or questions, please create an issue on the GitHub repository.

---

**Built with ❤️ for farmers and agricultural professionals**
