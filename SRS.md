# Software Requirements Specification (SRS)

## 1. Introduction
- **Purpose:**
  - To automate the evaluation of exam papers for teachers and professors using OCR and LLM technologies.
- **Project Scope:**
  - Web-based system for uploading, processing, and evaluating handwritten student answer sheets.

## 2. Overall Description
- **Product Perspective:**
  - The system is a standalone web application integrating OCR and LLM services for automated grading.
- **Product Features:**
  - Teacher registration/login
  - Exam setup (question paper, answer key, marks allocation)
  - Student answer sheet upload
  - Automated evaluation (objective/subjective)
  - Result reporting (PDF/CSV)
- **User Classes:**
  - Teachers, professors, academic staff
- **Operating Environments:**
  - Web browser, internet connection required for cloud LLM
- **Design & Implementation Constraints:**
  - English handwritten answers only
  - Secure authentication and data privacy
- **User Documentation:**
  - User manual, deployment guide

## 3. Functional Requirements


### 3.1 User Management & Authentication
- **Input:** Teacher registration details (email, password), login credentials 
- **Output:** Authentication status (success/failure), user session


### 3.2 Exam Setup & Configuration
- **Input:** Question paper file (PDF/DOC), answer key, marks allocation per question 
- **Output:** Exam configuration stored, confirmation of setup


### 3.3 Answer Sheet Processing
- **Input:** Scanned handwritten answer sheets (PDF/JPG/PNG), student identification 
- **Output:** Extracted text from answer sheets, linked to student ID


### 3.4 Answer Evaluation
- **Input:** Extracted student answers, answer key, exam configuration
- **Output:** Marks per question, short feedback for each answer


### 3.5 Result Generation & Reporting
- **Input:** Evaluation results (marks, feedback), student and exam data
- **Output:** Individual student reports (question-wise marks, total score, feedback), exported files (PDF/CSV)

## 4. External Interface Requirements
- **User Interface:**
  - Intuitive web UI for teachers to manage exams and view results.
- **Hardware Interface:**
  - Scanners or mobile cameras for digitizing answer sheets.
- **Software Interface:**
  - Integration with OCR agent (e.g., Tesseract)
  - Integration with LLM agent (e.g., OpenAI API)
- **Communication Interface:**
  - Secure HTTPS for all data transfers

## 5. Other Non-Functional Requirements
- **Performance Requirements:**
  - System should process batches of 50–200 answer sheets efficiently.
  - Low-latency OCR and evaluation pipeline.
- **Safety Requirements:**
  - Data backup and recovery mechanisms for exam and result data.
- **Security Requirements:**
  - Secure authentication for teachers
  - Encrypted storage for student answer sheets and results
  - Compliance with academic data privacy standards
