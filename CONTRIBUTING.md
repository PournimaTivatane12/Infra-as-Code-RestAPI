# Contributing to Infra-as-Code-RestAPI

Thank you for your interest in contributing to **Infra-as-Code-RestAPI**.  
This project is focused on building a REST API that interacts with cloud infrastructure using Infrastructure as Code (IaC) principles. Contributions of any form—code, documentation, suggestions, or testing—are welcome.

---

## 🛠 Ways to Contribute

You can help this project in several ways:

| Type of Contribution         | How to Help                                                                 |
|-----------------------------|------------------------------------------------------------------------------|
| 🐛 Report Bugs               | Open an issue with steps to reproduce and logs                             |
| 💡 Suggest Features         | Open a feature request issue                                                |
| 🧩 Add New Features         | Fork > Branch > Pull Request                                                |
| 🧽 Improve Code             | Refactor, improve structure, or remove duplication                          |
| 📚 Improve Documentation    | Update README, examples, or code comments                                   |
| ✅ Add Test Cases           | Increase test coverage                                                      |

---

## ✅ Project Tech Stack

| Layer                 | Technology Used                          |
|----------------------|-------------------------------------------|
| API Backend          | Python + Flask                            |
| Infrastructure as Code | Terraform                               |
| Cloud Provider       | AWS (Planned)                             |
| Version Control      | Git & GitHub                              |

---

## 📌 Before You Start

1. Check for open issues before creating new ones.
2. Use clear titles and detailed descriptions.
3. Follow the coding and commit guidelines below.
4. Be respectful and follow the Code of Conduct.

---

## 🚀 Local Development Setup

```bash
# Clone the repository
git clone https://github.com/PournimaTivatane12/Infra-as-Code-RestAPI.git
cd Infra-as-Code-RestAPI

# Set up Python environment
cd api
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate
pip install -r requirements.txt
flask run

# Terraform setup
cd ../infra
terraform init
terraform validate
terraform plan
