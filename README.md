# Docker Tutorial: Getting Started

Welcome to this Docker tutorial!

In this guide, we'll walk through the installation process of Docker Engine and understand what Docker is, how it works, and why it's such a powerful tool in modern development.

---

## 📚 Table of Contents

1. [What is Docker?](#1-what-is-docker)
2. [What is an Image?](#2-what-is-an-image)
3. [What is a Container?](#3-what-is-a-container)
4. [Installing Docker](#4-installing-docker)
5. [Testing Your Docker Installation](#5-testing-your-docker-installation)
6. [Common Docker Commands](#6-common-docker-commands)
7. [Enabling Kubernetes](#7-enabling-kubernetes)
8. [Practice and Testing Resources](#8-practice-learn-by-doing)

---

## 1. What is Docker?

Docker is an open-source **containerization platform** originally developed by **Docker, Inc.** to solve the age-old problem:

> “But it works on my machine!”

It allows you to package your application and its dependencies into a **Docker image**, which can then be run anywhere, ensuring consistency across environments.

---

## 2. What is an Image?

A **Docker image** is like a snapshot of a virtual computer. It includes everything your app needs: code, libraries, OS dependencies, and more.

📌 **Example:**
Imagine an image called `dylan/example-image` running a minimal Linux distro with a Python app that adds two numbers.

---

## 3. What is a Container?

A **container** is a running instance of an image. It's like turning that snapshot into a live machine. It uses your host's resources (CPU, RAM, storage) — but is isolated from the rest of the system.

Docker automatically manages resources efficiently, but you can also manually set limits.

📌 **Example:**
Your Python app from earlier can run inside a container, using just a small amount of memory and CPU. You can inspect it with commands like:

```bash
docker container ls
docker stats
docker logs <container-name>
```

---

## 4. Installing Docker

To install Docker, visit the official site:

👉 [https://www.docker.com/products/docker-desktop/](https://www.docker.com/products/docker-desktop/)

Choose the version suited for your system (Windows, Mac, or Linux).
📸 *(Add screenshot: ******`downloaddocker.png`****** here)*

---

## 5. Testing Your Docker Installation

After installation, open your terminal (e.g., Mac Terminal, Windows PowerShell), and run:

```bash
docker --version
```

📸 *(Add screenshot: Terminal with version output)*

✅ If you see a version message like:

```
Docker version 24.0.2, build cb74dfc
```

You're all set!

❌ If you get an error:

* On **Windows**, make sure **WSL 2** and **Virtual Machine Platform** are enabled.
* Try restarting Docker or reinstalling.

---

## 6. Common Docker Commands

Here are some helpful commands to get started:

```bash
docker images             # List all images
docker ps                 # List running containers
docker ps -a              # List all containers
docker run hello-world    # Run a test container
docker stop <name|id>     # Stop a container
docker rm <name|id>       # Remove a container
docker rmi <image>        # Remove an image
```

---

## 7. Enabling Kubernetes

Want to go further? Try Kubernetes!
Kubernetes (K8s) is an open-source platform for **automating** container deployment, scaling, and management.

### 🛠️ Enabling Kubernetes in Docker Desktop:

1. Open Docker Desktop.
2. Go to **Settings**.
3. On the left, select **Kubernetes**.
4. Check **"Enable Kubernetes"**.
5. Click **Apply & Restart**.

⚠️ **Note:** Kubernetes can be **resource-intensive**. It may slow your system.

### ✅ Testing Kubernetes

Once enabled, run:

```bash
kubectl get nodes
```

📸 *(Add screenshot: Terminal with kubectl output)*

✅ If you get a node list, Kubernetes is running.
❌ If not, try toggling it off and on, or restarting your machine.

---

## 8. Practice: Learn by Doing

To practice your Docker skills, check out:

* 🧺 [https://labs.play-with-docker.com/](https://labs.play-with-docker.com/)
* 📚 Try building small containers from scratch
* 👨‍💻 Clone public Docker projects and explore

---
