# 🦷 Dentso

### Cross-Platform Dental Clinic Management & Communication System

Dentso is a cross-platform dental clinic management ecosystem designed to connect **patients, dentists, and clinic administrators** through a unified digital platform.

The system combines **mobile applications, a web-based administration platform, cloud infrastructure, real-time communication, AI-powered assistance, and machine learning** to modernize dental clinic workflows and improve patient engagement.

> 🎓 Developed as my Bachelor’s Thesis in Computer Science at the German Jordanian University.

---

## 📱 Project Overview

Dentso consists of three interconnected interfaces:

* **Patient Mobile Application** — appointments, communication, AI assistance, notifications, treatment information, and X-ray results.
* **Doctor Mobile Application** — schedules, patient communication, notifications, and clinic expense management.
* **Administrator Web Platform** — patient and appointment management, billing, financial analytics, AI/ML tools, communication management, and system configuration.

All three interfaces are connected through a cloud-based backend and shared data layer.

---

## ✨ Key Features

### 📅 Appointment Management

Patients can browse available time slots, book appointments, cancel or reschedule visits, and receive automated reminders through push notifications and SMS.

### 💬 Real-Time Communication

A real-time chat system enables communication between patients, dentists, and clinic staff, with role-based access, typing indicators, read receipts, and push notifications.

### 🦷 Interactive Dental Chart

Dentists can visually record and manage a patient's dental status and treatment history through an interactive dental chart, including drag-and-drop functionality.

### 🤖 AI Dental Assistant

Dentso integrates a GPT-3.5-powered chatbot directly into the patient application.

The chatbot can provide clinic-specific information by dynamically incorporating details configured by administrators, such as:

* Clinic working hours
* Treatment pricing
* Staff names and specialties
* Appointment information
* Clinic-specific policies

This allows the chatbot to provide context-aware responses rather than relying solely on generic information.

### 🩻 AI-Assisted Dental X-Ray Analysis

An experimental **YOLOv8-based computer vision model** is integrated into the administrator platform to analyze panoramic dental X-rays.

The model detects:

* **Dental caries**
* **Impacted teeth**

Detected areas are visualized directly on the X-ray using bounding boxes and confidence scores, providing dentists with an additional decision-support tool.

> ⚠️ The ML component is an experimental decision-support feature and is **not intended to replace professional clinical diagnosis**.

### 💳 Billing & Financial Analytics

The administrator platform includes billing and financial management functionality with:

* Invoice generation
* Income tracking
* Expense tracking
* Visual financial analytics
* Date-based filtering

---

# 📸 Project Showcase

## Patient Mobile Application

The patient application provides a centralized interface for appointments, communication, notifications, and access to dental information.

![Dentso Mobile Application](screenshots/mobile-home.png)

---

## 🤖 AI Dental Assistant

Patients can interact with the integrated AI assistant to receive instant answers to common clinic-related questions.

![Dentso AI Chatbot](screenshots/ai-chatbot.png)

---

## 🦷 Interactive Dental Chart

The interactive dental chart allows dental professionals to visually manage tooth conditions and treatments through an intuitive interface.

![Dentso Dental Chart](screenshots/dental-chart.png)

---

## 🩻 ML-Powered X-Ray Analysis

Panoramic dental X-rays can be processed through the integrated YOLOv8 model, with detected conditions highlighted directly on the image.

![Dentso X-Ray Diagnosis](screenshots/xray-diagnosis.png)

---

# 🏗️ System Architecture

Dentso follows a modular, cloud-based architecture connecting the patient mobile application, doctor mobile application, and administrator web platform.

**Core infrastructure:**

* **Flutter** — Cross-platform frontend development
* **Firebase Cloud Firestore** — Real-time NoSQL database
* **Firebase Authentication** — User authentication
* **Firebase Cloud Functions** — Server-side operations and automation
* **Firebase Cloud Messaging (FCM)** — Push notifications
* **Cloudinary** — Dental image and X-ray storage
* **OpenAI GPT-3.5** — AI chatbot
* **YOLOv8** — Panoramic X-ray analysis
* **SMS API** — Appointment reminders

The architecture was designed around real-time synchronization, role-based access control, scalability, and integration with external services.

---

# 🔐 Security & Access Control

Dentso uses **role-based access control (RBAC)** to separate permissions between patients, doctors, and administrators.

Examples include:

* Patients can only access their own records and conversations.
* Doctors can access patients assigned to them.
* Administrators have broader management permissions.
* Firestore security rules restrict unauthorized data access.
* Sensitive dental images are managed through controlled Cloudinary access.

---

# 🛠️ Technology Stack

| Category           | Technologies                       |
| ------------------ | ---------------------------------- |
| Frontend           | Flutter, Dart                      |
| Backend & Database | Firebase, Cloud Firestore          |
| Authentication     | Firebase Authentication, OAuth 2.0 |
| Cloud Functions    | Firebase Cloud Functions           |
| Image Management   | Cloudinary                         |
| AI                 | OpenAI GPT-3.5                     |
| Machine Learning   | YOLOv8                             |
| Notifications      | Firebase Cloud Messaging, SMS API  |
| UI/UX              | Figma                              |

---

# 🧪 Testing & Evaluation

The system was evaluated through functional testing, integration testing, and user acceptance testing.

The tested modules included:

* Appointment booking
* Real-time chat
* Billing and analytics
* AI chatbot
* ML-based X-ray analysis

## All major functional tests reported in the thesis passed. The YOLOv8 model achieved an average precision of **82% for caries** and **88% for impacted teeth** on the project's small validation set.

# 🎯 Project Highlights

Dentso brought together several areas of software engineering into a single end-to-end system:

* Cross-platform mobile and web development
* Cloud-based backend architecture
* Real-time data synchronization
* Role-based access control
* Real-time communication
* AI integration
* Computer vision / machine learning
* Cloud image management
* Automated notifications
* Financial analytics
* User-centered UI/UX design

---

# 🔮 Future Development

Potential future improvements include:

* Training a custom YOLOv8 model on a larger and more diverse dataset
* Expanding detection to additional dental conditions
* Adding patient oral-health progress tracking
* Improving accessibility and mobile UI features
* Deploying and evaluating the system in a real clinical environment

---


---

> 🔒 **Source Code**
>
> The source code for Dentso is kept private. This repository serves as a public project showcase containing selected screenshots and technical documentation.
