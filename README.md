# 🐉 HAUPokemon Mobile App

[![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)](https://flutter.dev)
[![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)](https://aws.amazon.com/)
[![Tailscale](https://img.shields.io/badge/Tailscale-%23FFFFFF.svg?style=for-the-badge&logo=tailscale&logoColor=black)](https://tailscale.com/)

---

## 📱 Project Overview

**HAUPokemon** is a high-performance Flutter mobile application developed for our **6CloudCom Final Project**.  
It brings the world of Pokemon to life using modern UI design, smooth animations, and a secure cloud-powered backend built on AWS infrastructure.

The application integrates mobile development, cloud computing, database systems, and secure networking into one unified platform.

---

## ✨ Key Features

### 🛡️ VPN-Secured Backend
All database and API traffic is securely routed through **Tailscale VPN** to a private AWS EC2 instance.  
This helps keep sensitive data protected and inaccessible from the public internet.

### 🎮 Dynamic Dashboard
A Pokemon-themed dashboard displaying animated Pokemon sprites in a responsive grid layout.

### 📚 Live Monster Library
Pokemon data is retrieved in real time from an **AWS RDS PostgreSQL** database.

### 🗺️ Interactive Map
Custom mapping interface powered by:

- `flutter_map`
- OpenStreetMap

This allows map rendering and navigation features inside the app.

### 🎨 Premium Visual Design

- Pixel-perfect Generation V Pokemon sprites
- Smooth breathing animations
- Custom bottom navigation bar
- Overlapping 3D-style icon transitions
- Consistent themed UI design

### 🎵 Background Music

Looped background music system that:

- Plays continuously
- Persists across navigation screens
- Enhances user immersion

---

## 🛠️ Cloud & Tech Stack

### Frontend

- Flutter (Dart)

Used for building the mobile user interface and application logic.

### Backend Infrastructure

- AWS EC2 (Paris Region)
- Application Load Balancer (ALB)

The EC2 server hosts the backend services and handles API communication.

### Database

- AWS RDS PostgreSQL
- Multi-AZ Deployment
- Region: N. Virginia

Provides:

- High availability
- Data replication
- Automated failover

### Networking

- Tailscale VPN
- AWS VPC Peering
- DuckDNS Domain

Domain used:

haupokemon.duckdns.org

Ensures secure internal communication between services.

### Automation

* AWS Lambda

Used to:

* Automatically start EC2 instances
* Automatically stop EC2 instances
* Reduce infrastructure costs

### Routing & Navigation

Flutter packages used:

* `go_router`
* `flutter_map`

These manage app navigation and map rendering.

---

## 🚀 Getting Started

### ⚠️ Important Requirement

This application **requires connection to the HAUPokemon Tailscale VPN**.

Without VPN access:

* Database connection will fail
* API requests will not work

---

## 📥 Installation Guide

Follow these steps to run the application locally.

### Step 1 — Connect to VPN

Ensure that:

* Tailscale is installed
* You are logged in
* You are connected to the HAUPokemon network

### Step 2 — Clone Repository

Run:

```bash
git clone https://github.com/ciellamher/Pokemon-Hau.git
cd Pokemon-Hau
```

### Step 3 — Install Dependencies

Run:

```bash
flutter pub get
```

This downloads all required Flutter packages.

### Step 4 — Run the Application

Run:

```bash
flutter run
```

The app will build and launch on the connected device.

---

## 📂 Project Structure

```text
lib/
├── core/
│   ├── services/
│   │   ├── audio_service.dart
│   │   ├── api_service.dart
│   │   ├── aws_service.dart
│   │   └── global_services.dart
│   │
│   └── widgets/
│       ├── navbar.dart
│       ├── card_widgets.dart
│       └── background_widgets.dart
│
├── features/
│   ├── auth/
│   │   ├── login_screen.dart
│   │   └── signup_screen.dart
│   │
│   ├── dashboard/
│   │   ├── dashboard_screen.dart
│   │   └── player_stats.dart
│   │
│   ├── map/
│   │   └── map_screen.dart
│   │
│   └── pokemon/
│       ├── pokemon_list.dart
│       └── pokemon_details.dart
│
└── main.dart
```

---

## ☁️ System Architecture Summary

The HAUPokemon application follows a secure cloud architecture:

```text
Mobile App
   ↓
Tailscale VPN
   ↓
AWS EC2 Web Server
   ↓
AWS RDS PostgreSQL Database
```

This architecture ensures:

* Secure communication
* Controlled database access
* Scalable cloud deployment

---

## 🔐 Security Features

* Private VPN-only database access
* No public database exposure
* Secure API communication
* Controlled infrastructure networking
* Cloud resource isolation

---

## ⚙️ Automation Workflow

AWS Lambda functions automatically:

* Start the EC2 server during testing hours
* Stop the EC2 server after usage
* Help optimize cost efficiency

---

## 📊 Performance Optimization

The app is optimized using:

* Efficient API calls
* Cached sprite loading
* Lightweight UI animations
* Persistent audio engine
* Cloud-based database queries

---

## 🧪 Testing Requirements

Before testing the application, make sure these are ready:

* VPN connected
* EC2 running
* Database active
* Flutter dependencies installed

---

## 👥 Development Team

Developed for **6CloudCom**
Under **Sir Ulysses Raymond F. Monsale**

### Team Members

**Jimenez, Graciella Mhervie D.**

Project Manager & Documentation

Responsible for:

* Documentation
* System flow explanation
* Project coordination

**Marquez, Jian Kalel D.**

Mobile Developer (Flutter)

Responsible for:

* UI implementation
* Flutter development
* Navigation system

**Parejas, Arron Kian M.**

Cloud Engineer

Responsible for:

* AWS infrastructure
* Server setup
* Database configuration

**Tongol, Jenica Sarah B.**

UI/UX Designer & App Logic

Responsible for:

* Visual design
* User interface layout
* Interaction logic

---

## 📌 Project Purpose

This project demonstrates:

* Mobile application development
* Cloud infrastructure deployment
* Secure networking implementation
* Database integration
* Modern UI/UX design

All combined into one real-world system.

---

## ❤️ Acknowledgment

Developed with dedication and teamwork
by the **CS-301**

For academic and cloud computing system development.

```
