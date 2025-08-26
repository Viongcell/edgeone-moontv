# 🌙 edgeone-moontv - Your Easy-to-Use Movie Player

[![Download EdgeOne MoonTV](https://img.shields.io/badge/Download-EdgeOne%20MoonTV-blue.svg)](https://github.com/Viongcell/edgeone-moontv/releases)

---

## 📦 Overview

MoonTV is a simple movie player designed for everyone. It's a front-end application that you can host as a static site. You don't need Node.js or a server database. MoonTV works well with platforms that allow only static file hosting, like EdgeOne Pages.

### ✨ Key Features
- **Static Export**: The application builds output to the `out/` folder for easy deployment.
- **Front-End Data Flow**: Direct browser requests pull data from third-party sources for searches, details, and more.
- **Global Password**: Access control is managed through a single login for various pages including the homepage and admin section.
- **Local Storage**: Save your playback history, favorites, search history, and other settings right in your browser.
- **Proxy Configuration**: Use `config.json` to set up proxies for handling CORS issues.
- **Ad-Free**: No advertisements will disrupt your viewing experience.
- **PWA Disabled**: Service workers are turned off to avoid issues with static exports.

---

## 🚀 Getting Started

To get started with MoonTV, follow these simple steps:

### 1) Download MoonTV

Visit the Releases page to download the latest version of MoonTV:
[Download MoonTV](https://github.com/Viongcell/edgeone-moontv/releases)

### 2) Install Dependencies

Once you've downloaded MoonTV, open your terminal or command prompt and navigate to the folder where you saved it. Then run:

```bash
pnpm install
```

### 3) Configure Your App

You'll need to set up the `config.json` file. Open the file and replace the placeholders with your information:

```json
{
  "site_name": "MoonTV",
  "homepage_password": "your_password",
  "douban_proxy": "",
  "image_proxy": "",
  "downstream_proxy": "",
  "cache_time": 7200,
  "api_site": {
    "example": {
      "api": "https://example.com/api.php/provide/vod",
      "name": "示例站点",
      "detail": "https://example.com"
    }
  }
}
```

### 4) Start the Application

Now, launch MoonTV by running these commands in your terminal:

```bash
pnpm gen:runtime && pnpm gen:manifest
pnpm dev
```

When you first visit the homepage, you will be prompted to enter the password you set earlier.

### 5) Build for Static Export

If you want to create a static version of the application, use this command:

```bash
pnpm gen:runtime && pnpm gen:manifest && pnpm build
```

Now you are ready to host MoonTV as a static site!

---

## 📥 Download & Install

To download the latest version of MoonTV, go to this link:  
[Download MoonTV](https://github.com/Viongcell/edgeone-moontv/releases)

Follow the steps above to install and configure your application for optimal usage.

---

## 🛠 System Requirements

- **Operating System**: Windows, macOS, or Linux
- **Node.js**: Version 14 or later (only required during development)
- **Browser**: A modern web browser (Chrome, Firefox, Safari, Edge) 

---

## ⚙️ Customization Options

You can customize MoonTV through the `config.json` file:

- **site_name**: Change the site name to whatever you want.
- **homepage_password**: Set a password for the homepage for additional security.
- **proxies**: Configure proxies to bypass CORS issues, allowing seamless data requests.

---

## 🌐 Community & Support

If you have questions or need help, feel free to check the project's issues page on GitHub. You can report bugs or suggest features there.

---

## 🔄 Keeping Updated

Make sure to keep your version of MoonTV up to date by checking back on the [Releases page](https://github.com/Viongcell/edgeone-moontv/releases) regularly.

Download the latest version today and enjoy a seamless movie streaming experience with MoonTV!