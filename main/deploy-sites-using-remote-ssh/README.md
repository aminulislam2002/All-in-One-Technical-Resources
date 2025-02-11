Here's a more professional version of your documentation for the README file:

---

# **Deploying a MERN Stack Application to a VPS Using VS Code Remote SSH**

This guide walks you through the process of deploying a **MERN** (MongoDB, Express.js, React.js, Node.js) application to a **VPS** (Virtual Private Server) using **VS Code Remote SSH**. Follow these steps for a seamless deployment experience.

---

## **Step 1: Connect to Your VPS Using VS Code Remote SSH**

1. **Open VS Code**.
2. **Install the "Remote - SSH" extension** if you haven't already done so.
3. Press `Ctrl + Shift + P` to open the command palette, then search for and select **Remote-SSH: Connect to Host**.
4. Enter your **VPS SSH details**:
   ```bash
   ssh user@your-vps-ip
   ```
   Example:
   ```bash
   ssh root@103.191.241.110
   ```
5. If you're using an **SSH key**, ensure it's added to your SSH agent:
   ```bash
   ssh-add ~/.ssh/your-private-key
   ```
6. Once connected, the **VPS filesystem** will be available directly in VS Code.

---

## **Step 2: Upload the Frontend (React.js) to Your VPS**

To transfer your React project from your local machine to your VPS, use **SCP (Secure Copy)**:

### **Using SCP (Secure Copy)**

```bash
scp -r [files & folders] user@your-vps-ip:/www/wwwroot/project-frontend-folder-name
```

Example:

```bash
scp -r index.html vite.svg assets root@103.191.241.110:/www/wwwroot/aminulislamemon.com
```

---

## **Step 3: Upload the Backend (Node.js & Express) to Your VPS**

Similarly, to upload your backend project, use **SCP (Secure Copy)**:

### **Using SCP (Secure Copy)**

```bash
scp -r [files & folders] user@your-vps-ip:/www/wwwroot/project-backend-folder-name
```

Example:

```bash
scp -r index.js .env package.json package-lock.json images root@103.191.241.110:/www/wwwroot/serverapi
```

---

## **Step 4: Update and Restart the Backend Project**

Once the backend files are uploaded, you may need to restart the application to apply the changes.

1. SSH into your VPS:
   ```bash
   ssh root@your-vps-ip
   ```
   Example:
   ```bash
   ssh root@103.191.241.110
   ```
2. Navigate to the backend project directory:
   ```bash
   cd /www/wwwroot/serverapi
   ```
3. Restart the backend server using **PM2**:
   ```bash
   pm2 restart index.js
   ```

---

## **Step 5: Final Checklist**

- ✅ **Connected** to the VPS using **VS Code Remote SSH**.
- ✅ **Transferred** frontend and backend files using **SCP**.
- ✅ **Configured** the backend with **PM2** for process management.
- ✅ **Set up** the frontend with **Nginx** for efficient web serving.
- ✅ **Enabled** the firewall and **SSL** for security (optional but recommended).

---

Your **MERN stack application** is now **successfully deployed** to your **VPS**! 🚀

---
