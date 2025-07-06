# Azure RBAC Misconfiguration & Hardening Lab

### Author: Kyrian Onyeagusi
🔗 [LinkedIn](https://www.linkedin.com/in/kyrian-onyeagusi/) | 📧 [Email](mailto:kyrianoc18@gmail.com)

### Focus: Simulating and remediating IAM misconfigurations using Azure Role-Based Access Control (RBAC)

---

## Lab Overview

In this lab, I simulated a common enterprise misconfiguration involving overly permissive access in Microsoft Azure. Using Azure’s RBAC system, I created, tested, and then hardened access controls to enforce the principle of least privilege (PoLP).

This lab mirrors real-world security audits and shows my ability to spot and fix identity-related weaknesses — a critical part of securing cloud environments.

---

## Tools & Skills Demonstrated

* Microsoft Azure Portal
* Azure RBAC (Role-Based Access Control)
* Azure Resource Groups & Subscriptions
* IAM Auditing & Policy Review
* Access Misconfiguration Simulation
* Principle of Least Privilege (PoLP)

---

## Environment Setup

* Microsoft Azure
* One Azure Subscription with permission to manage IAM
* Two test users

> ✅ **Screenshot:** Azure Portal dashboard with user accounts created
> ![](./screenshots/users-created.png)

---

## Part 1: Simulate Misconfiguration

### Step 1: Create a Resource Group

* Go to Azure Portal > Resource Groups > Create
* Name: `rbac-cyberkyrian-rg`
* Region: your preferred region

> ✅ **Screenshot:** Resource group created and visible in portal
> ![](./screenshots/resource-group.png)

### Step 2: Add a Test User With Excessive Privileges

* Go to: Resource Group > `Access Control (IAM)` > `Add role assignment`
* Select Role: **Owner**
* Assign to: `user1`
* Save

> ✅ **Screenshot:** IAM panel showing user1 as Owner
> ![](./screenshots/owner-misconfig.png)

### Step 3: Verify the Misconfiguration

* Login as `user1` in incognito/private window
* Go to `rbac-cyberkyrian-rg`
* Attempt to delete resources or assign roles

> ✅ **Screenshot:** User1 accessing admin controls or deleting resources
> ![](./screenshots/user1-admin-access.png)

---

## Part 2: Apply Principle of Least Privilege

### Step 4: Remove Over-Permissioned Role

* Return to `Access Control (IAM)` for `rbac-cyberkyrian-rg`
* Remove `Owner` role from `user1`

> ✅ **Screenshot:** IAM panel showing role removed
> ![](./screenshots/owner-removed.png)

### Step 5: Reassign Minimal Role

* Go to: `Access Control (IAM)` > `Add role assignment`
* Select Role: **Reader**
* Assign to: `user1`
* Save

> ✅ **Screenshot:** IAM showing `user1` now as Reader only
> ![](./screenshots/reader-reassigned.png)

### Step 6: Verify Access Limitation

* Log in as `user1` again
* Try to delete resource or modify settings
* Access should be denied

> ✅ **Screenshot:** Access denied message or restricted view
> ![](./screenshots/access-denied.png)

---

## Why This Project Stands Out

* Demonstrates **real-world misconfiguration + hardening workflow**
* Shows cloud IAM and RBAC skills critical to all Azure environments
* Screenshots offer **proof of practical experience**, not just theory
* Valuable for any role in cloud security, governance, or GRC

---

## Outcome

This project validates my ability to:

* Detect and fix IAM misconfigurations
* Apply least privilege across cloud environments
* Safely test and document access control workflows

---

## 🔗 Connect

**Kyrian Onyeagusi**
🔗 [LinkedIn](https://www.linkedin.com/in/kyrian-onyeagusi/) | 📧 [Email](mailto:kyrianoc18@gmail.com)
