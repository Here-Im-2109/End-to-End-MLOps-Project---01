# 🚗 End-to-End MLOps Vehicle Insurance Prediction

An End-to-End MLOps project built using **Python, MongoDB, Scikit-Learn, AWS S3, Docker, GitHub Actions, and EC2**.

The project demonstrates a complete Machine Learning production pipeline starting from data ingestion to model deployment with CI/CD automation.

---

# 📌 Project Architecture

```
Data Source (MongoDB)
        │
        ▼
Data Ingestion
        │
        ▼
Data Validation
        │
        ▼
Data Transformation
        │
        ▼
Model Trainer
        │
        ▼
Model Evaluation
        │
        ▼
Model Pusher (AWS S3)
        │
        ▼
Prediction Pipeline
        │
        ▼
Flask Web Application
        │
        ▼
Docker + GitHub Actions + EC2 Deployment
```

---

# 📂 Project Structure

```
.
│
├── .github/workflows/
│      └── aws.yaml
│
├── artifact/
├── config/
│      ├── model.yaml
│      └── schema.yaml
│
├── logs/
│
├── notebook/
│      ├── data.csv
│      ├── EDA.ipynb
│      └── mongoDB_demo.ipynb
│
├── src/
│      ├── cloud_storage/
│      ├── components/
│      ├── configuration/
│      ├── constants/
│      ├── data_access/
│      ├── entity/
│      ├── exception/
│      ├── logger/
│      ├── pipeline/
│      └── utils/
│
├── static/
├── templates/
│
├── app.py
├── demo.py
├── Dockerfile
├── requirements.txt
├── setup.py
├── pyproject.toml
└── README.md
```

---

# 🚀 Features

- End-to-End ML Pipeline
- MongoDB Atlas Integration
- Data Validation
- Feature Engineering
- Model Training
- Model Evaluation
- AWS S3 Model Registry
- Flask Web Application
- Docker Support
- GitHub Actions CI/CD
- EC2 Deployment
- Logging & Exception Handling
- Modular Project Structure

---

# 🛠 Tech Stack

- Python 3.10
- Pandas
- NumPy
- Scikit-Learn
- MongoDB Atlas
- Flask
- AWS S3
- Docker
- GitHub Actions
- EC2
- YAML
- Joblib

---

# ⚙️ Installation

## Clone Repository

```bash
git clone https://github.com/Here-Im-2109/End-to-End-MLOps-Project---01.git

cd End-to-End-MLOps-Project---01
```

---

## Create Virtual Environment

Using Conda

```bash
conda create -p mlops python=3.10 -y
```

Activate Environment

### Windows

```bash
conda activate mlops
```

### Linux / Mac

```bash
conda activate ./mlops
```

---

## Install Dependencies

```bash
pip install -r requirements.txt
```

Verify Installation

```bash
pip list
```

---

# 📦 Local Package Installation

This project uses local packages.

Generate project template

```bash
python template.py
```

Install package

```bash
pip install -e .
```

---

# 🍃 MongoDB Setup

## Step 1

Create a MongoDB Atlas account.

Create a new project.

---

## Step 2

Create an M0 Free Cluster.

---

## Step 3

Create Database User.

---

## Step 4

Allow Network Access

```
0.0.0.0/0
```

---

## Step 5

Copy Python Connection String

```
mongodb+srv://username:password@cluster.mongodb.net
```

Replace

```
<username>
<password>
```

with your credentials.

---

## Step 6

Set Environment Variable

### Windows (PowerShell)

```powershell
$env:MONGODB_URL="mongodb+srv://..."
```

### Linux / Mac

```bash
export MONGODB_URL="mongodb+srv://..."
```

Verify

```bash
echo $MONGODB_URL
```

---

# 📊 Upload Dataset to MongoDB

Run

```bash
notebook/mongoDB_demo.ipynb
```

The notebook uploads the dataset into MongoDB Atlas.

---

# ▶️ Run Training Pipeline

```bash
python demo.py
```

The pipeline performs

- Data Ingestion
- Data Validation
- Data Transformation
- Model Training
- Model Evaluation
- Model Pusher

---

# 🌐 Run Flask Application

```bash
python app.py
```

Open

```
http://localhost:5000
```

Training Endpoint

```
/training
```

Prediction Endpoint

```
/
```

---

# ☁️ AWS Configuration

Create AWS IAM User

Create Access Key

Set Environment Variables

Linux

```bash
export AWS_ACCESS_KEY_ID=xxxxxxxx
export AWS_SECRET_ACCESS_KEY=xxxxxxxx
```

Windows

```powershell
$env:AWS_ACCESS_KEY_ID="xxxxxxxx"
$env:AWS_SECRET_ACCESS_KEY="xxxxxxxx"
```

Create S3 Bucket

Example

```
my-model-mlopsproj
```

The trained model will be automatically stored inside the S3 bucket.

---

# 🐳 Docker

Build Image

```bash
docker build -t vehicle-project .
```

Run Container

```bash
docker run -p 5000:5000 vehicle-project
```

---

# ⚡ GitHub Actions CI/CD

The project includes GitHub Actions workflow.

Workflow

```
Push Code
      │
      ▼
GitHub Actions
      │
      ▼
Build Docker Image
      │
      ▼
Push Image to AWS ECR
      │
      ▼
Deploy to EC2
```

---

# 🔐 GitHub Secrets

Configure the following repository secrets.

```
AWS_ACCESS_KEY_ID

AWS_SECRET_ACCESS_KEY

AWS_DEFAULT_REGION

ECR_REPO
```

---

# 🖥 EC2 Deployment

Launch Ubuntu EC2

Install Docker

```bash
curl -fsSL https://get.docker.com -o get-docker.sh

sudo sh get-docker.sh

sudo usermod -aG docker ubuntu

newgrp docker
```

Configure Self Hosted Runner

```
Settings

↓

Actions

↓

Runners

↓

New Self Hosted Runner
```

After pushing code, deployment happens automatically.

---

# 📈 Pipeline Components

### Data Ingestion

- Read data from MongoDB
- Export to DataFrame
- Split train/test

### Data Validation

- Schema validation
- Missing values
- Data drift detection

### Data Transformation

- Feature Engineering
- Encoding
- Scaling

### Model Trainer

- Train ML models
- Hyperparameter tuning
- Save best model

### Model Evaluation

- Compare new model with production model

### Model Pusher

- Upload best model to AWS S3

### Prediction Pipeline

- Load latest model
- Predict user input

---

# 📝 Logging

Application logs are stored inside

```
logs/
```

---

# 🚨 Exception Handling

Custom exception classes are implemented for easier debugging and production-ready error tracing.

---

# 📷 Screenshots

You can include screenshots here.

Example

- MongoDB Atlas
- Flask UI
- GitHub Actions
- AWS S3
- EC2 Deployment

---

# 👨‍💻 Future Improvements

- MLflow Integration
- Kubernetes Deployment
- Airflow Scheduling
- Monitoring with Prometheus
- Grafana Dashboard
- Model Drift Detection
- Unit Testing
- FastAPI Support

---

# 📄 License

This project is licensed under the MIT License.

---

# 🙌 Acknowledgements

This project demonstrates an end-to-end MLOps workflow combining modern machine learning engineering practices with cloud deployment and CI/CD automation.

---

# ⭐ Support

If you found this project helpful,

⭐ Star this repository

🍴 Fork the project

🐛 Raise issues

🚀 Contribute to improve it.