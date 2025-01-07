# QuickDataProcessor (QDP)

QuickDataProcessor (QDP) is a scalable, serverless, event-driven platform designed to handle user management, virtual assistance, messaging, notifications, data processing, and analytics workflows. Built using a cloud-native approach, QDP leverages the power of AWS and GCP services to deliver a robust and modular solution.

## Features

### 1. User Management & Authentication
- **Multi-Factor Authentication:**
    - **First Factor:** AWS Cognito for user ID and password authentication.
    - **Second Factor:** DynamoDB and Lambda for question/answer validation.
    - **Third Factor:** Lambda for mathematical skill validation.
- **User Registration:** Implemented via a lightweight React frontend with user data stored in DynamoDB.

### 2. Virtual Assistant
- **Online Navigation:** Developed using GCP DialogFlow, Firestore, and Cloud Functions to assist users with tasks such as registration and file retrieval.
- **Customer Queries:** Handles customer concerns and forwards them to QDP agents.
- **Real-Time Interaction:** Enabled through GCP Pub/Sub for seamless message passing.

### 3. Message Passing
- **Asynchronous Communication:** Implemented using GCP Pub/Sub to handle communication between users and QDP agents.
- **Message Logging:** All interactions logged in NoSQL databases (DynamoDB or Firestore).

### 4. Notifications
- **Event-Driven Notifications:**
    - Successful registration and login notifications sent via AWS SNS.
    - Processing success/failure updates sent via AWS SNS/SQS.
- **Decoupled Communication:** SNS-SQS integration ensures scalable and robust communication between application components.

### 5. Data Processing
- **Automated Workflows:**
    - **JSON to CSV Conversion:** Processed using AWS Glue and stored in DynamoDB.
    - **Named Entity Recognition:** Extracted from text files via AWS Lambda and saved in DynamoDB.
    - **Word Cloud Generation:** Created using GCP Looker Studio for visualization.
- **File Uploads:** Managed through the frontend and processed in the backend seamlessly.

### 6. Data Analysis
- **Interactive Dashboards:**
    - Admins can view user and login statistics via Looker Studio dashboards embedded in the frontend.
    - Customers and agents can access feedback and sentiment analysis results in tabular formats.
- **Sentiment Analysis:** Google Natural Language API analyzes feedback for meaningful insights.

### 7. Web Application Deployment
- **Frontend Development:** Built using React and hosted on GCP Cloud Run for scalable and efficient deployment.
- **CI/CD Pipeline:** Automated using GCP Cloud Build with GitHub push triggers for streamlined updates.
- **Infrastructure as Code:** Utilized CloudFormation and GCP Cloud Deployment Manager for automated service provisioning.

## Technologies Used
- **Frontend:** React
- **Authentication:** AWS Cognito, DynamoDB, AWS Lambda
- **Notifications:** AWS SNS, AWS SQS
- **Messaging:** GCP Pub/Sub
- **Data Processing:** AWS Glue, AWS Lambda, GCP Looker Studio
- **Data Analysis:** Google Natural Language API
- **Deployment:** GCP Cloud Run, GCP Cloud Build, GitHub

## Architecture Overview
The application follows a modular architecture, ensuring scalability and fault tolerance:
1. User interactions are handled by the React frontend.
2. Backend processing is decoupled and event-driven, leveraging services like AWS Lambda, SNS/SQS, and GCP Pub/Sub.
3. Data storage and analytics use DynamoDB, Firestore, and Looker Studio.
4. The entire application is hosted and deployed via GCP Cloud Run with automated pipelines.

## Key Highlights
- **Serverless Architecture:** Fully serverless design for cost efficiency and scalability.
- **Event-Driven Design:** Decoupled components using SNS/SQS and Pub/Sub.
- **Robust Security:** Multi-factor authentication and secure messaging workflows.
- **Cloud-Native CI/CD:** Automated deployments using GCP Cloud Build and GitHub.

## Conclusion
QuickDataProcessor (QDP) is a comprehensive platform that combines user management, virtual assistance, messaging, notifications, data processing, and analytics capabilities. Leveraging the power of AWS and GCP services, QDP provides a scalable, secure, and cost-effective solution for modern businesses. With its modular architecture and event-driven design, QDP is well-equipped to handle diverse workflows and adapt to changing business requirements.

---