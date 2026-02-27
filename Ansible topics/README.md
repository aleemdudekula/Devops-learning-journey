## Ansible tutorial

# Ansible in DevOps 🚀

## What is Ansible?

Ansible is an automation tool used in DevOps to manage servers, deploy applications, and maintain infrastructure automatically.

Instead of manually configuring servers one by one, DevOps engineers write automation instructions called **Playbooks** and run them across multiple machines at once.

---

## How DevOps Engineers Use Ansible

### 1. Server Configuration
Automatically install and configure software on new servers.

Example tasks:
- Install Docker, Nginx, or Git
- Create users
- Configure security settings

---

### 2. Application Deployment
Deploy applications consistently across environments.

Typical workflow:
- Pull code from GitHub
- Install dependencies
- Start application services

---

### 3. Infrastructure Automation
Used with cloud platforms like AWS, Azure, and GCP to prepare servers after creation.

Example:
- Launch EC2 instance
- Configure environment automatically using Ansible

---

### 4. Environment Consistency
Ensures Dev, Test, and Production environments have the same configuration.

This reduces:
- “Works on my machine” problems
- Manual errors

---

### 5. CI/CD Integration
Ansible is often used inside CI/CD pipelines.

Example flow:

