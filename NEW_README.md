# 🎯 AI Interview Integrity & Candidate Analytics Platform

An enterprise-grade interview monitoring system designed to ensure fair, secure, and trustworthy online assessments. The platform combines Computer Vision, AI-powered behavioral analytics, and real-time monitoring to detect suspicious activities, assess candidate engagement, and generate detailed interview reports.

---

## ✨ Key Features

### 🔍 Real-Time Face Tracking
- High-accuracy face detection using MediaPipe
- Continuous facial landmark tracking
- Multi-face detection alerts

### 👁️ Liveness Verification
- Eye Aspect Ratio (EAR) blink detection
- Head pose estimation
- Anti-photo and anti-video replay checks

### 🛡️ Spoof Detection
- Texture-based analysis (LBP)
- Frequency-domain analysis (FFT)
- Optional deep learning CNN model for advanced spoof classification

### 📊 Behavioral Intelligence
- Gaze tracking and screen-attention analysis
- Candidate engagement scoring
- Distraction and inactivity monitoring

### 🚨 Smart Alert System
- Off-screen gaze detection
- Multiple-person detection
- Potential spoofing attempts
- Suspicious behavior notifications

### 📑 Automated Reporting
- Session summaries
- Behavioral insights
- Attention score trends
- Security event logs

---

## 🏗️ System Architecture

```text
Candidate Webcam
        │
        ▼
 WebSocket Stream
        │
        ▼
 AI Processing Pipeline
 ├── Face Detection
 ├── Landmark Extraction
 ├── Liveness Detection
 ├── Spoof Detection
 ├── Behavior Analysis
 └── Alert Engine
        │
        ▼
 FastAPI Backend
        │
        ▼
 React Dashboard & Reports
```

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone <your-repository-url>
cd project-folder
```

### 2. Backend Setup

```bash
python -m venv .venv
```

Activate virtual environment:

**Windows**
```powershell
.venv\Scripts\activate
```

**Linux / macOS**
```bash
source .venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Start backend:

```bash
uvicorn backend.main:app --reload --port 8000
```

---

### 3. Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

---

## 🌐 Application Endpoints

| Service | URL |
|----------|-----|
| Frontend | http://localhost:5173 |
| Backend API | http://localhost:8000 |
| Swagger Docs | http://localhost:8000/docs |

---

## 📂 Project Structure

```text
backend/
├── pipeline/
│   ├── detector.py
│   ├── landmarks.py
│   ├── liveness.py
│   ├── spoof.py
│   ├── behavior.py
│   └── alerts.py
│
├── routers/
├── models/
├── utils/
└── main.py

frontend/
├── pages/
├── components/
└── hooks/

training/
├── preprocess.py
└── train_spoof.py
```

---

## 🤖 AI Models & Techniques

| Component | Method |
|------------|---------|
| Face Detection | MediaPipe |
| Landmark Detection | Face Mesh (468 Points) |
| Blink Detection | EAR Algorithm |
| Head Pose | PnP Estimation |
| Spoof Detection | LBP + FFT + CNN |
| Attention Analysis | Gaze Tracking |
| Reporting | Rule-Based Analytics |

---

## ⚙️ Configuration

Modify thresholds inside:

```python
backend/config.py
```

Common parameters:

- `EAR_THRESHOLD`
- `HEAD_POSE_YAW_LIMIT`
- `SPOOF_CONFIDENCE_THRESHOLD`
- `GAZE_OFF_SCREEN_SECONDS`
- `ATTENTION_SCORE_LIMIT`

---

## 🧠 Training a Custom Spoof Detection Model

### Dataset Suggestions
- CelebA-Spoof
- Replay-Attack
- NUAA Photograph Dataset

### Data Preprocessing

```bash
python training/preprocess.py --src <dataset_path> --dst training/data
```

### Training

```bash
python training/train_spoof.py --data training/data --epochs 20
```

Trained models are automatically loaded during backend startup.

---

## 🛠️ Tech Stack

| Category | Technology |
|-----------|------------|
| Backend | FastAPI, Python |
| Frontend | React, Vite |
| Database | SQLite, SQLAlchemy |
| Computer Vision | OpenCV, MediaPipe |
| Machine Learning | TensorFlow |
| Communication | WebSockets |
| Deployment | Docker, NGINX |

---

## 📈 Future Enhancements

- Voice emotion analysis
- Lip-sync verification
- Identity verification using Face Recognition
- AI-generated interview summaries
- Risk scoring dashboard
- Cloud deployment with Kubernetes

---

## 📄 License

This project is intended for educational, research, and assessment-monitoring purposes. Customize the license section according to your organization's requirements.

---

## 👨‍💻 Developed For

Secure online interviews, remote hiring assessments, proctored examinations, and AI-assisted candidate evaluation systems.
