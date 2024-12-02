# Node.js Application Deployment on AWS EC2  

This repository demonstrates the deployment of a Node.js application on an AWS EC2 instance. The project includes the use of a `.env` file to manage sensitive environment variables securely.

---

## 📑 Table of Contents  
1. [Project Overview](#project-overview)  
2. [Prerequisites](#prerequisites)  
3. [Setup and Deployment](#setup-and-deployment)  
4. [Environment Variables (.env)](#environment-variables-env)  
5. [Testing the Application](#testing-the-application)  
6. [Screenshots](#screenshots)  
7. [Why Use a .env File?](#why-use-a-env-file)  
8. [Tech Stack](#tech-stack)  
9. [Contributors](#contributors)  

---

## 🌟 Project Overview  

This project guides you through:  
- Setting up an AWS EC2 instance.  
- Installing necessary dependencies (Git, Node.js, npm).  
- Deploying a Node.js application.  
- Managing sensitive credentials using a `.env` file.  
- Testing the application locally and on the server.  

---

## ✅ Prerequisites  

1. AWS Account with EC2 instance created.  
2. Security group with port 3000 open.  
3. Basic understanding of Node.js and AWS.  

---

## 🚀 Setup and Deployment  

1. **Update the system:**  
   ```bash
   sudo yum update -y
Install Git and npm:

bash
Copy code
sudo yum install git -y  
sudo yum install npm -y  
Clone the repository and navigate to the project directory:

bash
Copy code
git clone <repository-url>  
cd <repository-name>  
Install dependencies:

bash
Copy code
npm install  
Create a .env file:
Create a hidden file named .env in the project root and configure it as shown below:

plaintext
Copy code
DOMAIN=  
PORT=3000  
STATIC_DIR="./client"  
PUBLISHABLE_KEY=<your-stripe-publishable-key>  
SECRET_KEY=<your-stripe-secret-key>  
Start the application locally:

bash
Copy code
npm run start  
Visit http://localhost:3000 to ensure the application is working locally.

Deploy the application to EC2:
Navigate to the EC2 instance (via AWS Session Manager or SSH) and repeat steps 4–6.

Test on the server:
Access the application using the EC2 public IP:

plaintext
Copy code
http://<your-ec2-public-ip>:3000  
🔐 Environment Variables (.env)
The .env file contains sensitive credentials such as API keys and configuration variables.
Example content:

plaintext
Copy code
DOMAIN=  
PORT=3000  
STATIC_DIR="./client"  
PUBLISHABLE_KEY=<Stripe Publishable Key>  
SECRET_KEY=<Stripe Secret Key>  
🧪 Testing the Application
Local Testing:
Run the application on http://localhost:3000.

Server Testing:
Visit http://<EC2-Public-IP>:3000 to confirm the deployment.

📷 Screenshots
Application Running Locally:

Application Running on EC2:

🤔 Why Use a .env File?
The .env file helps to:

Secure Credentials: Prevent sensitive information (like API keys) from being exposed in the codebase.
Easy Configuration: Centralize application settings for easy changes without modifying the source code.
Environment variables are critical for:

Hiding public access keys.
Configuring domain, port, and API keys dynamically.
Ensuring secure deployment practices.
💻 Tech Stack
Node.js
AWS EC2
npm
Stripe API
👥 Contributors
Rohit Anand
GitHub Profile
