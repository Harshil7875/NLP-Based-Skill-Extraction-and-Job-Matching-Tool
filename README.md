# NLP-Based Skill Extraction and Job Matching Tool

## Project Overview
The **NLP-Based Skill Extraction and Job Matching Tool** is designed to automate the extraction of key skills from job descriptions and candidate resumes and to match candidates with relevant job postings based on their skills. This tool leverages Natural Language Processing (NLP) techniques and machine learning to streamline the recruitment process, enhancing the relevance and speed of candidate-job matching.

## Objectives
- **Skill Extraction**: Identify and extract relevant skills from job descriptions and resumes.
- **Job Matching**: Use skill matching to rank job postings for candidates and vice versa.
- **Deployment-Ready API**: Serve the functionality via a RESTful API for easy integration into external applications.

## Key Technologies
- **Python**: Core programming language.
- **spaCy**: For NLP tasks, such as text tokenization and entity recognition.
- **TensorFlow with Metal**: GPU-accelerated training on macOS for fine-tuning BERT models.
- **Hugging Face Transformers**: Pre-trained BERT models for skill extraction.
- **FastAPI**: For creating a RESTful API.
- **Docker**: For containerization and easy deployment.

---

## Project Structure

```plaintext
nlp_skill_matching_project/
├── data/
│   ├── raw/
│   │   ├── job_listings.csv              # Raw job listings data
│   │   └── resumes.csv                   # Raw resumes data
│   ├── processed/
│   │   ├── cleaned_job_listings.csv      # Cleaned job listings data
│   │   └── cleaned_resumes.csv           # Cleaned resumes data
├── notebooks/
│   ├── data_preprocessing.ipynb          # Data cleaning and preprocessing notebook
│   ├── exploratory_data_analysis.ipynb   # EDA notebook for analyzing data patterns
│   └── model_training.ipynb              # Notebook for training and evaluating models
├── src/
│   ├── data_collection/
│   │   ├── linkedin_scraper.py           # Script to scrape LinkedIn job listings
│   │   └── resume_parser.py              # Script to parse resumes
│   ├── preprocessing/
│   │   ├── preprocess_jobs.py            # Job listing preprocessing script
│   │   └── preprocess_resumes.py         # Resume preprocessing script
│   ├── model/
│   │   ├── skill_extraction.py           # Fine-tuning BERT for skill extraction
│   │   ├── job_matching.py               # Job matching based on extracted skills
│   │   └── model_utils.py                # Helper functions for model training and evaluation
│   ├── api/
│   │   ├── main.py                       # FastAPI app for skill extraction and job matching
│   │   └── requirements.txt              # API dependencies
│   └── utils/
│       ├── config.py                     # Configuration file for project settings
│       └── helpers.py                    # Helper functions
├── models/
│   ├── bert_skill_extraction/            # Trained BERT model files
│   └── matching_model/                   # Job matching model files
├── logs/
│   ├── training.log                      # Model training logs
│   └── api.log                           # API request logs
├── tests/
│   ├── test_data_processing.py           # Tests for data processing
│   ├── test_skill_extraction.py          # Tests for skill extraction model
│   └── test_job_matching.py              # Tests for job matching
├── Dockerfile                            # Dockerfile for project containerization
├── README.md                             # Project documentation
├── config.yaml                           # Configuration file for paths and settings
└── requirements.txt                      # Dependencies for the project
