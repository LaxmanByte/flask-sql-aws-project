Flask Hello World + Jinja Templates
My First Flask Web Application – From Local Development to AWS Deployment
Project Goal: Learn Flask framework fundamentals and deploy a production-ready web application to AWS EC2
Completion Date: October 2025
Status: Successfully Completed and Deployed

Table of Contents

About This Project

What I Learned

Technical Implementation

Part 1: Understanding Flask Framework

Part 2: Hello World Application

Part 3: Jinja Template Integration

Part 4: AWS EC2 Deployment

Challenges and Solutions

Project Structure

How to Run

Technologies Used

About This Project
I built this project to gain hands-on experience with Flask web framework and cloud deployment. This demonstrates my ability to:

Develop Python web applications using Flask framework

Implement dynamic templates with Jinja2 templating engine

Deploy to AWS cloud on EC2 instances

Manage code with Git version control

Configure Linux servers for web hosting

Document technical work professionally

Key Achievement
Successfully took an application from local development through to production deployment on AWS infrastructure.

What I Learned
Technical Skills Acquired
Skill Area: What I Accomplished

Flask Framework: Built web applications with routing, request handling, and response generation

Jinja2 Templates: Created dynamic HTML pages that render data from Python backend

AWS EC2: Launched, configured, and deployed applications to cloud Linux servers

Linux Administration: Managed Amazon Linux 2 instances, installed packages, configured services

Git and GitHub: Version controlled my code and used GitHub as deployment source

Client-Server Architecture: Understood request/response cycle and web application flow

Learning Outcomes Achieved

Understood client-server software architecture

Became familiar with Python Flask framework

Installed Python and Flask on local and remote systems

Built functional web applications with Flask

Used Git for application versioning

Deployed applications to AWS EC2 from GitHub repository

Technical Implementation
Architecture Overview
Browser (Client) sends HTTP requests to Flask App (Python), which handles routes and logic, uses Jinja2 templates for HTML rendering, and sends a response back to the client. The application is deployed on AWS EC2 (Amazon Linux 2).

Development Workflow
Local Development → Git Commit → GitHub Push → AWS EC2 Deployment → Live Application

Part 1: Understanding Flask Framework
Flask is a lightweight Python web framework chosen for its micro-framework approach and ease of learning.
Flask Features Used:

Built-in development server

Jinja2 templating engine

WSGI 1.0 compliance

Integrated debugging

URL routing system

Part 2: Hello World Application
Built a Flask web application with multiple routes:

Static URL routing

Nested route structures

Dynamic URL parameters

Request handling and response generation

hello-world-app.py contains routes for the home page, second page, nested page, and a dynamic page demonstrating URL parameter handling.

Part 3: Jinja Template Integration
Created a Flask application that separates presentation (HTML) from business logic (Python) using Jinja2 templates.
Routes:

Homepage displays a message from Python backend

Calculation route shows the sum of two numbers passed from Python backend to HTML

Project Structure
flask-01-02-hello-world-app-Jinja-Template

README.md (This documentation)

flask-01-hello-world-app

hello-world-app.py (Basic Flask routing application)

flask-02-Jinja_Template

jinja.py (Flask with template rendering)

templates

index.html (Message display template)

body.html (Calculation display template)

How to Run
Prerequisites:

Python 3

pip
Local Development:

Clone repository
git clone https://github.com/LaxmanByte/flask-sql-aws-project.git

Install Flask
pip3 install flask

Run Hello World App
cd flask-01-02-hello-world-app-Jinja-Template/flask-01-hello-world-app
python3 hello-world-app.py
Access at: http://localhost:80

Run Jinja Template App
cd flask-02-Jinja_Template
python3 jinja.py
Access at: http://localhost:5000

AWS EC2 Deployment

Launch EC2 Instance

AMI: Amazon Linux 2

Instance Type: t2.micro

Security Group: SSH (22) and HTTP (80)

Connect via SSH
chmod 400 your-key.pem
ssh -i your-key.pem ec2-user@EC2-PUBLIC-IP

Install Dependencies
sudo yum update -y
sudo yum install python3 git -y
sudo pip3 install flask

Deploy Application
git clone https://github.com/LaxmanByte/flask-sql-aws-project.git
cd flask-sql-aws-project/flask-01-02-hello-world-app-Jinja-Template/flask-01-hello-world-app
sudo python3 hello-world-app.py

Access Application
http://EC2-PUBLIC-IP

Technologies Used
Core Technologies: Python 3, Flask, Jinja2
Cloud Infrastructure: AWS EC2 (t2.micro, Amazon Linux 2), Security Groups
Development Tools: Git, GitHub, SSH, pip, curl

Challenges and Solutions

Solved permission issues by running Flask on port 80 with sudo

Configured AWS security group to allow external HTTP access

Fixed Flask template loading errors by correcting folder structure

Used nohup and systemd for process management when running app on EC2

Key Takeaways

Gained real-world experience in Python Flask development, template integration, cloud deployment, and Linux server management

Developed skills in technical documentation, problem-solving, and best practices

Demonstrated ability to build, deploy, and document web applications professionally

Contact
Laxman Barre
GitHub: https://github.com/LaxmanByte
Project Repository: https://github.com/LaxmanByte/flask-sql-aws-project

Acknowledgments
Flask documentation and community, AWS documentation and tutorials, Python community resources

Last Updated: October 19, 2025
Status: Completed and Deployed

This project demonstrates my ability to build, deploy, and document web applications from scratch in a professional environment.
