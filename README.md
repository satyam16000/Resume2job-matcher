Job Matcher: Resume to Job Description Matching System
This project is a machine learning-based system that matches resumes to job descriptions, providing a list of top matching resumes based on semantic similarity. The project utilizes multiple technologies like FastAPI, Streamlit, spaCy, Sentence Transformers, and more.

Features
Upload resumes in PDF, DOCX, or TXT formats.
Enter a job description and match it with uploaded resumes.
The system computes semantic similarity scores between the job description and resumes using a pre-trained Sentence Transformer model.
The top 3 resumes with the highest similarity scores are displayed.
Technologies Used
FastAPI: A modern web framework for building APIs with Python.
Streamlit: A Python library to quickly build data apps.
spaCy: Natural Language Processing (NLP) library for text processing.
Sentence-Transformers: For obtaining embeddings and computing semantic similarity.
PyPDF2 and docx2txt: For extracting text from PDF and DOCX files.
Uvicorn: ASGI server for FastAPI.
NumPy: For array handling and numerical operations.
Installation
1. Clone the repository
bash
Copy
Edit
git clone https://github.com/satyam16000/job-matcher.git
cd job-matcher
2. Set up a virtual environment
bash
Copy
Edit
python -m venv venv
3. Activate the virtual environment
On Windows:
bash
Copy
Edit
.\venv\Scripts\activate
On macOS/Linux:
bash
Copy
Edit
source venv/bin/activate
4. Install dependencies
bash
Copy
Edit
pip install -r requirements.txt
5. Download spaCy model
bash
Copy
Edit
python -m spacy download en_core_web_md
6. Run the application
To start the FastAPI server with Streamlit:

bash
Copy
Edit
streamlit run main.py
This will start the Streamlit app, and you can view it in your browser.

API Endpoints
/matcher
Method: POST

This endpoint allows the user to submit a job description and a list of resumes (PDF, DOCX, TXT). It returns the top matching resumes with similarity scores.

Parameters:
job_description: The job description text.
resumes: A list of uploaded resumes (PDF, DOCX, or TXT).
Response:
top_matches: A list of tuples, where each tuple contains the filename and similarity score of the top matching resumes.
Example Request
json
Copy
Edit
{
  "job_description": "Looking for a Python developer with experience in machine learning.",
  "resumes": ["resume1.pdf", "resume2.docx"]
}
Example Response
json
Copy
Edit
{
  "top_matches": [
    ["resume1.pdf", 0.95],
    ["resume2.docx", 0.89]
  ]
}
Contributing
Fork the repository.
Create a new branch (git checkout -b feature-branch).
Make your changes and commit (git commit -am 'Add new feature').
Push to the branch (git push origin feature-branch).
Open a pull request.
License
This project is licensed under the MIT License - see the LICENSE file for details.

Feel free to customize this README with any additional information specific to your project, like known issues or additional setup steps!
