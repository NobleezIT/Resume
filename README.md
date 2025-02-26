# AI-Powered Resume Analyzer

## Overview
This project is a **Streamlit web app** that analyzes resumes and matches them with job descriptions. It performs **skill extraction, text analysis, and visualization** to help users identify gaps and optimize their resumes.

## Features
- 📄 **Upload Resume (PDF format)**
- 📌 **Extract and analyze skills** using NLP
- 📊 **Generate visual insights** (word clouds, skill matching, etc.)
- 🔍 **Compare resume with job descriptions**
- 📈 **Score resumes based on relevance**

## Tech Stack
- **Python**
- **Streamlit** (for the web interface)
- **spaCy** (for NLP-based skill extraction)
- **scikit-learn** (for text processing and similarity matching)
- **Pandas & NumPy** (for data handling)
- **Matplotlib & Seaborn** (for data visualization)

## Installation & Setup
### Prerequisites
Ensure you have **Python 3.8+** installed on your system.

### Clone the Repository
```sh
git clone https://github.com/your-username/resume-analyzer.git
cd resume-analyzer
```

### Install Dependencies
```sh
pip install -r requirements.txt
```

### Download NLP Model (if not pre-installed)
```sh
python -m spacy download en_core_web_sm
```

## Usage
Run the Streamlit app using:
```sh
streamlit run app.py
```
Then, open the provided **localhost URL** in your browser.

## Deployment
### Deploying on Streamlit Cloud
1. Push your code to **GitHub**
2. Go to [Streamlit Cloud](https://share.streamlit.io/)
3. Connect your repository & deploy

### Deploying with Docker
Create a **Dockerfile**:
```dockerfile
FROM python:3.8
WORKDIR /app
COPY requirements.txt ./
RUN pip install -r requirements.txt
COPY . .
CMD ["streamlit", "run", "app.py", "--server.port=8501", "--server.address=0.0.0.0"]
```
Then build and run the container:
```sh
docker build -t resume-analyzer .
docker run -p 8501:8501 resume-analyzer
```

## Contributing
Feel free to open issues or submit pull requests! 🚀

## License
[MIT License](LICENSE)

---
