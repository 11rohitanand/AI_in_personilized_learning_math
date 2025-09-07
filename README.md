# AI_in_personilized_learning_math
Project in the course Minor in AI


AI-Powered Personalized Learning Platform
Project Overview
This project is an AI-powered personalized learning platform designed to adapt educational content to a student's progress and learning style. It features a dynamic math quiz for students in classes 1-5, tracking their performance across different topics and difficulty levels. The platform provides a personalized analysis of strengths and weaknesses and recommends areas for improvement.
The core of this system is a rule-based AI engine that processes quiz results to provide tailored feedback. This approach offers a practical and effective demonstration of how AI principles can be applied to create smart, adaptive educational tools without the need for complex machine learning models.
Features
•	Student Registration: A simple and secure form for students to enter their name, a unique 6-digit code, and class level.
•	Persistent Data Storage: Student information and quiz history are stored in a local student_data.json file, allowing the application to track progress over multiple sessions on the same machine.
•	Adaptive Quiz Generation: The platform selects 10 random questions from a diverse bank of 50, ensuring a unique test experience for each attempt.
•	Personalized Analysis: After each quiz, the system provides a detailed breakdown of performance by topic (e.g., addition, fractions) and difficulty level (easy, medium, hard).
•	Progress Tracking: When a returning student completes a quiz, the system retrieves their previous score and highlights their improvement, providing motivational feedback.
•	Strengths and Weaknesses Identification: The AI engine analyzes quiz results to identify areas where the student excels and areas that require more practice.
•	Content Recommendation: Based on the performance analysis, the system recommends specific chapters for the student to focus on.
Technology Stack
•	Python: The primary programming language used for the entire application logic.
•	Streamlit: An open-source Python library used to build and serve the interactive web application interface.
•	JSON: A simple, lightweight data-interchange format used for local data storage.
Getting Started
This application can be deployed in two ways: locally on your computer or publicly using Streamlit Community Cloud.
Prerequisites
•	GitHub Account: Required for hosting the project code, especially for online deployment.
•	Streamlit Account: Required to deploy the application online via Streamlit Community Cloud.
Local Deployment
Follow these steps to set up and run the application on your local machine.
Step 1: Install Required Libraries
Open your command prompt or terminal and install Streamlit.
pip install streamlit

Step 2: Project Structure
Organize your project files as follows:
project/
├── src/
│   └── math_recommender_advanced.py
├── database/
│   └── student_data.json
└── README.md

Step 3: Run the Application
1.	Open your command prompt or terminal.
2.	Navigate to the src directory where your Python file is located.
3.	cd "C:\Minor in AI- IIT Ropar\project\src"

4.	Run the application using the Streamlit command.
5.	streamlit run math_recommender_advanced.py

6.	A new browser tab will automatically open with the application running. The first time you run it, a database folder and a student_data.json file will be created at the path specified in the code.
Online Deployment via Streamlit Community Cloud
1.	Push to GitHub: Ensure your project, including the math_recommender_advanced.py file, is pushed to your GitHub repository.
2.	Connect to Streamlit: Log in to your Streamlit account and click "New app".
3.	Deploy: Select your repository, the correct branch, and set the main file path to src/math_recommender_advanced.py. Click "Deploy!".
Note: The local student_data.json file will not be available in the online version. Each session on the deployed app will be new.
How the System Works
1.	User Input: The student provides their name, a 6-digit code, and class. This information is used to load their existing profile or create a new one in the local JSON file.
2.	Quiz Generation: A quiz with 10 random questions is dynamically generated from the question bank.
3.	Data Collection: When the student submits the quiz, the application grades their answers.
4.	Analysis Engine: The system calculates scores for each chapter and difficulty level and compares the current score with the student's most recent score from their quiz history.
5.	Personalized Feedback: Based on the analysis, the system provides a report on strengths, weaknesses, and progress.
6.	Data Persistence: All quiz results are saved to the local student_data.json file for future analysis.
Evaluation
Since this project utilizes a rule-based AI system, its performance is not measured by traditional machine learning accuracy metrics. Instead, its success is evaluated based on its effectiveness in providing a personalized learning experience. Key evaluation criteria include:
•	Relevance of Recommendations: The system's ability to correctly identify a student's weak areas based on their quiz performance and provide logical recommendations.
•	Impact on Learning: Whether the student's scores show improvement over time after following the system's feedback, a metric tracked by the progress-monitoring feature.
•	User Experience: The clarity, usability, and motivational quality of the feedback provided to the student.
Future Work
This project serves as a strong foundation that can be expanded in several ways:
•	Machine Learning Integration: The rule-based engine could be replaced with a supervised learning model to predict which topics a student might struggle with based on their historical data.
•	Advanced Content Adaptation: The system could adapt not just the recommended topics but also the difficulty of the next quiz based on the student's performance.
•	Teacher Dashboard: A separate interface could be developed for educators to view class-wide performance and track individual student progress.
•	Cloud Database Migration: For a scalable, multi-user application, the local JSON storage could be migrated to a cloud database like Firebase Firestore.

