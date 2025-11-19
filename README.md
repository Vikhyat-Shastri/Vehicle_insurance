# Vehicle Insurance Prediction - MLOps Pipeline

An end-to-end machine learning operations (MLOps) project for predicting vehicle insurance responses. This project demonstrates production-grade ML pipeline development with cloud integration, automated deployment, and scalable architecture.

## 🎯 Project Overview

This project implements a complete MLOps pipeline for vehicle insurance prediction, featuring:

- **Modular Architecture**: Well-structured components for data ingestion, validation, transformation, and model training
- **Cloud Integration**: MongoDB Atlas for data storage and AWS S3 for model versioning
- **Production Ready**: FastAPI-based REST API with web interface
- **CI/CD Pipeline**: Automated deployment using Docker and GitHub Actions
- **Scalable Design**: Enterprise-level code organization following best practices

## 🏗️ Architecture

```
Data Ingestion → Data Validation → Data Transformation → Model Training → Model Evaluation → Deployment
```

The pipeline is built with:
- MongoDB for data persistence
- AWS S3 for model storage
- FastAPI for API serving
- Docker for containerization
- GitHub Actions for CI/CD

## 🚀 Quick Start

### Prerequisites
- Python 3.10+
- MongoDB Atlas account
- AWS account (for S3 and deployment)
- Docker (for containerization)

### Installation

1. Clone the repository:
```bash
git clone <your-repo-url>
cd Vehicle_insurance
```

2. Create and activate virtual environment:
```bash
conda create -n vehicle python=3.10 -y
conda activate vehicle
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Set up environment variables:
```bash
# Windows PowerShell
$env:MONGODB_URL = "your_mongodb_connection_string"
$env:AWS_ACCESS_KEY_ID = "your_aws_access_key"
$env:AWS_SECRET_ACCESS_KEY = "your_aws_secret_key"
$env:AWS_DEFAULT_REGION = "us-east-1"
```

### Running the Application

1. Train the model:
```bash
python demo.py
```

2. Start the FastAPI server:
```bash
python app.py
```

3. Access the web interface at `http://localhost:5000`

## 📊 Features

### Data Pipeline
- **Data Ingestion**: Automated data loading from MongoDB
- **Data Validation**: Schema validation using YAML configurations
- **Data Transformation**: Feature engineering and preprocessing
- **Model Training**: Hyperparameter-tuned machine learning models

### Model Management
- Model versioning with AWS S3
- Automated model evaluation and comparison
- Model registry for production deployments

### API & Interface
- RESTful API with FastAPI
- Interactive web interface for predictions
- Health check endpoints
- Swagger documentation

### DevOps
- Docker containerization
- GitHub Actions CI/CD
- AWS EC2 deployment
- Environment-based configuration

## 🗂️ Project Structure

```
├── src/
│   ├── components/       # Pipeline components
│   ├── configuration/    # Database and cloud connections
│   ├── data_access/      # Data access layer
│   ├── entity/           # Data models and entities
│   ├── pipline/          # Training and prediction pipelines
│   └── utils/            # Utility functions
├── config/               # Configuration files
├── notebook/             # Jupyter notebooks for EDA
├── static/               # Static files for web UI
├── templates/            # HTML templates
├── app.py               # FastAPI application
├── Dockerfile           # Container configuration
└── requirements.txt     # Python dependencies
```

## 🔧 Configuration

Configuration files are located in the `config/` directory:
- `model.yaml`: Model hyperparameters
- `schema.yaml`: Data validation schema

## 🧪 Testing

Run tests using:
```bash
pytest tests/
```

## 📦 Deployment

### Docker

Build and run the Docker container:
```bash
docker build -t vehicle-insurance .
docker run -p 5000:5000 vehicle-insurance
```

### AWS EC2

The project includes GitHub Actions workflows for automated deployment to AWS EC2. Configure the following secrets in your GitHub repository:
- `AWS_ACCESS_KEY_ID`
- `AWS_SECRET_ACCESS_KEY`
- `AWS_DEFAULT_REGION`
- `ECR_REPO`
- `MONGODB_URL`

## 📝 API Documentation

Once the server is running, access the interactive API documentation at:
- Swagger UI: `http://localhost:5000/docs`
- ReDoc: `http://localhost:5000/redoc`

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

Built with modern MLOps practices and tools including FastAPI, scikit-learn, MongoDB, AWS, and Docker.