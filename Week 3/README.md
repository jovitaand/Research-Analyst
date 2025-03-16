# 📚 iSchool Chatbot

A Streamlit-based chatbot application developed to provide information about Syracuse University's iSchool programs, courses, and program requirements. The chatbot retains chat history and responds dynamically based on user queries.

## 🚀 Features

- Lists available iSchool programs (On-Campus and Online)
- Provides core and elective courses for the Applied Data Science program
- Displays program requirements and tracks
- Maintains chat history using Streamlit's session state
- Public deployment accessible via GitHub Codespaces

## 🛠️ Setup Instructions

### 1. Clone Repository
```bash
git clone <repository-url>
cd <repository-directory>
```

### 2. Open in Codespaces
1. Open the repository on GitHub.
2. Click on **Code** > **Codespaces** > **Create codespace on main**.

### 3. Install Dependencies
```bash
pip install streamlit
```

### 4. Run the Application
```bash
streamlit run app.py --server.address 0.0.0.0 --server.port 8501
```

### 5. View the Application
A public URL will be provided by Codespaces to access the chatbot in your browser.

## 📝 Program Information Memory
- On-Campus Programs
  - Applied Data Science
  - Applied Human-Centered AI
  - Information Systems
  - Library and Information Science
  - Library and Information Science: School Library Media

- Online Programs
  - Applied Data Science
  - Information Systems for Executives
  - Library and Information Science
  - Library and Information Science: School Library Media

- Core Courses for Applied Data Science
  - IST 659 - Data Administration Concepts and Database Management
  - IST 686 - Quantitative Reasoning for Data Science
  - IST 687 - Introduction to Data Science
  - IST 707 - Applied Machine Learning
  - SCM 651 - Business Analytics

## 🌟 Future Enhancements
- Include real-time data fetching from the official iSchool website
- Enhance NLP capabilities for better query understanding
- Detailed program information for Applied Data Science program and other tracks
- Deployment on additional platforms like Streamlit Cloud

## 📄 License

This project is licensed for educational purposes.

