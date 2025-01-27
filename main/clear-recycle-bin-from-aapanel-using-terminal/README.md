# Clearing `.Recycle_bin` Folder via Terminal in aaPanel

Follow these steps to clear the `.Recycle_bin` folder on your server managed by aaPanel using terminal commands.

---

## Step 1: Access Your Server Terminal
- Log in to your server via SSH using a terminal application (e.g., PuTTY, or a built-in terminal on Linux/Mac).
- Alternatively, you can use the terminal provided within aaPanel by navigating to the **"Terminal"** section in the panel.

---

## Step 2: Locate the `.Recycle_bin` Folder
The `.Recycle_bin` folder is usually located at the root (`/`) directory or within the `www` folder if it’s related to web files.

To check its location, run the following command:

```bash
ls -la /
```

Look for `.Recycle_bin` in the output.

---

## Step 3: Clear Contents of `.Recycle_bin`
To delete the contents of the `.Recycle_bin` folder, use the command:

```bash
rm -rf /.Recycle_bin/*
```

This command will:
- `rm`: Remove files and directories.
- `-r`: Recursively delete directories and their contents.
- `-f`: Force deletion without prompting for confirmation.

---

## Step 4: Verify the Folder is Empty
To confirm the folder is empty, run:

```bash
ls -la /.Recycle_bin
```

If the folder is empty, you’ll see only `.` and `..` in the output.

---

By following these steps, you can successfully clear the `.Recycle_bin` folder from your server using terminal commands.