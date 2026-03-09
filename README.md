# 🌐 Subham Gaurav — Personal Portfolio Website

A personal portfolio website built with pure **HTML**, **CSS**, and **JavaScript**, showcasing projects, certifications, and Kaggle competition work. Deployed on **GitHub Pages**.

[![Live Demo](https://img.shields.io/badge/Live-GitHub%20Pages-blue?style=for-the-badge&logo=github)](https://subhamgrv.github.io/)
[![GitHub](https://img.shields.io/badge/GitHub-subhamgrv-black?style=for-the-badge&logo=github)](https://github.com/subhamgrv)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-subhamgrv-0077B5?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/subhamgrv/)
[![Kaggle](https://img.shields.io/badge/Kaggle-subhamgrv-20BEFF?style=for-the-badge&logo=kaggle)](https://www.kaggle.com/subhamgrv/)

---

## 📋 Table of Contents

- [About](#about)
- [Live Demo](#live-demo)
- [Features](#features)
- [Pages Overview](#pages-overview)
- [Project Structure](#project-structure)
- [Tech Stack](#tech-stack)
- [Key JavaScript Components](#key-javascript-components)
- [Data Files (JSON)](#data-files-json)
- [Projects Showcased](#projects-showcased)
- [Certifications](#certifications)
- [Kaggle Competitions](#kaggle-competitions)
- [Getting Started (Clone & Run Locally)](#getting-started-clone--run-locally)
- [Deployment (GitHub Pages)](#deployment-github-pages)
- [Customization Guide](#customization-guide)
- [Connect with Me](#connect-with-me)

---

## About

This is the personal portfolio website of **Subham Gaurav**, a developer with interests in:

- 📊 **Data Science**
- 🌐 **Web Development**
- 🔓 **Open Source**

The website features an animated particle background, a typing text animation, dynamically rendered project cards, certifications gallery, and an embedded Kaggle project listing — all built without any framework or build tool.

---

## Live Demo

> The website is deployed on **GitHub Pages** and accessible at:
> **https://subhamgrv.github.io/**

The **About Me** page embeds the separate CV website:
> **https://subhamgrv.github.io/CV_website/**

---

## Features

| Feature | Description |
|---|---|
| ✨ Animated Particle Background | Interactive particle network using `particles.js` on every page |
| ⌨️ Typing Text Animation | Home page displays rotating animated text: *Data Science, Web Development, Open Source* |
| 🃏 Dynamic Project Cards | Projects loaded from `assets/projects.json` and rendered as interactive cards |
| 📜 Certifications Gallery | Certifications dynamically loaded from `assets/certificates.json` |
| 🏆 Kaggle Projects List | Kaggle competition entries fetched and displayed from `assets/kaggle_projects.json` |
| 📄 Embedded CV | About Me page embeds the full CV website via `<iframe>` |
| 🖱️ Interactive Particles | Particles repulse on hover; new particles spawn on click |
| 📱 Responsive Navigation | Navigation bar present on all pages with active link states |
| 🔗 Social Links | Links to CV website, LinkedIn, GitHub, and Kaggle on the home page |

---

## Pages Overview

### 🏠 Home (`index.html`)
- Greeting section: "Hi 👋, I'm **Subham Gaurav**"
- Circular profile photo
- Animated typing text cycling through: `Data Science`, `Web Development`, `Open Source`
- Social icon links: **CV**, **LinkedIn**, **GitHub**, **Kaggle**
- Animated particle background

### 📜 Certifications (`certifications.html`)
- Grid layout of certification images dynamically loaded from JSON
- Displays certificate name and image for each entry

### 💼 Projects (`projects.html`)
- Grid of project cards dynamically rendered from JSON
- Each card shows: **project image**, **name**, **duration**, **description**, **features list**, and **technologies used**
- Click on a project image to toggle displaying full project details

### 🏆 Kaggle (`kaggle.html`)
- Lists Kaggle competition projects with links, descriptions, difficulty level, and technologies used
- All data loaded dynamically from JSON

### 👤 About Me (`aboutme.html`)
- Embeds the full **CV website** (`https://subhamgrv.github.io/CV_website/`) in a full-height iframe

---

## Project Structure

```
PortfolioWebsite/
│
├── index.html                  # Home page
├── aboutme.html                # About Me page (embeds CV website)
├── certifications.html         # Certifications gallery
├── projects.html               # Projects showcase
├── kaggle.html                 # Kaggle competition projects
├── sidebar.html                # Sidebar component (loaded dynamically)
│
├── css/
│   ├── styles.css              # Global styles (dark theme, nav, layout, particles)
│   ├── project.css             # Project card & grid styles
│   ├── certificate.css         # Certification grid & image styles
│   └── kaggle.css              # Kaggle section styles
│
├── js/
│   ├── animateText.js          # Typing text animation for the home page
│   ├── particles-config.js     # Particles.js configuration (golden particles)
│   ├── projects.js             # Fetches & renders project cards from JSON
│   ├── certificate.js          # Fetches & renders certifications from JSON
│   ├── kaggle.js               # Fetches & renders Kaggle projects from JSON
│   └── script.js               # Misc: form handlers, theme color changer, sidebar loader
│
├── assets/
│   ├── projects.json           # Project data (name, description, features, tech stack)
│   ├── certificates.json       # Certification data (name, image path)
│   ├── kaggle_projects.json    # Kaggle competition data (name, URL, tech, difficulty)
│   └── images/                 # Project & certificate images
│       └── Certificates/       # Certificate image files
│
└── images/
    └── profile.jpg             # Profile photo used on the home page
```

---

## Tech Stack

| Layer | Technology |
|---|---|
| Markup | HTML5 |
| Styling | CSS3 (Vanilla) |
| Logic | JavaScript (ES6+, Fetch API) |
| Fonts | Google Fonts — [Lobster](https://fonts.google.com/specimen/Lobster) |
| Icons | [Font Awesome 5.15.4](https://fontawesome.com/) |
| Particles | [Particles.js](https://vincentgarreau.com/particles.js/) (via CDN) |
| Data | JSON files (no backend required) |
| Hosting | GitHub Pages |

---

## Key JavaScript Components

### `animateText.js`
Implements a classic **typewriter effect** on the home page hero section.
- Cycles through words defined in the `data-words` attribute of `.animated-text`
- Types at 100ms per character, pauses 1000ms between words
- Words animated: `Data Science`, `Web Development`, `Open Source`

### `particles-config.js`
Configures the **interactive particle background** present across all pages:
- **80 golden particles** (`#f0a500`) on each page
- Particles are linked by lines and move randomly
- **Hover**: particles repulse away from cursor
- **Click**: new particles are pushed/spawned
- Retina display support enabled

### `projects.js`
Fetches `assets/projects.json` and dynamically renders **project cards** into `#project-grid`.
- Each card displays: image, name, duration, description, features, and technologies
- Clicking a project image toggles the visibility of full project details (`.show-details`)

### `certificate.js`
Fetches `assets/certificates.json` and renders a **certifications grid** into `#certification-grid`.
- Displays each certification's image and name

### `kaggle.js`
Fetches `assets/kaggle_projects.json` and renders a **linked list of Kaggle projects** into `#kaggle-list`.
- Each item shows: project name (as clickable link), description, difficulty, and technologies

### `script.js`
- Handles project and Kaggle form submissions (dynamic list appending)
- Implements a **theme color changer** using CSS custom properties (`--theme-color`)
- Loads `sidebar.html` dynamically into `#sidebar-placeholder` via `fetch()`

---

## Data Files (JSON)

All content is data-driven and can be updated without touching any HTML.

### `assets/projects.json`
```json
{
  "projects": [
    {
      "name": "Project Name",
      "duration": "MM/YYYY – MM/YYYY",
      "description": "Short description...",
      "features": ["Feature 1", "Feature 2"],
      "technologies_used": { "front_end": ["HTML", "CSS"], "back_end": "PHP" },
      "image": "assets/images/project_image.png"
    }
  ]
}
```

### `assets/certificates.json`
```json
[
  {
    "name": "Certificate Name",
    "date": "MM/DD/YYYY",
    "description": "Description...",
    "image": "assets/images/Certificates/CertificateName.png"
  }
]
```

### `assets/kaggle_projects.json`
```json
[
  {
    "name": "Competition Name",
    "url": "https://www.kaggle.com/c/competition-slug",
    "description": "Description...",
    "difficulty": "Beginner | Intermediate | Advanced",
    "technologies": ["Python", "Pandas"]
  }
]
```

---

## Projects Showcased

| Project | Duration | Tech Stack |
|---|---|---|
| Life Insurance Management System | Sep 2020 – Jan 2021 | HTML, CSS, PHP, MySQL |
| Unidentified Flying Objects (UFO Simulator) | Apr 2021 – Jul 2021 | C, OpenGL |
| Basic Banking App | Apr 2021 – Jul 2021 | Android Studio, Firebase |
| Behavioral-Based Student Stress Detection with Attendance Management | Sep 2021 – Jul 2022 | Python, OpenCV, Image Processing |

---

## Certifications

The following certifications are displayed on the website:

| Certificate | Platform |
|---|---|
| Applied Data Science Capstone | IBM / Coursera |
| Data Analysis with Python | IBM / Coursera |
| Data Science Methodology | IBM / Coursera |
| What is Data Science | IBM / Coursera |
| Tools for Data Science | IBM / Coursera |
| Python Project for Data Science | IBM / Coursera |
| Python for Data Science, AI & Development | IBM / Coursera |
| Programming in JAVA | Coursera |
| Programming for Everybody (Getting Started with Python) | University of Michigan / Coursera |
| Machine Learning with Python | IBM / Coursera |
| Databases and SQL for Data Science with Python | IBM / Coursera |
| Data Visualization with Python | IBM / Coursera |
| Data Structure and Algorithms using JAVA | Coursera |
| Minecraft Apply and Enrich: Chemistry | Microsoft (Jun 2021) |

---

## Kaggle Competitions

| Competition | Difficulty | Technologies |
|---|---|---|
| [Titanic - Machine Learning from Disaster](https://www.kaggle.com/c/titanic) | Beginner | Python, Pandas, Scikit-learn |
| [House Prices - Advanced Regression Techniques](https://www.kaggle.com/c/house-prices-advanced-regression-techniques) | Intermediate | Python, R, XGBoost |
| [Digit Recognizer - Handwritten Digit Classification](https://www.kaggle.com/c/digit-recognizer) | Intermediate | Python, OpenCV, TensorFlow |

---

## Getting Started (Clone & Run Locally)

No build tools, no npm, no servers required. Just a browser.

### 1. Clone the Repository

```bash
git clone https://github.com/subhamgrv/PortfolioWebsite.git
cd PortfolioWebsite
```

### 2. Open in Browser

Simply open `index.html` in any modern web browser:

```bash
# On Windows
start index.html

# On macOS
open index.html

# On Linux
xdg-open index.html
```

> ⚠️ **Note:** Because project data is loaded via the `Fetch API` from local JSON files, some browsers block local file fetches due to CORS policy. To avoid this, serve the files using a local development server.

### 3. Using a Local Dev Server (Recommended)

**Option A — VS Code Live Server:**
1. Install the [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension in VS Code
2. Right-click `index.html` → **Open with Live Server**

**Option B — Python HTTP Server:**
```bash
# Python 3
python -m http.server 8000
# Then open http://localhost:8000 in your browser
```

**Option C — Node.js `http-server`:**
```bash
npx http-server .
# Then open http://localhost:8080
```

---

## Deployment (GitHub Pages)

This site is deployed using **GitHub Pages** from the repository's `main` branch.

### Steps to Deploy Your Fork

1. **Fork** this repository
2. Go to your forked repo's **Settings** → **Pages**
3. Under **Source**, select `main` branch and `/ (root)` folder
4. Click **Save** — your site will be live at:
   ```
   https://<your-github-username>.github.io/PortfolioWebsite/
   ```

### To Update Your Portfolio

1. Edit the relevant JSON file in `assets/`:
   - Add a new project → `assets/projects.json`
   - Add a new certification → `assets/certificates.json`
   - Add a Kaggle project → `assets/kaggle_projects.json`
2. Commit and push:
   ```bash
   git add .
   git commit -m "Add new project/certification"
   git push origin main
   ```
3. GitHub Pages will automatically rebuild and deploy within ~30 seconds.

---

## Customization Guide

### Change Profile Photo
Replace `images/profile.jpg` with your own photo (keep the same filename, or update the `src` in `index.html`).

### Update Animated Text Roles
In `index.html`, find the `data-words` attribute and update the comma-separated list:
```html
<span class="animated-text" data-words="Data Science, Web Development, Open Source"></span>
```

### Change Particle Color
In `js/particles-config.js`, change the `color.value` and `line_linked.color` fields:
```js
"color": { "value": "#f0a500" },  // Change to your preferred hex color
"line_linked": { "color": "#f0a500" }
```

### Update Social Links
In `index.html`, update the `href` attributes of the social icon links:
```html
<a href="https://your-cv-url.com" class="icon">CV</a>
<a href="https://linkedin.com/in/yourprofile" class="icon">LinkedIn</a>
<a href="https://github.com/yourusername" class="icon">GitHub</a>
<a href="https://kaggle.com/yourusername" class="icon">Kaggle</a>
```

### Update CV Page
In `aboutme.html`, replace the `src` of the `<iframe>` with your own CV website URL:
```html
<iframe src="https://your-cv-website.github.io/" ...></iframe>
```

### Change Theme Color
The global accent color `#f0a500` (golden) is used throughout `styles.css`. Use Find & Replace to change it to any color of your choice.

---

## Connect with Me

| Platform | Link |
|---|---|
| 🌐 CV Website | [subhamgrv.github.io/CV_website](https://subhamgrv.github.io/CV_website/) |
| 💼 LinkedIn | [linkedin.com/in/subhamgrv](https://www.linkedin.com/in/subhamgrv/) |
| 🐙 GitHub | [github.com/subhamgrv](https://github.com/subhamgrv) |
| 📊 Kaggle | [kaggle.com/subhamgrv](https://www.kaggle.com/subhamgrv/) |

---

<p align="center">Deployed on <strong>GitHub Pages</strong> · Built with ❤️ by <strong>Subham Gaurav</strong></p>
