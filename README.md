# T-Flow AI Medical Triage System

[![API Status](https://img.shields.io/badge/API-Live-brightgreen)](https://tflow-medical-triage.onrender.com/docs)
[![Frontend Demo](https://img.shields.io/badge/Frontend-Live-blue)](https://vercel.com/iyad07s-projects/v0-t-flow-ai-frontend)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Next.js](https://img.shields.io/badge/Next.js-15.2.4-black)](https://nextjs.org)
[![Python](https://img.shields.io/badge/Python-3.12+-blue.svg)](https://python.org)

## 🏥 Project Overview

T-Flow is a comprehensive AI-powered medical triage system that revolutionizes patient assessment and prioritization in healthcare facilities. The system combines cutting-edge artificial intelligence with traditional rule-based medicine to provide accurate, fast, and reliable patient triage assessments.

**🌟 Key Innovation**: Integration of Groq's Llama 3.3 70B model with comprehensive vital signs monitoring and real-time patient management dashboard.

### 🎯 Problem Statement
Healthcare facilities face challenges in:
- Efficiently triaging patients based on symptom severity
- Managing patient flow and wait times
- Ensuring consistent assessment quality
- Integrating vital signs with symptom analysis
- Providing real-time visibility into patient status

### 💡 Solution
T-Flow addresses these challenges through:
- **AI-Powered Analysis**: Advanced language model for intelligent symptom interpretation
- **Integrated Vital Signs**: Automated flagging of abnormal vital signs with age-adjusted thresholds
- **Real-Time Dashboard**: Comprehensive patient management and analytics
- **Hybrid Approach**: AI with rule-based fallback ensuring 100% system availability
- **Production-Ready**: Hospital-grade security and reliability

## ✨ Key Features

### 🤖 AI-Powered Medical Triage
- **Groq Llama 3.3 70B Integration**: State-of-the-art language model for medical analysis
- **Intelligent Symptom Analysis**: Processes complex medical descriptions with high accuracy
- **Safety-First Design**: "When in doubt, escalate" principle built into AI logic
- **Fallback System**: Rule-based triage ensures continuous operation

### 💓 Comprehensive Vital Signs Monitoring
- **Multi-Parameter Analysis**: Pulse, systolic BP, diastolic BP with intelligent flagging
- **Age-Adjusted Thresholds**: Personalized normal ranges based on patient demographics
- **Real-Time Alerts**: Immediate flagging of abnormal vital signs
- **Integrated Assessment**: Combined symptom and vitals analysis for holistic evaluation

### 📊 Advanced Dashboard & Analytics
- **Real-Time Statistics**: Live patient counts, triage distribution, system metrics
- **Patient Queue Management**: Dynamic patient tracking with priority indicators
- **Performance Monitoring**: Wait times, processing rates, capacity utilization
- **Visual Analytics**: Interactive charts and trend analysis

### 🏥 Patient Management System
- **Comprehensive Patient Profiles**: Complete medical assessment history
- **Status Tracking**: Real-time updates with full audit trails
- **Priority Management**: Color-coded triage levels (Critical, Urgent, Moderate, Low)
- **Change History**: Detailed timeline of all patient interactions

### 🔒 Enterprise-Grade Security
- **Data Validation**: Comprehensive input sanitization and PII protection
- **Secure API**: RESTful architecture with proper error handling
- **Audit Trails**: Complete logging of all system interactions
- **HIPAA Considerations**: Privacy-focused design patterns

## 🏗️ System Architecture

```
┌─────────────────────┐    ┌─────────────────────┐    ┌─────────────────────┐
│   Next.js Frontend  │    │   FastAPI Backend   │    │   Groq AI Engine   │
│   - Dashboard       │◄──►│   - Triage Logic    │◄──►│   - Llama 3.3 70B   │
│   - Patient Mgmt    │    │   - Vitals Analysis │    │   - Medical Prompts │
│   - Real-time UI    │    │   - Data Validation │    │   - Fallback Rules  │
└─────────────────────┘    └─────────────────────┘    └─────────────────────┘
                                      │
                                      ▼
                              ┌─────────────────────┐
                              │   Supabase DB       │
                              │   - Patient Records │
                              │   - Triage History  │
                              │   - Vital Signs     │
                              └─────────────────────┘
```

## 🛠️ Technology Stack

### Frontend (Next.js)
- **Framework**: Next.js 15.2.4 with App Router
- **Language**: TypeScript
- **Styling**: Tailwind CSS
- **UI Components**: Shadcn/ui, Radix UI
- **Charts**: Recharts for data visualization
- **State Management**: React Hooks
- **HTTP Client**: Axios

### Backend (Python)
- **Framework**: FastAPI
- **AI Integration**: Groq API (Llama 3.3 70B)
- **Database**: Supabase PostgreSQL
- **Validation**: Pydantic models
- **Deployment**: Render.com

### Database & Infrastructure
- **Database**: PostgreSQL (Supabase)
- **Hosting**: Vercel (Frontend), Render (Backend)
- **API Documentation**: Automatic OpenAPI/Swagger

## 📁 Project Structure

```
t-flow/
├── 📁 frontend/                    # Next.js Frontend Application
│   ├── 📁 app/                    # Next.js App Router
│   │   ├── globals.css           # Global styles
│   │   ├── layout.tsx            # Root layout
│   │   └── page.tsx              # Main dashboard
│   ├── 📁 components/            # React Components
│   │   ├── 📁 auth/              # Authentication components
│   │   ├── 📁 dashboard/         # Dashboard components
│   │   ├── 📁 triage/            # Triage form components
│   │   ├── 📁 ui/                # Reusable UI components
│   │   ├── 📁 vitals/            # Vital signs components
│   │   ├── SimpleTriageForm.tsx  # Basic triage form
│   │   └── UnifiedTriageForm.tsx # Advanced triage form
│   ├── 📁 hooks/                 # Custom React hooks
│   ├── 📁 lib/                   # Utilities and API client
│   ├── 📁 types/                 # TypeScript definitions
│   └── 📁 public/                # Static assets
│
├── 📁 backend-and-ai-integrations/ # Python Backend
│   ├── 📁 ai/                    # AI Engine
│   │   ├── triage.py             # Core AI triage logic
│   │   └── test.py               # AI system tests
│   ├── 📁 backend/               # FastAPI Application
│   │   ├── main.py               # API entry point
│   │   ├── triage_core.py        # Core triage functions
│   │   └── system_check.py       # Health monitoring
│   ├── 📁 Frontend Integration Docs/
│   │   ├── NEXTJS_INTEGRATION.md
│   │   ├── NEXTJS_QUICK_START.md
│   │   └── RECENT_ENDPOINT_FIX.md
│   ├── requirements.txt          # Python dependencies
│   ├── render.yaml              # Deployment config
│   └── supabase_setup.sql       # Database schema
│
└── 📁 Demo/                      # Demo Materials (see below)
    ├── screenshots/              # Application screenshots
    ├── demo-video-link.md       # Link to demo video
    └── user-guide.md            # Usage instructions
```

## 🚀 Getting Started

### Prerequisites
- **Node.js** 18+ and npm/yarn
- **Python** 3.12+
- **Groq API Key** (free tier available)
- **Supabase Account** (free tier available)

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/t-flow.git
cd t-flow
```

### 2. Backend Setup
```bash
cd backend-and-ai-integrations
pip install -r requirements.txt

# Create .env file
echo "GROQ_API_KEY=your_groq_api_key" > .env
echo "SUPABASE_URL=your_supabase_url" >> .env
echo "SUPABASE_ANON_KEY=your_supabase_key" >> .env

# Setup database
# Run supabase_setup.sql in your Supabase dashboard

# Start backend server
cd backend
python main.py
```

### 3. Frontend Setup
```bash
cd frontend
npm install

# Create .env.local file
echo "NEXT_PUBLIC_API_URL=http://localhost:8000" > .env.local

# Start development server
npm run dev
```

### 4. Access the Application
- **Frontend**: http://localhost:3000
- **Backend API**: http://localhost:8000
- **API Documentation**: http://localhost:8000/docs

## 🎯 How It Works

### 1. Patient Assessment Flow
1. **Symptom Input**: Healthcare provider enters patient symptoms and basic information
2. **Vital Signs**: Optional vital signs input (pulse, blood pressure)
3. **AI Analysis**: Groq Llama 3.3 70B processes symptoms with medical context
4. **Vitals Flagging**: Automated analysis of vital signs with age-adjusted thresholds
5. **Triage Classification**: Combined assessment produces final triage level
6. **Dashboard Update**: Real-time update of patient queue and statistics

### 2. Triage Levels
- **🔴 Critical**: Life-threatening conditions requiring immediate intervention
- **🟠 Urgent**: Serious conditions requiring attention within 2-4 hours
- **🟡 Moderate**: Conditions requiring evaluation within 24-48 hours
- **🟢 Low**: Minor conditions suitable for routine care

### 3. AI Safety Features
- **Medical-Grade Prompting**: Specialized prompts for medical scenarios
- **Conservative Bias**: System errs on the side of higher acuity when uncertain
- **Fallback System**: Rule-based triage activates if AI is unavailable
- **Input Validation**: Comprehensive sanitization and PII protection

## 📊 API Endpoints

### Primary Triage Endpoint
```bash
POST /api/triage
```
**Request:**
```json
{
  "symptoms": "Patient has chest pain and difficulty breathing",
  "patient_info": {"age": 45, "gender": "M"},
  "vitals": {
    "pulse": 120,
    "systolicBP": 180,
    "diastolicBP": 95
  },
  "use_ai": true
}
```

**Response:**
```json
{
  "triage_level": "Critical",
  "record_id": "uuid-here",
  "timestamp": "2025-01-10T12:00:00Z",
  "vitals_flags": {
    "pulse_flag": true,
    "systolic_flag": true,
    "any_flag": true
  }
}
```

### Recent Assessments
```bash
GET /api/triage/recent?limit=10
```

### Health Check
```bash
GET /api/health
```

## 🎬 Demo Materials

The `Demo/` folder contains comprehensive demonstration materials:

### 📸 Screenshots
- **Dashboard Overview**: Main application interface
- **Triage Assessment**: Step-by-step patient evaluation
- **Patient Management**: Queue and status tracking
- **Analytics Dashboard**: Real-time statistics and charts
- **Mobile Responsive**: Cross-device compatibility

### 🎥 Demo Video
A comprehensive walkthrough video demonstrating:
- Complete patient triage workflow
- AI-powered symptom analysis
- Vital signs monitoring and flagging
- Dashboard analytics and patient management
- System reliability and error handling

**Video Link**: [T-Flow AI Demo Video](Demo/demo-video-link.md)

### 📋 User Guide
Detailed instructions for:
- System navigation
- Patient assessment procedures
- Dashboard interpretation
- Troubleshooting common issues

## 🔬 Testing & Validation

### Automated Testing
```bash
# Backend tests
cd backend-and-ai-integrations/ai
python test.py

# Frontend tests
cd frontend
npm test
```

### Manual Testing Scenarios
- **Critical Cases**: Chest pain, difficulty breathing, severe trauma
- **Urgent Cases**: High fever, severe pain, moderate injuries
- **Moderate Cases**: Persistent symptoms, minor injuries
- **Low Priority**: Routine check-ups, minor complaints

## 🚀 Deployment

### Production Deployment
- **Frontend**: Deployed on Vercel with automatic CI/CD
- **Backend**: Deployed on Render.com with health monitoring
- **Database**: Supabase PostgreSQL with automated backups

### Live Instances
- **Frontend Demo**: https://vercel.com/iyad07s-projects/v0-t-flow-ai-frontend
- **Backend API**: https://tflow-medical-triage.onrender.com
- **API Documentation**: https://tflow-medical-triage.onrender.com/docs

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support & Contact

For questions, issues, or contributions:
- **GitHub Issues**: Create an issue for bug reports or feature requests
- **Documentation**: Check the `/docs` folder for detailed guides
- **API Documentation**: Visit the live API docs for endpoint details

## 🏆 Project Highlights

### Innovation
- **First-of-its-kind** integration of Groq Llama 3.3 70B for medical triage
- **Hybrid AI approach** ensuring 100% system availability
- **Real-time analytics** with comprehensive patient management

### Technical Excellence
- **Production-ready** architecture with proper error handling
- **Responsive design** optimized for healthcare environments
- **Comprehensive testing** with automated validation
- **Security-first** approach with data protection

### Impact
- **Improved Patient Outcomes**: Faster, more accurate triage decisions
- **Enhanced Efficiency**: Streamlined workflow for healthcare providers
- **Data-Driven Insights**: Analytics for continuous improvement
- **Scalable Solution**: Designed for healthcare facilities of all sizes

---

**Built with ❤️ for healthcare professionals worldwide**

*T-Flow AI - Revolutionizing Medical Triage Through Artificial Intelligence*