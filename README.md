# MLflow CI/CD Project

A comprehensive MLflow project demonstrating the full machine learning lifecycle with CI/CD integration.

## Overview

This project showcases how to use MLflow for tracking, registering, and deploying machine learning models using a CI/CD pipeline. It uses the Iris dataset to train a simple Logistic Regression model.

## Project Structure

- `start-mlflow.sh`: Script to start the MLflow tracking server
- `models/main.py`: Main script for training and registering the model
- `models/show_iris.py`: Utility script to display the Iris dataset
- `.github/workflows/mlflow.yml`: GitHub Actions workflow for CI/CD
- `requirements.txt`: Project dependencies

## Getting Started

### Prerequisites

- Python 3.7+
- Git

### Installation

1. Clone the repository
2. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

### Running the MLflow Server

```
./start-mlflow.sh
```

The server will be available at http://localhost:8080

### Training the Model

```
cd models
python main.py
```

## CI/CD Pipeline

The project includes a GitHub Actions workflow that:
1. Builds the environment
2. Trains the model
3. Deploys the model to Dev, Test, and Prod environments

## Monitoring and Maintenance

After deploying your model, you can monitor its performance using MLflow's tracking capabilities:

```
mlflow ui --port 8080
```

Regularly check model metrics and consider retraining when performance degrades.

## License

MIT