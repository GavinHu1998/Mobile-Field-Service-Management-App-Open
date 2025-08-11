# 📄 Project Proposal: Mobile Field Service Management App

🔗 [Demo Vedio](https://drive.google.com/file/d/1m0C3A5NL_mA8XTFI_Qmb_H4Lm_tfOSLW/view?usp=drive_link)

## Project Overview
This project proposes the development of a mobile Field Service Management (FSM) application built using **React Native + Expo**. The goal is to streamline job scheduling, assignment, and real-time updates for cleaning and maintenance services, specifically tailored for **Services Pro**, a Canadian field service provider.

---

## 🧩 Core Features

### 1. **Authentication & Secure Storage**
- **Login Screen** using `SecureStore` to persist sensitive credentials.
- Token-based authentication handled securely, with error validation.
- Conditional navigation based on token existence.

### 2. **Dashboard with Filtering**
- Fetches jobs dynamically from `https://us-west-1c.zuperpro.com/api/jobs`.
- Supports filtering by creation date (`ASC`, `DESC`, `All`).
- Renders job cards with:
  - Title, creation date, customer name
  - Assigned worker (or shows "Assign to" button if none)
  - Navigation to job details

### 3. **Job Details View**
- Displays full job information including:
  - Category, schedule, customer contact, address
  - Status, creator, invoicing state
- Allows deletion of jobs via confirmation dialog
- Secure API calls using stored token

### 4. **Create Job Entry**
- Form-based interface with:
  - Job title, description, service category (radio options)
  - Customer info and address
  - Date pickers for scheduling
- Token check and validation prior to submission
- Uses `simulate=true` endpoint for test submission

### 5. **User Profile Screen**
- Displays logged-in user’s name, email, role, and avatar
- Offers dynamic login/logout
- Includes external links to company’s site and subpages

### 6. **Navigation System**
- Bottom tab navigation using `expo-router`
- Tabs: Dashboard, Add Job, Profile
- Hidden tabs: Login (Index), Job Detail

---

## 🔧 Tech Stack

| Layer        | Technology         |
|--------------|-------------------|
| **Frontend** | React Native (Expo) |
| **Navigation** | expo-router + @react-navigation |
| **State & Storage** | React hooks + expo-secure-store |
| **UI** | React Native components + custom styles |
| **API** | REST API (ZuperPro endpoint) |

---

## 🎯 Target Users
- Field technicians
- Operations managers
- Customer support teams

---

## ✅ Project Goals
- Replace manual job tracking with a mobile-first solution
- Improve service response time and reduce scheduling errors
- Provide real-time updates and access to job data
- Enable secure login/logout and user-based customization

---

## 📦 Deliverables
- Fully functional React Native mobile app
- Login/Auth + CRUD operations for jobs
- Filtering and sorting support
- Persistent user sessions
- Clean UX optimized for mobile workflows

---

## 📈 Future Enhancements
- Push notifications
- Role-based access control (admin vs. technician)
- Map integration for job address visualization
- Offline mode for field technicians
