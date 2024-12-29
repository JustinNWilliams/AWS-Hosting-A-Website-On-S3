# Hosting a Website on Amazon S3

In this project I will walk you through the process of hosting a static website on Amazon S3 (Simple Storage Service). By the end of this project, you’ll have a fully functional website hosted in the cloud.

---

## Table of Contents

1. [What is Amazon S3](#what-is-amazon-s3)
2. [Project Overview](#project-overview)
3. [Steps to Host a Website on S3](#steps-to-host-a-website-on-s3)
   - [1. Setting Up an S3 Bucket](#1-setting-up-an-s3-bucket)
   - [2. Uploading Website Files to S3](#2-uploading-website-files-to-s3)
   - [3. Enabling Static Website Hosting](#3-enabling-static-website-hosting)
   - [4. Resolving Permission Issues](#4-resolving-permission-issues)
4. [Success!](#success)

---

## What is Amazon S3
![image](https://github.com/user-attachments/assets/de6bd154-6a7b-4902-892c-baf69b5c31ef)


Amazon S3 stands for **Amazon Simple Storage Service**. It is a cloud-based storage solution that allows users to store and retrieve data from anywhere, at any time. 

With S3, you can:
- Store files securely.
- Access your files globally.
- Use it for various applications, including website hosting.

---

## Project Overview

In this project, I used **Amazon S3** to host a fully functional static website. One thing I didn’t expect was how simple and quick it would be to set up! The entire process took me about **15-20 minutes** to complete.

---

## Steps to Host a Website on S3

### 1. Setting Up an S3 Bucket

The first step is creating an S3 bucket to store your website files.

- **Time Taken**: ~1-2 minutes.
- **Region Chosen**: `us-east-1` (I selected this region because I’m located near Chicago.)
- **Important Note**: S3 bucket names are **globally unique**. This means no other account in the world can use the same bucket name unless you delete it.

![Screenshot 2024-12-29 020441](https://github.com/user-attachments/assets/707dc109-af4c-4abb-b46f-bcbaa6e1004c)

---

### 2. Uploading Website Files to S3

Next, I uploaded my website files to the S3 bucket.

- **Files Uploaded**:
  - `index.html` (the main HTML file for the website).
  - `image assets` (a folder containing images and other resources for the website).

Both files are essential for the project, as they contain all the resources needed to fully render the website.

![Screenshot 2024-12-29 020917](https://github.com/user-attachments/assets/27725b67-7a4e-4da3-897e-a52fcc504edc)

---

### 3. Enabling Static Website Hosting

To make the website publicly accessible, I enabled **Static Website Hosting** in my S3 bucket.

- Steps to Enable Static Website Hosting:
  1. Go to the **"Properties"** tab of your S3 bucket.
  2. Scroll down to the **"Static Website Hosting"** section and click **Edit**.
  3. Enable static web hosting, select the hosting type, and set `index.html` as the **index document**.

- **What is Website Hosting?**
  Website hosting means making your website publicly available on the internet for anyone to access.

![Screenshot 2024-12-29 021406](https://github.com/user-attachments/assets/ac581c4d-4437-4d7d-95bb-16ee4db492f5)


---

### 4. Resolving Permission Issues

Once static website hosting is enabled, S3 generates a **bucket endpoint URL**. By default, this URL is private, which means you’ll encounter an error if you try to access it.

- **Error Encountered**: When I first visited the bucket endpoint URL, I saw a `403 Forbidden` error. This happened because the files I uploaded were private.
![Screenshot 2024-12-29 021856](https://github.com/user-attachments/assets/07b066d6-91bb-498c-b44b-9baa1721fc66)

- **Solution**:
  1. Go to the **"Objects"** tab in your S3 bucket.
  2. Select the files you want to make public.
  3. Click **"Actions"** and choose **"Make public using ACL"**.

- **What is an ACL?**
  An **Access Control List (ACL)** is a set of rules that determines who can access specific resources in your S3 bucket.

After making the files public, the website became accessible at the bucket endpoint URL.

---

## Success!

Once I resolved the permission issues, my website was live and accessible to the public. Hosting a website on Amazon S3 turned out to be much easier and faster than I expected.

![Screenshot 2024-12-29 022417](https://github.com/user-attachments/assets/0ed249f0-0ff0-4092-8060-cc9a0144438d)

---
