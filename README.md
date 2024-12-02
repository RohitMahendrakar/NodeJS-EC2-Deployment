Here's the complete `README.md` with all the points you provided, formatted correctly with code blocks and additional information:

```markdown
# Node.js Application Deployment on AWS EC2 🚀

This repository demonstrates the deployment of a Node.js application on an AWS EC2 instance. The project uses a `.env` file to securely manage environment variables like API keys and other sensitive information.

---

## 📋 Project Overview

This project covers:
- Setting up an AWS EC2 instance.
- Installing necessary dependencies (Git, Node.js, npm).
- Deploying a Node.js application.
- Using a `.env` file to manage sensitive credentials.
- Testing the application both locally and on the server.

---

## ⚙️ Prerequisites

Before you begin, ensure you have the following:
1. An **AWS Account** with an EC2 instance created.
2. A **Security group** with port 3000 open.
3. Basic knowledge of **Node.js** and **AWS**.

---

## 🛠 Setup and Deployment

### 1. **Update the System:**
```bash
sudo yum update -y
```

### 2. **Install Git and npm:**
```bash
sudo yum install git -y  
sudo yum install npm -y  
```

### 3. **Clone the Repository:**
Clone the repository and navigate to the project directory:
```bash
git clone <repository-url>  
cd <repository-name>  
```

### 4. **Install Dependencies:**
```bash
npm install  
```

### 5. **Create a `.env` File:**

Create a hidden file `.env` in the project root and configure it as shown below:

```plaintext
DOMAIN=  
PORT=3000  
STATIC_DIR="./client"  
PUBLISHABLE_KEY=<your-stripe-publishable-key>  
SECRET_KEY=<your-stripe-secret-key>  
```

### 6. **Start the Application Locally:**
```bash
npm run start  
```
Go to `http://localhost:3000` to verify that the application is working locally.

### 7. **Deploy to EC2:**

- Access the EC2 instance (via SSH or AWS Session Manager).
- Repeat steps 4–6 on the EC2 instance.

### 8. **Test on EC2:**
Open your browser and visit the following to test the deployment:
```plaintext
http://<your-ec2-public-ip>:3000
```

---

## 🌱 Environment Variables (.env)

The `.env` file holds sensitive information like API keys, which should not be exposed in your codebase.

**Example `.env` content:**
```plaintext
DOMAIN=  
PORT=3000  
STATIC_DIR="./client"  
PUBLISHABLE_KEY=<Stripe Publishable Key>  
SECRET_KEY=<Stripe Secret Key>  
```

This file helps keep sensitive credentials secure and makes it easier to configure the app for different environments.

---

## ✅ Testing the Application

- **Local Testing:**  
  Run the application on `http://localhost:3000` to check locally.

- **Server Testing:**  
  Open the EC2 instance’s public IP in a browser: `http://<EC2-Public-IP>:3000`.

---

## 🖼 Screenshots

1. **Application Running Locally:**  
   ![Localhost Screenshot](./screenshots/localhost.png)

2. **Application Running on EC2:**  
   ![EC2 Screenshot](./screenshots/ec2.png)

---

## 🔐 Why Use a `.env` File?

The `.env` file is essential for securely managing environment variables and configuration settings. Here’s why it’s important:

- **Secure Credentials:** Prevents exposing sensitive information (like API keys) in the codebase.
- **Configuration Flexibility:** Easily adjust configuration without modifying source code.

### Benefits of Environment Variables:
- Hide public access keys.
- Configure domain, port, and API keys dynamically.
- Ensure best practices for secure deployment.

---

## 🖥 Tech Stack

- **Node.js**  
- **AWS EC2**  
- **npm**  
- **Stripe API**
```

This `README.md` is structured with code blocks and icons to maintain readability and clarity.
