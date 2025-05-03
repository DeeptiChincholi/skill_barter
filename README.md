# Skill Barter Platform

A web application that allows users to exchange skills with one another. Users can register, create a profile, list the skills they can teach, and the skills they want to learn. They can then search for users who can teach them a given skill—and connect if there’s mutual benefit.

---

## 🛠 Tech Stack

- **Backend:** PHP 7+  
- **Database:** MySQL (via XAMPP)  
- **Frontend:** HTML5, CSS3, JavaScript  
- **Icons:** Font Awesome  
- **Server:** Apache (bundled with XAMPP)

---

## ⚙️ Features

1. **User Authentication**  
   - Secure registration & login with `password_hash()`.  
2. **Profile Management**  
   - View & edit full name, skills you can teach, skills you want to learn, and bio.  
3. **Skill Search & Matching**  
   - Search **any** skill.  
   - Show only users who **teach** that skill.  
   - Show “Connect” button **only if** you can teach them one of **their** desired skills.  
   - Otherwise display:  
     > “They can teach you `<skill>`, but you have nothing they want yet.”  
4. **Email Connection**  
   - One‑click `mailto:` link to start the barter conversation.  
5. **Responsive Design**  
   - Mobile‑first layout for all device sizes.

---

## 📂 Project Structure

/skill-barter/  
├── db.php # Database connection  
├── home.php # Landing page  
├── register.php # User registration  
├── login.php # User login  
├── logout.php # User logout  
├── profile.php # View & edit profile  
├── search.php # Skill search & matching  
├── style.css # Site-wide styles  
└── README.md # Project documentation  

---

## 📝 Setup Instructions

### Prerequisites
1. **XAMPP** (or similar) installed.  
2. **MySQL** running with a user that can create databases.

### Installation
1. Clone or download this repo into your XAMPP **`htdocs/skill-barter/`** folder.  
2. Start **Apache** and **MySQL** in the XAMPP Control Panel.

### Database Setup
1. Open **phpMyAdmin** (`http://localhost/phpmyadmin`).  
2. Create a database named `skill_barter`.  
3. In **phpMyAdmin → SQL**, run your table‑creation script (example below):

CREATE TABLE users (
  id INT AUTO_INCREMENT PRIMARY KEY,
  full_name VARCHAR(255) NOT NULL,
  email VARCHAR(255) NOT NULL UNIQUE,
  password VARCHAR(255) NOT NULL,
  skills TEXT NOT NULL,
  desired_skills TEXT NOT NULL,
  bio TEXT
);

### In db.php, confirm your credentials:

$host = "localhost";  
$user = "root";  
$pass = "";  
$db   = "skill_barter";

### 🚀 Running the App
1. Visit http://localhost/skill-barter/home.php in your browser.  
2. Register a new user, then log in.  
3. Build your profile, then use the Search page to find barter partners.

---

### 📑 License
This project is open‑source under the MIT License.
