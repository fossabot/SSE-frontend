# 🌱 Rently Frontend — SSE Version
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Fredyz13%2FSSE-frontend.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2Fredyz13%2FSSE-frontend?ref=badge_shield)


## 📌 Overview

This repository contains the **frontend of the Rently project**, originally developed by students of the Software Engineering course.
We forked the original project (full credit to the authors: [https://github.com/rently-unisa/front-end](https://github.com/rently-unisa/front-end)) and extended it as part of the **Sustainable Software Engineering (SSE)** course.

The objective of this work is to **evaluate and improve the environmental and performance sustainability** of the frontend using the tools introduced during the course.

The repository includes three branches used during the analysis:

```
├─ baseline/            # version before sustainability evaluations
├─ sse-improvements/    # version after sustainability enhancements
└─ main                 # final integrated frontend
```

Experiment logs, tool outputs, and structured reports are stored under:

```
sse-reports/
   ├─ baseline/
   └─ sse-improvements/
```

Each directory contains:

* Raw tool results
* Screenshots
* Analysis notes

---

## 🌍 Sustainability Tools

As part of the SSE course activities, the frontend was evaluated using the tools presented during the laboratory sessions.
Each tool contributes to a different dimension of software sustainability.

---

### 🌐 **WebsiteCarbon**

WebsiteCarbon estimates the environmental impact of a public web page.
It provides metrics such as:

* CO₂ emitted per page view
* Estimated yearly emissions
* Grade (A+–F)
* Green hosting classification
* Comparison with other tested sites

In this project, WebsiteCarbon was used to evaluate the deployed version of the frontend hosted via GitHub Pages.

---

### 🍃 **EcoIndex**

EcoIndex analyzes web pages by estimating their environmental footprint based on:

* DOM complexity
* Number of HTTP requests
* Total page weight

EcoIndex generates indicators such as:

* EcoIndex score (0–100)
* Grade (A–G)
* Water consumption
* Greenhouse gas emissions

The tool was applied to the deployed frontend entrypoint to evaluate its environmental sustainability.

---

### 🖼️ **GreenIT-Analysis**

GreenIT-Analysis is a browser extension that evaluates the environmental impact and performance characteristics of individual web pages.
For the frontend, it provides insights on:

* DOM complexity
* Media and image optimization
* CSS/JS weight
* Page loading impact
* Recommendations for reducing resource usage

Because the frontend is a Single Page Application (SPA), GreenIT-Analysis was also used to analyze different *logical views* of the application through forced reloads and navigation.

---
## 🐳 Running the Frontend with Docker

### 1️⃣ Create a `.env` file

The frontend uses only one environment variable:

```
REACT_APP_BACKEND_URL=http://localhost:4000
```

If not provided, the application defaults to:

```
http://localhost:4000
```

As defined in `api.js`:

```js
export const API_BASE =
  process.env.REACT_APP_BACKEND_URL || "http://localhost:4000";
```

---

### 2️⃣ Run the Frontend

```bash
docker compose up --build
```

This command starts:

* `frontend` → React development server (port 3000)

The application will be available at:

```
http://localhost:3000
```

---

## 👥 Credits

Original frontend authors: [https://github.com/rently-unisa/front-end](https://github.com/rently-unisa/front-end)


## License
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Fredyz13%2FSSE-frontend.svg?type=large)](https://app.fossa.com/projects/git%2Bgithub.com%2Fredyz13%2FSSE-frontend?ref=badge_large)