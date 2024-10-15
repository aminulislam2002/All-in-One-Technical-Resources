<h1>All-in-One Troubleshooting Guides</h1>

## Windows 10 / 11 Activation Key [Click Here](./main/windows-activation-key/README.md)

## Microsoft Office 16 / 19 / 21 Activation Key [Click Here](./main/microsoft-office-activation-key/README.md)

## Internet Download Manager (IDM) Activation Key [Click Here](./main/idm-activation-key/README.md)

## Internet Download Manager (IDM) Trial Reset File [Click Here](./main/idm-reset/README.md)

## Download Pixie for PC [Click Here](./main/pixie/README.md)


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

# Contact

For questions or support, contact [Aminul Islam](https://aminulislamemon.com/)
