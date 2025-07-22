# SOP: Gunicorn 


> This SOP is a simple guide for setting up and using Gunicorn, a Python WSGI HTTP Server, on Ubuntu.



---
## Author Information

| Created by      | Created on  | Version | Last updated ON | pre Reviewer | 
|-----------------|------------|---------|-----------------|--------------| 
| Sunny kumar | 22-07-2025 | V 1.0   | 22-07-2025      | Aman Raj       | 

---

## Table of Contents
- [Purpose](#1-purpose)
- [Scope](#2-scope)
- [Prerequisites](#3-prerequisites)
- [Procedure](#4-procedure)
  - [4.1. Introduction](#41-introduction)
  - [4.2. Update system packages](#42-Update-system-packages)
  - [4.3. Install Python3 and pip](#43-Install-Python3-and-pip)
  - [4.4. Create a project directory](#44-Create-a-project-directory)
  - [4.5. Create a virtual environment](#45-Create-a-virtual-environment)
  - [4.6. Install Gunicorn inside the virtual environment](#46-Install-Gunicorn-inside-the-virtual-environment)
  - [4.7. Verify Gunicorn installation](#47-Verify-Gunicorn-installation)
- [Troubleshooting](#troubleshooting)
- [Conclusion](#conclusion)
- [References](#references)
- [Contact Information](#contact-information)

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
<img width="1044" height="314" alt="image" src="https://github.com/user-attachments/assets/51c8bc30-d580-4eee-b027-894c70c20824" />


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

## Troubleshooting

| **Issue**                                          | **Possible Cause**            | **Solution**                                                                 |
|----------------------------------------------------|------------------------------|------------------------------------------------------------------------------|
| pip: command not found         | pip is not installed on your system | `sudo apt install python3-pip`|
| gunicorn: command not found after installation                | Gunicorn was installed in a virtual environment that's not activated.       | Activate the virtual environment: `source venv/bin/activate`                |
|  Permission denied while installing Gunicorn globally                      | Insufficient privileges when using pip.         | Use `sudo` with `pip3 `                     |
| SSL/TLS or network errors during installation                          | Network issues or outdated `pip`   | `pip install --upgrade pip`


---


## Conclusion

By following this SOP, you’ve successfully installed Gunicorn on an Ubuntu system and resolved common installation-related issues. Gunicorn provides a robust, efficient way to serve Python web applications in production. 

---

## References

| Links                                                                                     | Descriptions                           |
|-------------------------------------------------------------------------------------------|----------------------------------------|
| [Python Packaging Guide (Official)](https://packaging.python.org/en/latest/) | Install & best practices      |
| [W3Schools - Python venv](https://www.w3schools.com/python/python_virtualenv.asp) | Simple explanation   |
| [Gunicorn](https://docs.gunicorn.org/en/latest/install.html) |How to install gunicorn|


---

## Contact Information

| Name             | Email                                         |
|------------------|-----------------------------------------------|
| Sunny kumar  | sunny.kumar.snaatak@mygurukulam.co        |

---
