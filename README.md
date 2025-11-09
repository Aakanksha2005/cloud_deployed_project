# 🚖 TransVahan — Smart Campus Shuttle Management System

**TransVahan** is a full-stack, real-time campus shuttle platform connecting **Users**, **Drivers**, and **Administrators**.  
It provides live shuttle tracking, route editing, occupancy analytics, and predictive ETAs — built using Node.js, React, React Native, Firebase, AWS, and Terraform.

---

## 🧭 Project Overview

| Module | Description |
|--------|-------------|
| **Backend** | Node.js + Express + Firebase + WebSocket for APIs & live updates |
| **Admin Portal** | React + Vite dashboard for managing routes, vehicles, and drivers |
| **User App** | React Native + Expo mobile app (EAS-built APK) |
| **Infra** | Terraform + AWS (ECR, App Runner, S3 hosting) |

---

## ⚙️ 1. Prerequisites

Install the following tools (latest stable versions recommended):

| Tool | Purpose | Command |
|------|----------|---------|
| **Node.js** (≥ 20) | For backend & frontend builds | `sudo apt install nodejs npm` |
| **Docker** | For backend containerization | [Install Guide](https://docs.docker.com/get-docker/) |
| **AWS CLI v2** | To interact with AWS ECR/AppRunner/S3 | [AWS CLI Install](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html) |
| **Terraform (≥1.6)** | Infrastructure provisioning | `sudo apt install terraform` |
| **Expo CLI + EAS CLI** | For React Native APK builds | `npm install -g expo-cli eas-cli` |
| **Git** | Version control | `sudo apt install git` |

---

## 🌍 2. Repository Setup

```bash
# Clone repo
git clone -b <add_branch_name> --single-branch https://github.com/skmanoj2006/StormCrafters.git
cd StormCrafters


# 1) Backend env
cp backend/.env.example backend/.env
# edit backend/.env and fill real secrets

# 2) Admin portal env
cp admin-portal/.env.example admin-portal/.env
# later, set VITE_API_BASE after backend URL is known

# 3) Mobile app env
cp transvahan-user/.env.example transvahan-user/.env
# later, set API_BASE_URL + WS_URL after backend URL is known



