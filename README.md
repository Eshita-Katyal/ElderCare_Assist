👴 ElderCare Assist

ElderCare Assist is an educational prototype web application built with Python, Streamlit, SQLite, and Machine Learning to provide basic assistance and activity monitoring for elderly people.

The application brings elderly profiles, assistance requests, reminders, emergency alerts, activity monitoring, request management, and activity history into a single Streamlit dashboard.

📸 Application Preview
<img width="959" height="365" alt="image" src="https://github.com/user-attachments/assets/7870275b-1147-47ba-965c-edefa5a38152" />
The application includes a sidebar-based navigation system with:

🏠 Dashboard

👴 Elderly Profile

🤝 Assistance Request

💊 Reminders

🆘 Emergency Help

🤖 Activity Monitor

📋 Request Management

📊 Activity History

🎯 Project Objective

The main objective of ElderCare Assist is to develop a simple technology-based solution that can help manage common elderly-support activities while demonstrating the integration of:

Web Application + Database + Machine Learning

The project is designed as a prototype and can be extended in the future with real-time notifications, authentication, cloud deployment, and ServiceNow integration.

✨ Features

🏠 1. Dashboard

The dashboard provides a quick overview of the application.

It displays:

👴 Number of elderly users

🤝 Open assistance requests

💊 Pending reminders

🆘 New alerts

🔔 Today's reminders

📋 Recent assistance requests

The dashboard helps a caregiver or administrator get a quick view of the current status of the application.

👴 2. Elderly Profile

The application provides a section for maintaining elderly user information.

The profile can be used as the central reference for connecting assistance requests, reminders, emergency alerts, and activity monitoring with an elderly person.

🤝 3. Assistance Request

The Assistance Request module allows an elderly person or caregiver to submit a request for help.

The request includes:

Request type

Priority

Description of assistance needed

Submission of the request

Example request types can include medicine-related assistance and other daily support requirements.

💊 4. Reminders

The Reminders module is designed to manage important reminders for elderly users.

It can be used for activities such as:

Taking medicine

Appointments

Daily tasks

Other important activities

The dashboard can display pending reminders.

🆘 5. Emergency Help

The Emergency Help module provides a dedicated area for recording emergency assistance requirements.

This feature is intended to provide a simple way to capture an emergency-related request within the application.

Important: This is an educational prototype. The current application does not automatically contact emergency services.

🤖 6. Activity Monitor

The Activity Monitor is the machine-learning component of ElderCare Assist.

It uses HAR70+ sensor data to recognize human activities.

The application supports:

Demo sensor data

Uploading a sensor CSV

Running activity prediction

Displaying prediction results

Displaying prediction confidence

The sensor data uses six main sensor columns:

back_x
back_y
back_z
thigh_x
thigh_y
thigh_z

The application processes the sensor data and sends it to the trained machine-learning model.

Example activities

The activity monitoring component can recognize activities such as:

Walking

Sitting

Standing

Lying

Shuffling

Other activities represented by the trained model

Example prediction output:

Window    Activity     Confidence (%)
1         Standing     99.17
2         Standing     100.00
3         Standing     100.00
...

📊 7. Activity History

The Activity History module stores and displays activity prediction results.

It provides:

Activity-wise prediction history

Prediction confidence

Activity distribution

Average prediction confidence

The application can visualize the distribution of activities using a chart.

Example:

Activity Distribution

Walking      █████████████████
Standing     █████████████
Sitting      ███████
Shuffling   █

The activity history also displays the average prediction confidence calculated from the stored prediction results.

📋 8. Request Management

The Request Management module allows assistance requests to be reviewed and their status to be updated.

A request can be selected using its Request ID.

Possible request statuses include:

New
In Progress
Resolved
Closed

This provides a simple workflow for tracking an assistance request from creation to completion.

🧠 Machine Learning Workflow

The activity monitoring workflow is:

HAR70+ Sensor Data
        ↓
CSV Upload / Demo Data
        ↓
Data Loading
        ↓
Sensor Feature Selection
        ↓
Data Processing
        ↓
Feature / Window Processing
        ↓
Trained ML Model
        ↓
Activity Prediction
        ↓
Prediction Confidence
        ↓
Activity History
        ↓
Streamlit Visualization

🏗️ Application Architecture

                    ElderCare Assist
                           |
                    Streamlit Interface
                           |
          +----------------+----------------+
          |                |                |
      Dashboard       User Support       ML Module
          |                |                |
          |        +-------+-------+        |
          |        |       |       |        |
       Overview  Requests Reminders Emergency |
          |                |                |
          +----------------+----------------+
                           |
                       SQLite DB
                           |
                    Activity Results
                           |
                    Machine Learning
                           |
                     Sensor Data

🛠️ Technologies Used

Technology

Purpose

Python

Application development

Streamlit

Web application interface

SQLite

Local database management

Pandas

Data processing

NumPy

Numerical operations

Scikit-learn

Machine learning

Joblib

Loading the trained ML model

Jupyter Notebook

Development environment

HAR70+

Human activity sensor data

📁 Project Structure

A typical project structure is:

ElderCare_Assist/
│
├── eldercare_full_app.py
├── eldercare_activity_model.joblib
├── demo_sensor_data.csv
├── eldercare.db
├── README.md
├── requirements.txt
│
└── images/
    └── eldercare-dashboard.png

Keep the actual filenames in your repository consistent with the files you upload.

💻 Installation

Clone the repository:

git clone https://github.com/YOUR_USERNAME/ElderCare_Assist.git

Move into the project directory:

cd ElderCare_Assist

Install the required Python packages:

pip install streamlit pandas numpy scikit-learn joblib

If you have a requirements.txt file:

pip install -r requirements.txt

▶️ Run the Application

If the main Streamlit file is:

eldercare_full_app.py

run:

streamlit run eldercare_full_app.py

Streamlit will provide a local address such as:

http://localhost:8501

Open that address in your browser.

If your main application file has a different name, replace the filename in the command.

📓 Running from Jupyter Notebook

The project was developed using Jupyter Notebook and can be launched from a Jupyter cell.

Example:

import subprocess
import sys

app_path = r"C:\Users\eshit\eldercare_full_app.py"

process = subprocess.Popen([
    sys.executable,
    "-m",
    "streamlit",
    "run",
    app_path
])

print("ElderCare Assist is starting...")

Then open the Streamlit URL displayed by Streamlit.

🗄️ Database

The application uses SQLite for local data storage.

The database can store information related to:

Elderly Users
Assistance Requests
Reminders
Emergency Alerts
Activity Results

SQLite makes the prototype simple to develop and test without requiring a separate database server.

🤖 Machine Learning Model

The trained model is stored using Joblib:

eldercare_activity_model.joblib

The Streamlit application loads the model and uses sensor data to generate activity predictions.

The model is connected to the Streamlit interface through the Activity Monitor module.

📌 Current Status

Implemented

✅ Streamlit dashboard

✅ Elderly profile section

✅ Assistance request module

✅ Reminder module

✅ Emergency help module

✅ ML-based activity monitor

✅ Demo sensor data support

✅ Sensor CSV upload

✅ Activity prediction

✅ Prediction confidence

✅ Activity history

✅ Activity distribution visualization

✅ Request management

✅ SQLite database integration

Future Enhancements

🔐 User authentication

👨‍⚕️ Caregiver accounts

📱 Mobile application

🔔 SMS/email notifications

🚨 Real-time emergency notifications

📡 Real-time wearable/sensor integration

📈 Advanced activity analytics

☁️ Cloud database

🌐 Online deployment

🏥 Healthcare/appointment integration

🔗 ServiceNow integration

🔗 Future ServiceNow Integration

The current project is developed first as a standalone Python + Streamlit application.

A future version can connect the application with ServiceNow using APIs.

Possible ServiceNow records/tables could include:

Elderly Profile
Assistance Request
Reminder
Emergency Alert
Activity Monitoring
Activity History

Possible architecture:

ElderCare Assist
Python + Streamlit
        |
        | REST API
        ↓
    ServiceNow
        |
        +── Elderly Profiles
        +── Assistance Requests
        +── Reminders
        +── Emergency Alerts
        +── Activity Records

🔐 Disclaimer

ElderCare Assist is an educational prototype created for learning and portfolio purposes.

It is not a medical diagnosis system and should not replace professional medical advice or emergency services.

The emergency feature currently records information inside the application and does not automatically contact emergency services.

For production use, the application would require appropriate authentication, authorization, encryption, privacy controls, secure deployment, monitoring, and reliable emergency communication.

👩‍💻 Author

Eshita Katyal

B.Tech – Artificial Intelligence and Data Engineering

⭐ Project Highlights

This project demonstrates practical experience with:

Python
↓
Streamlit
↓
SQLite
↓
Machine Learning
↓
Sensor Data Processing
↓
Activity Prediction
↓
Interactive Dashboard

ElderCare Assist is intended to demonstrate how machine learning and application development can be combined to build a practical elderly-support prototype.
