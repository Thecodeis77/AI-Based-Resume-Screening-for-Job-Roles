# AI-Based Resume Screening for Job Roles

## Project Overview

This project uses Deep Learning and Natural Language Processing to classify resumes into different job categories. It uses a pretrained BERT model that is fine-tuned on a labelled resume dataset.

The main goal is to make resume sorting easier by predicting suitable categories from the text available in a resume.

## Objectives

- Prepare and clean resume data.
- Convert resume text into tokens using the BERT tokenizer.
- Fine-tune a pretrained BERT model for resume classification.
- Evaluate the model using classification metrics.
- Predict the top three job categories for a new resume.

## Technologies Used

- Python
- Google Colab
- PyTorch
- Hugging Face Transformers
- pandas
- scikit-learn
- Matplotlib
- PyMuPDF for PDF text extraction

## Dataset

The project uses a dataset named `Resume.csv`, containing resume text and job category labels.

- Initial records: 2,484
- Records after cleaning: 2,481
- Number of categories: 24
- Input feature: Resume text
- Target variable: Job category

The dataset should be obtained from its original source. It is not included in this repository.

## Model

The project uses the pretrained `bert-base-uncased` model. It is fine-tuned for resume classification using the labelled dataset.

Main training settings:

- Batch size: 8
- Epochs: 2
- Learning rate: 2e-5
- Weight decay: 0.01
- Maximum sequence length: 256 tokens
- Optimizer: AdamW

## Results

The model achieved the following results on the test dataset:

- Test accuracy: 76.41%
- Weighted F1-score: 0.7402
- Test loss: 1.5195

These results apply to the dataset and test split used in this project. Predictions may not always be correct.

## Project Workflow

1. Load the resume dataset.
2. Clean missing and duplicate records.
3. Encode job categories.
4. Tokenize resume text using BERT.
5. Split the data into training, validation, and testing sets.
6. Fine-tune the pretrained BERT model.
7. Evaluate model performance.
8. Extract text from a PDF resume and predict the top three categories.

## How to Run

1. Download or open the `Jobs_pred.ipynb` notebook.
2. Open it in Google Colab.
3. Obtain the `Resume.csv` dataset from its original source.
4. Upload the dataset to the expected Colab location.
5. Run the notebook cells in order.
6. Follow the notebook instructions to train the model and test resume predictions.

A GPU runtime is recommended for faster model training.

## Limitations

- Prediction quality depends on the dataset and its category labels.
- The model may incorrectly classify some resumes.
- The system predicts resume categories; it does not make final hiring decisions.
- The current implementation is notebook-based and does not include a separate web application.

## Future Improvements

- Use a larger and more varied resume dataset.
- Compare BERT with other classification models.
- Improve the prediction interface.
- Add job-description matching.
- Explore explainable AI techniques.

## Author

Developed as a Deep Learning project for resume classification.
