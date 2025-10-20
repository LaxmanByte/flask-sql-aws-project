Excellent — you’ve written a solid technical project report. To make it **portfolio-ready** and **professional for LinkedIn, GitHub README, or a résumé project section**, I’ve reformatted and enhanced it for clarity, scannability, and aesthetics while keeping *all technical details intact*.

Here’s the polished version:

---

# 🚀 Flask Hello World + Jinja Templates

### **My First Flask Web Application – From Local Development to AWS Deployment**

**Completion Date:** October 2025
**Status:** ✅ Successfully Completed and Deployed

---

## 🧩 **About This Project**

This project was built to gain **hands-on experience with Flask** and **end-to-end AWS deployment**.
It demonstrates my ability to:

* Develop Python web applications using **Flask Framework**
* Implement dynamic web pages with **Jinja2 Templates**
* Deploy production-ready applications to **AWS EC2 (Amazon Linux 2)**
* Manage source code using **Git and GitHub**
* Configure and administer **Linux servers for web hosting**
* Professionally document technical projects

> **Key Achievement:**
> Successfully took an application from **local development** to **live deployment on AWS infrastructure.**

---

## 🧠 **What I Learned**

### 🧩 Technical Skills Acquired

| **Skill Area**                 | **What I Accomplished**                                             |
| ------------------------------ | ------------------------------------------------------------------- |
| **Flask Framework**            | Built multi-route applications handling HTTP requests & responses   |
| **Jinja2 Templates**           | Created dynamic HTML templates that render Python data              |
| **AWS EC2**                    | Launched, configured, and deployed Flask apps to cloud servers      |
| **Linux Administration**       | Managed Amazon Linux 2, installed dependencies, configured services |
| **Git & GitHub**               | Version-controlled code and used GitHub as deployment source        |
| **Client-Server Architecture** | Understood the full HTTP request/response flow                      |

### 🎯 Learning Outcomes

* Understood client-server architecture
* Installed and configured Flask locally and remotely
* Built functional Flask applications with routes and templates
* Used Git effectively for versioning
* Deployed and hosted applications on AWS EC2

---

## ⚙️ **Technical Implementation**

### **Architecture Overview**

```
Browser (Client)
   ↓
Flask App (Python)
   ↓
Jinja2 Templates (Dynamic HTML)
   ↓
Response → Client Browser
```

**Hosting:** AWS EC2 (Amazon Linux 2, t2.micro)

### **Development Workflow**

`Local Development → Git Commit → GitHub Push → AWS EC2 Deployment → Live Application`

---

## 🔍 **Part 1: Understanding Flask Framework**

Flask is a lightweight, micro-framework for Python ideal for small to medium web apps.

**Flask Features Used:**

* Built-in development server
* Jinja2 templating engine
* URL routing system
* Integrated debugger
* WSGI 1.0 compliance

---

## 💻 **Part 2: Hello World Application**

**File:** `hello-world-app.py`

Implemented routes for:

* Static URLs
* Nested routes
* Dynamic URL parameters (`/<name>`)
* Request handling and response generation

---

## 🧩 **Part 3: Jinja Template Integration**

Separated **presentation logic (HTML)** from **business logic (Python)** using Jinja2.

**Routes include:**

* **Homepage:** Displays a message passed from backend
* **Calculation route:** Renders arithmetic results dynamically

**Templates Folder:**

```
templates/
│── index.html     → Display message  
└── body.html      → Display calculation result  
```

---

## 📁 **Project Structure**

```
flask-01-02-hello-world-app-Jinja-Template/
│
├── README.md
│
├── flask-01-hello-world-app/
│   └── hello-world-app.py
│
├── flask-02-Jinja_Template/
│   ├── jinja.py
│   └── templates/
│       ├── index.html
│       └── body.html
```

---

## 🧑‍💻 **How to Run**

### **Prerequisites**

* Python 3
* pip

### **Local Setup**

```bash
git clone https://github.com/LaxmanByte/flask-sql-aws-project.git
pip3 install flask
```

#### Run Hello World App

```bash
cd flask-01-02-hello-world-app-Jinja-Template/flask-01-hello-world-app
python3 hello-world-app.py
# Access: http://localhost:80
```

#### Run Jinja Template App

```bash
cd flask-02-Jinja_Template
python3 jinja.py
# Access: http://localhost:5000
```

---

## ☁️ **AWS EC2 Deployment**

### **1. Launch EC2 Instance**

* **AMI:** Amazon Linux 2
* **Instance Type:** t2.micro
* **Security Group:** Allow ports 22 (SSH) and 80 (HTTP)

### **2. Connect via SSH**

```bash
chmod 400 your-key.pem
ssh -i your-key.pem ec2-user@EC2-PUBLIC-IP
```

### **3. Install Dependencies**

```bash
sudo yum update -y
sudo yum install python3 git -y
sudo pip3 install flask
```

### **4. Deploy Application**

```bash
git clone https://github.com/LaxmanByte/flask-sql-aws-project.git
cd flask-sql-aws-project/flask-01-02-hello-world-app-Jinja-Template/flask-01-hello-world-app
sudo python3 hello-world-app.py
```

### **5. Access Application**

Visit:
👉 `http://<EC2-PUBLIC-IP>`

---

## 🧰 **Technologies Used**

| Category              | Tools / Services         |
| --------------------- | ------------------------ |
| **Languages**         | Python 3                 |
| **Framework**         | Flask                    |
| **Templating Engine** | Jinja2                   |
| **Cloud Platform**    | AWS EC2 (Amazon Linux 2) |
| **Version Control**   | Git, GitHub              |
| **Utilities**         | SSH, pip, curl           |

---

## 🧩 **Challenges and Solutions**

| **Challenge**                              | **Solution Implemented**                            |
| ------------------------------------------ | --------------------------------------------------- |
| Permission errors running Flask on port 80 | Used `sudo` and configured correct permissions      |
| HTTP access blocked                        | Updated AWS Security Group inbound rules            |
| Template loading issues                    | Fixed directory structure for `templates/` folder   |
| App termination after SSH logout           | Used `nohup` and `systemd` for persistent execution |

---

## 🌟 **Key Takeaways**

* Developed and deployed a complete **Flask web app from scratch**
* Strengthened understanding of **Python web development & cloud deployment**
* Improved **problem-solving and debugging skills**
* Learned **production deployment best practices**

---

## 🔗 **Project Links**

* **GitHub Profile:** [github.com/LaxmanByte](https://github.com/LaxmanByte)
* **Project Repository:** [github.com/LaxmanByte/flask-sql-aws-project](https://github.com/LaxmanByte/flask-sql-aws-project)





**📅 Last Updated:** October 19, 2025
**📌 Status:** Completed & Deployed on AWS EC2


