# Drug Prediction Machine Learning Model

## Overview
This project aims to predict the efficacy and potential toxicity of drug compounds using machine learning. It leverages datasets from chemical compound databases, clinical trials, and molecular structures to train predictive models for drug discovery and development.

## Architecture
The system follows a structured pipeline:

1. **Data Ingestion**: Collects data from sources like PubChem, DrugBank, and clinical trial reports.
2. **Data Preprocessing**: Cleans and preprocesses data, including feature extraction and normalization.
3. **Machine Learning Models**: Implements various algorithms such as Random Forest, Support Vector Machines (SVM), and Deep Learning models.
4. **Model Training & Validation**: Trains models, performs hyperparameter tuning, and validates performance using metrics like accuracy, ROC-AUC, and F1-score.
5. **Prediction & Inference**: Uses trained models to predict drug properties such as efficacy and toxicity.
6. **Deployment & API Integration**: Deploys the model as a REST API for real-time predictions.
7. **Monitoring & Feedback**: Continuously updates the model based on new data to maintain accuracy.

## Installation

### Prerequisites
- Python 3.8+
- pip
- Virtual environment (optional but recommended)

### Dependencies
```bash
pip install -r requirements.txt
```

## Usage

1. **Prepare the Dataset**: Ensure the dataset is available in the `data/` directory.
2. **Run Preprocessing**:
   ```bash
   python preprocess.py
   ```
3. **Train the Model**:
   ```bash
   python train.py
   ```
4. **Evaluate the Model**:
   ```bash
   python evaluate.py
   ```
5. **Run Inference**:
   ```bash
   python predict.py --input sample_data.csv
   ```
6. **Deploy as API**:
   ```bash
   python app.py
   ```

## API Endpoints
- `POST /predict`: Predicts drug efficacy based on input data.
- `GET /health`: Checks API health status.

## Project Structure
```
├── data/                 # Raw and processed datasets
├── models/               # Trained model files
├── src/
│   ├── preprocess.py     # Data preprocessing script
│   ├── train.py         # Model training script
│   ├── evaluate.py      # Model evaluation script
│   ├── predict.py       # Inference script
│   ├── app.py           # API server script
├── requirements.txt      # Required dependencies
├── README.md             # Project documentation
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
