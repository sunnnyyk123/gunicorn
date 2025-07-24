# SOP: Gunicorn 


---
## Author Information

| Created by      | Created on  | Version | Last updated | Pre-Reviewer | 
|-----------------|------------|---------|-----------------|--------------| 
| Sunny Kumar | 22-07-2025 | V 1.0   | 22-07-2025      | Aman Raj       | 

---

## Table of Contents
- [1. Purpose](#1-purpose)
- [2. Scope](#2-scope)
- [3. Prerequisites](#3-prerequisites)
- [4. Procedure](#4-procedure)
  - [4.1. Introduction](#41-introduction)
  - [4.2. Update system packages](#42-Update-system-packages)
  - [4.3. Install Python3 and pip](#43-Install-Python3-and-pip)
  - [4.4. Create a project directory](#44-Create-a-project-directory)
  - [4.5. Create a virtual environment](#45-Create-a-virtual-environment)
  - [4.6. Install Gunicorn inside the virtual environment](#46-Install-Gunicorn-inside-the-virtual-environment)
  - [4.7. Verify Gunicorn installation](#47-Verify-Gunicorn-installation)
- [5. Troubleshooting](#troubleshooting)
- [6. Conclusion](#conclusion)
- [7. Contact Information](#contact-information)
- [8. References](#references)

## 1. Purpose

This SOP outlines the standard procedure for installing, configuring, and verifying Gunicorn, a Python WSGI HTTP server, to serve Python web applications efficiently on Ubuntu systems.

## 2. Scope
This guide covers:

- Step-by-step installation of Gunicorn on Ubuntu

- Setting up a Python virtual environment

- Installing Gunicorn via pip

- Verifying the Gunicorn installation

## 3. Prerequisites
- A Debian/Ubuntu-based Linux system

- Python 3 and pip installed

- User privileges to run commands with sudo

- Internet connection to download required packages

## 4. Procedure

### 4.1. Introduction
Gunicorn is a lightweight, production-ready WSGI HTTP server for running Python web applications. It works seamlessly with frameworks like Flask and Django, handling multiple requests efficiently using a pre-fork worker model.

### 4.2. Update system packages
```bash
sudo apt update && sudo apt upgrade -y
```

### 4.3. Install Python3 and pip


```bash
sudo apt install python3 python3-pip -y
```
<img width="883" height="183" alt="image" src="https://github.com/user-attachments/assets/61cd6de6-94f9-43f5-ac21-d6c9f2cbfe2d" />

### 4.4. Create a project directory 

Create and navigate to your project folder :

```bash
mkdir myproject
cd myproject
```
<img width="900" height="181" alt="image" src="https://github.com/user-attachments/assets/19121976-cf0a-44ac-b51b-429c49a178e5" />


### 4.5. Create a virtual environment 
```bash
python3 -m venv venv
source venv/bin/activate
```
<img width="900" height="181" alt="image" src="https://github.com/user-attachments/assets/97d9c33f-4f06-43ea-9fb3-822d28a96f7f" />


### 4.6. Install Gunicorn inside the virtual environment


```bash
pip install gunicorn
```
<img width="909" height="225" alt="image" src="https://github.com/user-attachments/assets/309c332b-13ff-43ac-bf9d-2d6340db94c9" />


### 4.7. Verify Gunicorn installation

```bash
gunicorn --version
```
<img width="909" height="225" alt="image" src="https://github.com/user-attachments/assets/17e0a509-2a4c-4c9f-af89-6f4f42f425d8" />

---

## 5. Troubleshooting

| **Issue**                                          | **Possible Cause**            | **Solution**                                                                 |
|----------------------------------------------------|------------------------------|------------------------------------------------------------------------------|
| pip: command not found         | pip is not installed on your system | `sudo apt install python3-pip`|
| gunicorn: command not found after installation                | Gunicorn was installed in a virtual environment that's not activated.       | Activate the virtual environment: `source venv/bin/activate`                |
|  Permission denied while installing Gunicorn globally                      | Insufficient privileges when using pip.         | Use `sudo` with `pip3 `                     |
| SSL/TLS or network errors during installation                          | Network issues or outdated `pip`   | `pip install --upgrade pip`


---


## 6. Conclusion

By following this SOP, you’ve successfully installed Gunicorn on an Ubuntu system and resolved common installation-related issues. Gunicorn provides a robust, efficient way to serve Python web applications in production. 

---

## 7. Contact Information

| Name             | Email                                         |
|------------------|-----------------------------------------------|
| Sunny Kumar  | sunny.kumar.snaatak@mygurukulam.co        |

---
## 8. References

| Links                                                                                     | Descriptions                           |
|-------------------------------------------------------------------------------------------|----------------------------------------|
| [Python Packaging Guide (Official)](https://packaging.python.org/en/latest/) | Install & best practices      |
| [W3Schools - Python venv](https://www.w3schools.com/python/python_virtualenv.asp) | Simple explanation   |
| [Gunicorn](https://docs.gunicorn.org/en/latest/install.html) |How to install Gunicorn|



---
