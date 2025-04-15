# 🎓 Club Management Web Application

A full-stack web application designed to streamline and simplify the management of student clubs at a college. This platform allows students to sign up, log in, join clubs, and explore club-related activities while providing administrative tools for club heads to manage events, galleries, and member requests.

---

## 🚀 Technologies Used

### Frontend
- **HTML5**
- **Bootstrap 5** – for responsive design and styling
- **JavaScript** – for interactivity and dynamic behavior

### Backend
- **Django** – high-level Python web framework for rapid development

### Database
- **MySQL** – integrated with Django's ORM via the Django admin panel

---

## 🗂️ File Structure

### Templates (Frontend HTML Files)
All templates are located in the `templates/` directory:
- `base.html` – Base layout for all pages
- `landing_page.html` – Homepage
- `club_display_page.html` – List of all clubs
- `individual_clubs.html` – Details of a specific club
- `events.html` – Add/View club events
- `login.html` – Member login page
- `signup.html` – User registration page
- `request_to_join.html` – Request form to join a club
- `profile.html` – Member profile with club affiliations

---

## 🧩 Models

The Django app utilizes the following models:

- `Clubs` – Stores details about each club
- `Members` – Stores member data and login credentials
- `JoinRequest` – Handles club membership requests
- `ClubMembership` – Join table linking members and clubs with their roles (Head, Sub-Head, Member)
- `Event` – Club-specific event listings with date, title, description, and images
- `GalleryImage` – Image gallery feature for each club

---

## ✅ Key Features & Advantages

- **Secure Authentication**  
  - Uses hashed passwords for secure login  
  - CSRF protection enabled for all forms  
  - User sessions managed securely

- **User Account System**  
  - Users must **sign up** to create an account  
  - Must **log in** to join, explore, or interact with clubs

- **Role-Based Access Control**  
  - Only **authenticated members** can view club-specific content such as events or merchandise  
  - Club **Heads** and **Sub-Heads** can approve join requests, manage events, and upload gallery images

- **Club Join Requests**  
  - Simple, in-browser join form  
  - Requests go to club admins for review and approval

- **Event Management**  
  - Heads/Sub-Heads can create, view, and manage events  
  - Events are displayed in a clean, date-sorted format

- **Gallery Uploads**  
  - Visual image uploads to showcase past events or achievements

- **User Profile Dashboard**  
  - Displays personal info and current club memberships

- **Interactive & Responsive UI**  
  - Built using Bootstrap for seamless access across devices  
  - Clean, modern layout with fast page load times

- **Extensibility**  
  - Modular architecture allows for future enhancements such as chat, notifications, or club analytics

---

## 🌐 URL Configuration

All routes are defined in `urls.py`. Key endpoints include:
- `/` – Landing page
- `/clubs` – All clubs list
- `/clubs/<club_id>` – Club-specific page
- `/login`, `/signup`, `/profile` – Auth and profile management

---

## ⚙️ Prerequisites & Setup

Before running the project locally, ensure you have the following:

### 1. Install Python (3.x recommended)

### 2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`

