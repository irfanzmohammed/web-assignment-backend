# Backend (Node.js + Express + MongoDB + JWT + n8n)

This is the backend for the authentication system.  
It provides REST APIs for:

- User Signup  
- User Login  
- Protected Dashboard Route  
- Triggering an n8n workflow on new signup (Welcome Email)

---

## 🚀 Tech Stack
- Node.js  
- Express.js  
- MongoDB Atlas (Mongoose)  
- JSON Web Token (JWT)  
- bcryptjs  
- Axios (for n8n webhook)

---

## 📌 API Endpoints

### **POST /api/auth/signup**
Creates a new user and triggers the n8n workflow to send a welcome email.

### **POST /api/auth/login**
Returns a JWT token and user data.

### **GET /api/auth/dashboard**
Protected route — requires:

## 🔐 Environment Variables
Create a **.env** file in the backend root:

## ▶️ Run the Server

### Install dependencies:
npm install

### Start (Production):
npm run start

### Development mode:
npm run dev


## ☁️ Deployment
This backend is deployed on **Render**.

## 📬 n8n Workflow (Signup → Welcome Email)
A webhook is triggered on every signup, and n8n sends a welcome email using **MailTrap SMTP**.

### Workflow Overview  
![Workflow](backend\assets\workflow.png)

### Execution Log  
![Execution](backend\assets\execution.png)

### Sample Email from MailTrap  
![Welcome Email](backend\assets\mailtrap-email.png)





