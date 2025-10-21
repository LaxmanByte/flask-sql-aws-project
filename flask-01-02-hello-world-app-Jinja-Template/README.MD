
# 🚀 Flask Web App Deployment on AWS EC2

**From Code → to Cloud**  
A complete software development lifecycle project — from initial concept and local development to production deployment on AWS cloud infrastructure.

***

## 📖 Table of Contents

1. Overview
2. Challenge & Solution
3. Technology Stack
4. Architecture Diagram
5. Features Demonstrated
6. Project Journey
7. Setup & Installation
8. AWS Deployment Process
9. Code Walkthrough
10. Skills Demonstrated
11. Challenges & Solutions
12. Future Improvements
13. Project Statistics
14. Resources
15. File Structure Reference
16. Quick Start Commands
17. Connect With Me

***

## 🧭 Overview

This project represents a complete software development lifecycle—from local Flask app development to production-grade deployment on **AWS EC2**.

**Live Demo:**  
http://ec2-35-91-211-143.us-west-2.compute.amazonaws.com/

**GitHub Repo:**  
https://github.com/LaxmanByte/flask-sql-aws-project

***

## 💡 Challenge & Solution

**Challenge:**  
Build and deploy a web application that demonstrates:
- Flask + Jinja2 for dynamic routing and templates
- AWS EC2 hosting
- DevOps automation practices

**Solution:**  
A fully functional Flask app deployed on **AWS EC2**, accessible via a public URL — following real-world deployment workflows.

***

## 🛠️ Technology Stack

| Category      | Tools / Services                         |
| ------------- | ---------------------------------------- |
| Backend       | Python 3.9+, Flask 3.0+, Jinja2          |
| Cloud         | AWS EC2, Amazon Linux 2, Security Groups |
| Dev Tools     | VS Code, Git, GitHub, SSH, wget          |
| DevOps        | pip, bash, systemd (optional)            |

***

## 🏗️ Architecture Diagram

```
END USER (Web Browser)
        │
        ▼
   HTTP Request (Port 80)
        │
        ▼
┌──────────────────────────────┐
│ AWS EC2 INSTANCE (t3.micro)  │
│ us-west-2 (Oregon)           │
│                              │
│ ┌──────────────────────────┐ │
│ │   Flask Web Application  │ │
│ │  ├─ jinja.py             │ │
│ │  ├─ index.html           │ │
│ │  └─ body.html            │ │
│ └──────────────────────────┘ │
│                              │
│ Security Group: HTTP/SSH     │
└──────────────────────────────┘
        │
        ▼
GITHUB REPOSITORY (Source + Docs)
```

***

## ✨ Features Demonstrated

**Core Web Development**
- Dynamic routing (`/`, `/mult`)
- Template rendering (Jinja2)
- Data flow between Python and HTML

**Cloud & DevOps**
- AWS EC2 deployment
- Automated setup with `wget`
- Proper permissions & port 80 configuration

**Professional Practices**
- Version control (Git + GitHub)
- Documentation & screenshots
- Debugging & troubleshooting

***

## 🧩 Project Journey

<details>
<summary>📘 Phase 1: Learning Flask Framework</summary>

![Flask Overview](screenshots/01_flask_framework

  
*Understanding Flask's architecture, routing, and templates.*

</details>

<details>
<summary>💻 Phase 2: Local Development</summary>

![VS Code Structure](screenshots/02_vscode_project

  
*Organized project structure with templates folder.*

```plaintext
flask-02-Jinja_Template/
├── jinja.py
└── templates/
    ├── index.html
    └── body.html
```
</details>

<details>
<summary>🧪 Phase 3: Local Testing</summary>

![Local Test](screenshots/06_local_browser

  
*Homepage rendering successfully on localhost.*

</details>

<details>
<summary>☁️ Phase 4: AWS EC2 Setup</summary>

![EC2 Launch](screenshots/10_aws_ec2_instance

  
*AWS EC2 instance configured and running.*

</details>

<details>
<summary>🚀 Phase 5: Deployment</summary>

![Deployment](screenshots/13_ssh_terminal used:
```bash
ssh -i "key.pem" ec2-user@your-ec2-dns
sudo yum install -y python3 pip wget
pip3 install flask
wget .../jinja.py
sudo python3 jinja.py
```
</details>

***

## ⚙️ Setup & Installation

**Prerequisites**
- Python 3.9+
- pip
- Git
- AWS Account

**Local Setup**
```bash
git clone https://github.com/LaxmanByte/flask-sql-aws-project.git
cd flask-sql-aws-project/flask-01-02-hello-world-app-Jinja-Template/flask-02-Jinja_Template
pip install flask
python jinja.py
```
Visit:  
http://127.0.0.1/  
http://127.0.0.1/mult

***

## ☁️ AWS Deployment Process

```bash
# Connect
ssh -i "Lax-key.pem" ec2-user@<your-ec2-dns>

# Install dependencies
sudo yum update -y
sudo yum install -y python3 python3-pip wget
pip3 install flask

# Download app
mkdir -p templates
wget https://raw.githubusercontent.com/<username>/<repo>/main/flask-01-02-hello-world-app-Jinja-Template/flask-02-Jinja_Template/jinja.py
wget -P templates/ https://raw.githubusercontent.com/<username>/<repo>/main/flask-01-02-hello-world-app-Jinja-Template/flask-02-Jinja_Template/templates/index.html
wget -P templates/ https://raw.githubusercontent.com/<username>/<repo>/main/flask-01-02-hello-world-app-Jinja-Template/flask-02-Jinja_Template/templates/body.html

# Run app
sudo python3 jinja.py
```

***

## 🧠 Code Walkthrough

**jinja.py**
```python
from flask import Flask, render_template
app = Flask(__name__)

@app.route('/')
def head():
    return render_template('index.html', number1=12, number2=15)

@app.route('/mult')
def mult():
    num1, num2 = 3027, 15
    return render_template('body.html', value1=num1, value2=num2, value3=num1*num2)

if __name__=="__main__":
    app.run(host='0.0.0.0', port=80)
```

***

## 🎓 Skills Demonstrated

| Domain         | Skills                              |
| -------------- | ----------------------------------- |
| Programming    | Python, Flask, Jinja2               |
| Cloud          | AWS EC2, SSH, Linux, Security Groups|
| DevOps         | Automation, Deployment, Bash        |
| Versioning     | Git & GitHub                        |
| Documentation  | Markdown, Screenshots, Code comments|

***

## ⚔️ Challenges & Solutions

| Challenge           | Root Cause               | Solution                     |
| ------------------- | ------------------------| ---------------------------- |
| TemplateNotFound    | Files outside /templates | Move HTML to correct folder  |
| wget Mispath        | Folder not created       | Use mkdir -p templates       |
| Port 80 Denied      | Requires root            | Run with sudo                |
| Missing jinja.py    | Wrong directory          | Check pwd, re-download       |

***

## 🔮 Future Improvements

- Add CSS / Bootstrap UI
- Integrate SQLite or PostgreSQL
- Use Gunicorn + Nginx for production
- Add HTTPS, CI/CD (GitHub Actions)
- Dockerize for scalable deployment

***

## 📊 Project Statistics

| Metric         | Value           |
| -------------- | --------------- |
| Python LOC     | ~30             |
| HTML LOC       | ~50             |
| Total Files    | 3               |
| Routes         | 2               |
| Screenshots    | 16              |
| Cloud Provider | AWS (us-west-2) |
| Instance       | t3.micro        |
| Deployment Time| ~30 min         |

***

## 📚 Resources

- https://flask.palletsprojects.com
- https://jinja.palletsprojects.com
- https://docs.aws.amazon.com/ec2/
- https://docs.python.org/3

***

## 📂 File Structure Reference

```plaintext
flask-sql-aws-project/
├── README.md
├── flask-01-02-hello-world-app-Jinja-Template/
│   └── flask-02-Jinja_Template/
│       ├── jinja.py
│       └── templates/
│           ├── index.html
│           └── body.html
└── screenshots/
```

***

## ⚡ Quick Start Commands

**Local**
```bash
git clone https://github.com/LaxmanByte/flask-sql-aws-project.git
cd flask-sql-aws-project/flask-01-02-hello-world-app-Jinja-Template/flask-02-Jinja_Template
pip install flask
python jinja.py
```

**AWS EC2**
```bash
ssh -i "your-key.pem" ec2-user@your-ec2-dns
sudo yum install -y python3 pip wget
pip3 install flask
mkdir -p templates
wget <file_urls>
sudo python3 jinja.py
```

***

## 📞 Connect With Me

**LinkedIn:** https://www.linkedin.com/in/laxman-barre-073735256  
**GitHub:** https://github.com/LaxmanByte

***

<div align="center">

⭐ If you found this project helpful, please star the repo!  
 ❤️ by Laxman — From Code to Cloud**

</div>
```

