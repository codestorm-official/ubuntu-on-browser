
![Ubuntu](https://img.shields.io/badge/Ubuntu-Latest-E95420?logo=ubuntu)
![Ubuntu](https://img.shields.io/badge/Ubuntu-20.04-E95420?logo=ubuntu)
![Ubuntu](https://img.shields.io/badge/Ubuntu-22.04-E95420?logo=ubuntu)
![Ubuntu](https://img.shields.io/badge/Ubuntu-24.04-E95420?logo=ubuntu)
![Ubuntu](https://img.shields.io/badge/Other-Version-E95420?logo=ubuntu)
![Docker](https://img.shields.io/badge/Railway-Supported-blue?logo=railway)
![Docker](https://img.shields.io/badge/Docker-Supported-blue?logo=docker)

# 🐧 Ubuntu on Browser
**Repository Name:** ubuntu-on-browser

**Template Name:** Ubuntu

[![Deploy on Railway](https://railway.app/button.svg)](https://railway.com/template/ubuntu-on-browser)

## 📖 Description
Want to try out Ubuntu or need a lightweight version of Linux available at all times? 🚀 

This project allows you to deploy a fully functional Ubuntu environment in the cloud, accessible directly via your web browser.

This project utilizes the Ubuntu Docker image to deploy a container that supports most CLI tools. It uses [ttyd](https://github.com/tsl0922/ttyd) to provide a seamless, browser-based terminal experience with built-in security.

![Ubuntu Home](./img/ubuntu_home.png)

---

### ✨ Key Features
- 🐧 **Dynamic Ubuntu Base:** Defaults to the `latest` version, but customizable to any version (20.04, 22.04, 24.04).
- 🔒 **Secure Access:** Password-protected web terminal via Basic Authentication.
- 💻 **Dev-Ready:** Neofetch display on login and pre-installed essential tools.
- 🌐 **Web-Accessible:** Use it from any device with a browser—no SSH client needed.
- 💾 **Persistence Ready:** Easily mount Railway Volumes to save your workspace.

---

## 🛠️ Configuration & Variables

### Environment Variables (Runtime)
Configure these in the **Variables** tab of your Railway dashboard to secure your terminal:

| Variable     | Description                                      |
| :----------- | :----------------------------------------------- |
| **PORT**     | The port on which the ttyd program will listen.  |
| **USERNAME** | The username required to login to the web shell. |
| **PASSWORD** | The password required to login to the web shell. |

### Build Arguments (Dynamic Versioning)
If you want to use a specific Ubuntu version, add this in **Settings > Build > Build Arguments**:

| Argument           | Default  | Description                                                |
| :----------------- | :------- | :--------------------------------------------------------- |
| **UBUNTU_VERSION** | `latest` | Set this to `22.04`, `20.04`, etc., to change the base OS. |

> **⚠️ SECURITY NOTE:** It is strongly advised to set a custom **USERNAME** and **PASSWORD** before deploying to prevent unauthorized access.

---

## 📂 Data Persistence (Recommended)
By default, Railway containers are ephemeral. To save your files permanently:
1. Create a **New Volume** in your Railway project.
2. Mount the volume to your Ubuntu service.
3. Set the **Mount Path** to `/root/workspace`.
4. All files inside this folder will persist even after a re-deploy!

---

## 🚀 Why Deploy on Railway?
- **Instant Access:** Get a Linux terminal from any device in minutes.
- **Zero Setup:** No local installation, VirtualBox, or VM configuration required.
- **Testing Ground:** Perfect for learning Linux, testing scripts, or running Python automation.
- **Modern Infrastructure:** Automatic HTTPS/SSL and easy resource scaling.

## 🤝 Common Use Cases
- Testing shell scripts and automation workflows.
- Learning Linux command-line basics in a safe sandbox.
- Remote development environment for lightweight coding.
- Package and dependency testing for IT Middleware tasks.

---

## 📦 Tech Stack & Dependencies
- **Base OS:** Ubuntu (Flexible Versioning)
- **Terminal Engine:** `ttyd` (Shares terminal over HTTP)
- **Pre-installed Tools:** `wget`, `curl`, `git`, `python3`, `python3-pip`, `neofetch`.

---

## 🛡️ License
Distributed under the **MIT License**. Copyright (c) 2023-2026 **ASEP SAPUTRA**.