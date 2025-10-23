# ⚡ ChargeHub Berlin

**Advanced Software Engineering – Final Project** 

## 📘 Overview

**ChargeHub Berlin** is a web application designed to **manage and visualize electric-vehicle charging stations across Berlin**.  
It enables users to search, rate, and comment on charging stations, helping to build a community-driven overview of the city’s charging infrastructure.

The project applies **Domain-Driven Design (DDD)** and **Test-Driven Development (TDD)** principles.

---

## 🚀 Key Features

- 🔐 **User Authentication** — Secure user registration and login  
- 🗺️ **Interactive Map** — Visualization of Berlin’s charging stations and district densities using **Folium + Leaflet.js**  
- 🔎 **Station Search** — Filter and locate charging stations by district or location  
- 💬 **User Reviews & Ratings** — Registered users can add, edit, and view comments  
- 🧩 **Data Integration** — Combines geospatial datasets, user content, and authentication into one platform  

---

## 🧱 Domain Logic & Objectives

1. **User Login / Registration** — enables personalized access and review tracking  
2. **Add Rating / Comment** — allows sharing user feedback to enhance service quality  
3. **View Rating / Comment** — provides insight into charging-station reliability  

---
## 🛠️ Technology Stack

| Category | Technologies |
|-----------|--------------|
| **Language** | Python |
| **Backend Framework** | Flask |
| **Frontend** | HTML, CSS, JavaScript, HTMX |
| **Visualization** | Folium, Leaflet.js |
| **Database** | SQLite |
| **Testing** | pytest + coverage |
| **Version Control** | Git / GitHub |
| **Dependency Mgmt.** | pip |
| **IDE** | VS Code |
| **Caching** | flask-caching |

---
## 🧩 Architecture (DDD Layers)

```bash
app/
├── domains/          # Entities, Events, Value Objects
├── models/           # Database Models
├── repositories/     # Data Access Logic
├── routes/           # Flask Routes (HTTP Handlers)
├── static/           # CSS & JS Files
├── templates/        # HTML Templates
└── datasets/         # Input Data (CSV / GeoJSON)
tests/                # Unit & Integration Tests
```

- **Domain Layer:** Core business logic (`User.py`, `ChargingStation.py`, `Review.py`)  
- **Infrastructure Layer:** Persistence & repositories  
- **Application Layer:** REST endpoints (`auth.py`, `map.py`, `reviews.py`)  
---

## 🧪 Testing & TDD

- Implemented **pytest** for unit and integration testing  
- Achieved **~84 % test coverage** using **coverage.py**  
- Tests organized by component: repositories, routes, entities, value objects  
- Example domains/events:  
  - `accountCreated.py` | `accountLoggedIn.py` | `reviewAdded.py`

---

## 🖥️ User Interface

- Interactive map with clickable charging-station markers  
- Login / Register pages for user authentication  
- Add-Review and Review-List pages  
- Responsive layout (desktop + mobile)

**Front-End Libraries:** HTML + CSS + JavaScript + HTMX + Leaflet.js + Font Awesome

---

## 🌍 Datasets Integration

Integrated the following datasets for Berlin:

- `Ladesaeulenregister_SEP.xlsx` — detailed charging-station data  
- `geodata_berlin_dis.csv` — district-level polygon boundaries  

These datasets are cleaned and merged to visualize station distribution.

---

## 🤖 LLM Integration

LLMs were used to assist with:

| Task | Tools |
|------|--------|
| Code Generation & Optimization | DeepSeek |
| Test Idea Brainstorming | ChatGPT |
| Documentation Formatting (LaTeX) | Gemini |

Examples:
- **Test Case Generation:** automatic ideas for authentication & search tests  
- **Code Optimization:** improved filtering logic for district-based queries  

---

## ⚙️ Technical Challenges & Solutions

| Challenge | Solution |
|------------|-----------|
| Lack of isolated testable code | Refactored into DDD bounded contexts |
| Git merge conflicts | Structured branch workflow + regular syncs |
| Streamlit → Flask migration | Rebuilt map features with Folium & clean datasets |
| Team coordination | Regular meetings & shared coding standards |

---

## 🏁 Project Completion & Lessons Learned

- Delivered all **core functionalities** and **documentation**  
- Practiced **DDD & TDD** for maintainability  
- Learned effective **team collaboration**, **testing discipline**, and **LLM-assisted development**  
- Strengthened understanding of **Flask architecture** and **geospatial visualization**

---

## 📂 Repository Structure & Usage

```bash
# Clone repository
git clone https://github.com/the5avage/se_project.git
cd se_project

# Install dependencies
pip install -r requirements.txt

# Run the Flask app
python app.py

# Run tests
pytest --cov=app
```
---
Authors: *Shadi Farzankia, Farel Arden, Rene Heldmaier, Hameez Ahmad*  
Date: *14 January 2025*  
