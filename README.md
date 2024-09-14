# Quiz Titan
Quiz Titan is a dynamic trivia game that pulls questions from the Open Trivia
Database (OpenTDB) or uses pre-recorded fallback questions. The game allows
players to select difficulty levels, answer multiple-choice questions, and
track scores across multiple rounds.

## Table of Contents
+ Installation
+ Setup and Configuration
+ Teck Stack
+ Features

## Installations
### Prerequisites
Ensure you have the following installed on your system
+ Python 3.x
+ Virtualenv
+ Git

### Steps
**1. Clone the Repository**
 ```bash
  git clone https://github.com/Yemisi-jay/Quiz-Titan.git
  cd quiz-titan
  ```

**2. Create and Activate Virtual Environment**
 ```bash
  python3 -m venv .venv
  source .venv/bin/activate <-- For Linux/Mac -->
  .venv\Scripts\activate <-- For windows -->
 ```
**3. Install Dependencies:**
   Use the `requirements.txt` file to install the necessary packages:
 ```bash
 pip install -r requirements.txt
 ```
**4. Setup the Database**
    Perform initial migrations to set up the database schema:
 ```bash
 python manage.py migrate
 ```
**5. Create a Superuser (Admin Access):**
   Create an admin user to manage the game via the Django Admin panel:
 ```bash
 python manahe.py createsuperuser
 ```
**6. run the Development Server:**
 ```bash
 python manage.py runsever
 ```
**7. Access the Game:**
+ Visit `http://127.0.0.1:8000` to start the game.
+ Admin panel: `http://127.0.0.1:8000/admin` for managing players and scores.
    
## Setup and Configuration
**1. Database Configuration:** By default, the project uses SQLite as its
database. If you wish to use another database (e.g. PostgreSQL), update the
`DATABASES` setting in `settings.py`.

**2. OpenTDB API Configuration:** Questions are fetched from the Open Trivia
Database API. The default endpoint is configured in `views.py`.

**3. Fallback Questions:** If the API fails, the game will load pre-recorded
questions from a local `fallback_questions.json` file located in `data/`.
you can modify or add more questions to this file

## Teck Stack
**Backend:**
+ Django 5.1.1 (Pyton-based web framework)
+ SQLite (default database)

**Frontend**
+ HTML
+ CSS
+ JavaScript

**Third-Party APIs:**
+ Open Trivia Database API for fetching trivia questions

## Features
+ Game Fetches trivia questions from OpenTDB API.
+ Players can select genres and difficulty levels.
+ Tracks player scores across rounds.
+ Fallback system to load local questions if API fails.
+ Admin interface to manage players and scores.
+ Responsive design.


