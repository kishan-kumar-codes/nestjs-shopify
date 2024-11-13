# @nestjs-shopify application
Project Name is a Shopify app built to integrate with stores for streamlined data operations, featuring both Online and Offline authentication methods, ensuring secure installation and efficient data handling.

Table of Contents
Project Overview
Features
Installation
Authentication
Environment Variables
Usage
Contributing
License
Project Overview
This app connects with Shopify stores to perform CRUD operations on store data via a secure backend. Built with Next.js on the frontend and NestJS on the backend, it utilizes Shopify Polaris and Tailwind CSS for a responsive, user-friendly interface.

Features
Authentication: Supports Online and Offline modes.
CRUD Operations: Enables Create, Read, Update, and Delete actions on Shopify products.
Responsive Frontend: Developed with Next.js, Shopify Polaris, and Tailwind CSS.
Backend Integration: NestJS backend handles secure API interactions with Shopify.
Environment Configurations: Easily manage credentials and tokens using environment variables.
Installation
Clone the repository:

git clone https://github.com/username/repository-name.git
cd repository-name

```
npm install
```

# In the directory
npm run dev

Authentication
This application implements Online and Offline authentication for Shopify:

Offline Authentication: Used exclusively for the initial installation of the application in a store. It ensures the app can remain authorized even if a user logs out, making it ideal for background tasks and long-term access.

Online Authentication: Used whenever data needs to be loaded on the frontend, offering a session-based, user-specific token. This provides a more secure, temporary session for data interactions during the user's active session.

Shopify Recommendation: Use offline auth for installation and online auth for secure data interactions on the frontend. This setup adheres to Shopify’s security and data management guidelines, ensuring optimal app performance and data handling.

Environment Variables
Set up the following environment variables in both frontend/.env and backend/.env files:

Backend
```
SHOPIFY_API_KEY: Your Shopify API Key
SHOPIFY_API_SECRET: Your Shopify API Secret
SHOPIFY_SCOPES: Permissions required, e.g., read_products,write_products
SHOPIFY_REDIRECT_URI: Redirect URL for authentication
SHOPIFY_ACCESS_TOKEN: Store access token for the app (for persistent access)

```