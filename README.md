# Web Issues Solutions

## Windows, Office Activation Key
```apache
irm https://get.activated.win | iex
```

### Instructions
#### Step 1: Open PowerShell (Not CMD). To do that, right-click on the Windows start menu and select PowerShell or Terminal.
#### Step 2: Copy and paste the code below and press enter
#### Step 3: You will see the activation options. Choose [1] HWID for Windows activation. Choose [2] Ohook for Office activation.
#### Step 4: That's all

## Internet Download Manager (IDM) Activation Key
```apache
irm https://massgrave.dev/ias | iex
```

### Instructions
#### Step 1: Open PowerShell (Not CMD). To do that, right-click on the Windows start menu and select PowerShell or Terminal.
#### Step 2: Copy and paste the code below and press enter
#### Step 3: You will see the activation options. Choose [2] Activate & then choose [9] Activate for IDM Activation.
#### Step 4: That's all

## Issue-1: Solution to React Router 404 Error on Refresh After Deployment in cPanel

### Issue Description

When deploying a React application to cPanel and using React Router for client-side routing, you may encounter a 404 error when refreshing the URLs. This is because cPanel's default behavior doesn't handle single-page applications (SPAs) correctly.

### Solution

To resolve this issue and make your React Router work correctly after deployment on cPanel, follow these steps:

1. Create an `.htaccess` file in your cPanel's public_html directory (or the directory where your React app is deployed).

2. Add the following code to the `.htaccess` file:

```apache
<IfModule mod_rewrite.c>
  RewriteEngine On
  RewriteBase /
  RewriteRule ^index\.html$ - [L]
  RewriteCond %{REQUEST_FILENAME} !-f
  RewriteCond %{REQUEST_FILENAME} !-d
  RewriteRule . /index.html [L]
</IfModule>
```

## Issue-2: Solution to React Router 404 Error on Refresh After Deployment in VPS server

### Solution

To fix loading error go to "Website" or website list and click on site name and go to "URL rewrite".

```apache
location / {
try_files $uri /index.html;
}
```

Save with this code
