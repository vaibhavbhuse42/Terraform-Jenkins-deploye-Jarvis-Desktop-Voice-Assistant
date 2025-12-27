# 🤖 Jarvis Desktop Voice Assistant – CI/CD Deployment using Terraform & Jenkins

## 📌 Project Overview

This project demonstrates **end-to-end automation** of a Python-based **Desktop Voice Assistant (Jarvis)** using **Terraform for infrastructure provisioning** and **Jenkins for CI/CD deployment** on **AWS EC2**.

The goal of this project is to showcase **DevOps skills** by combining:

* Infrastructure as Code (IaC)
* Continuous Integration & Deployment
* Linux service management (systemd)
* Python automation

---

## 🚀 Tech Stack Used

| Category        | Tools / Technologies       |
| --------------- | -------------------------- |
| Cloud           | AWS (EC2, Security Group)  |
| IaC             | Terraform                  |
| CI/CD           | Jenkins                    |
| OS              | Ubuntu Linux               |
| Language        | Python 3                   |
| Voice Libraries | pyttsx3, SpeechRecognition |
| Automation      | systemd, shell scripting   |
| Version Control | Git & GitHub               |

---

## 🧠 About Jarvis Voice Assistant

Jarvis is a Python-based desktop voice assistant that can:

* 🕒 Tell current **time & date**
* 🔍 Search **Wikipedia**
* 🎵 Play **music**
* 🌐 Open **Google / YouTube**
* 📸 Take **screenshots**
* 😂 Tell **jokes**
* 🔄 Restart / Shutdown system
* 🧑‍💻 Change assistant name dynamically

The assistant uses **speech recognition** for input and **text-to-speech** for responses.

---

## 🏗️ Infrastructure Provisioning (Terraform)

Terraform is used to automate AWS resource creation:

### Resources Created:

* ✅ AWS EC2 Instance (Ubuntu)
* ✅ Security Group with required ports:

  * 22 (SSH)
  * 80 (HTTP)
  * 443 (HTTPS)
  * 5000, 8000, 8080, 9000 (App usage)

### Terraform Flow:

```bash
terraform init
terraform plan
terraform apply
```

---

## 🔐 Security Group Configuration

Inbound rules allow traffic for:

* SSH access
* Web services
* Jenkins & application ports

Outbound traffic is allowed to all destinations.

---

## 🔄 CI/CD Pipeline using Jenkins

Jenkins automates **build, transfer, dependency installation, and service restart**.

### Jenkins Pipeline Stages:

1. **Checkout Source Code** from GitHub
2. **Package & Transfer Code** to EC2 using `rsync`
3. **Setup Python Virtual Environment**
4. **Install Dependencies**
5. **Create / Update systemd Service**
6. **Restart Jarvis Service & Verify Logs**

---

## ⚙️ systemd Service Configuration

Jarvis runs as a background Linux service:

* Auto-restart on failure
* Uses Python virtual environment
* Logs stored for debugging

Service name:

```bash
jarvis.service
```

---

## 🧪 How Deployment Works (Flow)

1. Developer pushes code to GitHub
2. Jenkins pipeline triggers automatically
3. Code is copied to EC2 server
4. Dependencies are installed inside venv
5. systemd service is updated
6. Jarvis assistant runs automatically

---

## 📸 Screenshots Section (Add Your Screenshots Here)

> 📷 **Add screenshots after running the project**

### Suggested Screenshots:

* Terraform `apply` output
* AWS EC2 instance running
* Jenkins pipeline success
* systemd service status
* Jarvis application logs


![](/img/Screenshot%20(68).png)
![](/img/Screenshot%20(65).png)
![](/img/Screenshot%20(66).png)
![](/img/Screenshot%20(70).png)
![](/img/Screenshot%20(69).png)
![](/img/Screenshot%20(67).png)


## 🏛️ Architecture Diagram


![](/img/unnamed.png)


### Architecture Explanation:

* Developer pushes code to GitHub
* Jenkins pulls code and executes pipeline
* Terraform provisions AWS infrastructure
* Jenkins deploys application to EC2
* Jarvis runs as a Linux service


## ✅ Project Highlights

* ✔ Fully automated infrastructure
* ✔ CI/CD pipeline with Jenkins
* ✔ Infrastructure as Code (Terraform)
* ✔ Production-like Linux service setup
* ✔ Real-world DevOps workflow



## 🧑‍💻 Author

**Vaibhav Navnath Bhuse**
🚀 DevOps Enthusiast | Cloud | Automation | CI/CD



## 📌 Conclusion

This project demonstrates a **real-world DevOps deployment** where infrastructure provisioning, application deployment, and service management are fully automated. It is a strong example of how **Terraform + Jenkins** can be used together to deploy Python applications efficiently and reliably.



⭐ If you like this project, don’t forget to star the repository!
