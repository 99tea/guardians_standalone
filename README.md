# 🛡️ Comnect Guardians

> Gamified **multi-tenant** cybersecurity awareness and training platform for corporate environments.

![Django](https://img.shields.io/badge/django-framework-092E20.svg)
![Python](https://img.shields.io/badge/python-3.x-blue.svg)
![Multi-Tenant](https://img.shields.io/badge/architecture-multi--tenant-purple.svg)

## 📌 About

**Comnect Guardians** is a gamified cybersecurity awareness and training platform built for companies. It transforms information security education into a practical, competitive, and engaging experience, with **complete data isolation and rankings per organization and department**.

The platform combines tactical minigames, a class/progression system, an in-game economy, daily missions, and isolated leaderboards — turning security training into something employees actually want to do.

## 🚀 Key Features

### 🏢 Corporate Multi-Tenant Architecture

- **Interdepartmental Competition:** Employees earn points for both their individual ranking and their department's average/total within the company.
- Full data isolation per organization and department.

### 🎮 Minigames & Tactical Challenges

- **Quiz Simulations (`/minigames/quiz/:id/play`):** Phishing & Social Engineering, Password Management & MFA, and Network Security/Cryptography scenarios, with time limits and dynamic reward calculation.
- **Password Vault (`/minigames/cofre`):** Interactive challenge for creating strong passwords based on progressive complexity rules.
- **Decrypt (`/minigames/decriptar/play`):** Minigame for decoding technical terms and cybersecurity concepts, with hints and time control.
- **LogScan (`/minigames/logscan/play`):** Tactical word-search focused on quickly identifying threats in log matrices.
- **Daily Patrol:** Quick challenge integrated into the main dashboard for daily XP and coin collection.

### ⚔️ Progression, Classes & Economy

- **Class System:** Choose between **Guardian**, **Analyst**, **Sentinel**, and **Ethical Hacker**, each with exclusive perks (extra time, forensic XP bonus, offensive multiplier, or coin bonus).
- **Shop & Inventory (`/loja`):** Buy, sell, and reroll the catalog, and use **Passive** items (e.g., *128-Core CPU*, *Cold Wallet*, *Layer 7 Firewall*) and **Consumables** (e.g., *Overclock Injector*, *Memory Backup*).
- **Daily Missions, Streak & Achievements:** Track daily goals, certification levels, and automatic achievement unlocks.
- **Rankings (`/rankings`):** Company-isolated leaderboards filterable by XP, Coins, and Streak, plus a department ranking.
- **Training Center & Feedback (`/treinamentos`, `/feedback`):** Security glossary, quiz gallery, and a channel for reporting bugs/vulnerabilities with coin rewards.

## 🧱 Project Structure

```
guardians_standalone/
├── apps/                    # Django applications (modules)
├── comnect_guardians/       # Project settings and core config
├── static/                  # Static assets (CSS, JS, images)
├── templates/               # HTML templates
├── manage.py                # Django management entry point
├── requirements.txt         # Python dependencies
└── README.md
```

## 📦 Installation

### Prerequisites

- Python 3.x
- pip
- (Recommended) a virtual environment

### Setup

1. Clone the repository:

```bash
git clone https://github.com/99tea/guardians_standalone.git
cd guardians_standalone
```

2. Create and activate a virtual environment:

```bash
python -m venv venv
source venv/bin/activate      # Linux/macOS
venv\Scripts\activate         # Windows
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Apply database migrations:

```bash
python manage.py migrate
```

5. Create a superuser (admin access):

```bash
python manage.py createsuperuser
```

6. Run the development server:

```bash
python manage.py runserver
```

7. Access the platform at `http://127.0.0.1:8000/`.

## 🎯 Usage Overview

| Area | Route | Description |
|------|-------|-------------|
| Dashboard | `/` | Daily patrol, streak, and progress overview |
| Quizzes | `/minigames/quiz/:id/play` | Scenario-based security quizzes |
| Password Vault | `/minigames/cofre` | Strong password creation challenge |
| Decrypt | `/minigames/decriptar/play` | Technical term decoding minigame |
| LogScan | `/minigames/logscan/play` | Threat-hunting word search |
| Shop | `/loja` | Buy/sell/reroll items |
| Rankings | `/rankings` | Individual and department leaderboards |
| Trainings | `/treinamentos` | Glossary and quiz gallery |
| Feedback | `/feedback` | Bug/vulnerability reporting |

## 🛠️ Tech Stack

- **Framework:** Django (Python)
- **Architecture:** Multi-tenant, with per-organization and per-department data isolation
- **Frontend:** Django templates + static assets

## 📝 Notes

- This is a **standalone** deployment — each instance serves its own tenant set unless extended.
- Data isolation between companies and departments is a core design principle; review tenant scoping carefully when extending models.
- The repository does not currently include a LICENSE file — add one if you plan to distribute or open-source it.

## 👤 Author

Developed by **99tea**
