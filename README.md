# 🚀 BigQuery Release Notes Hub

A modern Flask-based dashboard that fetches, parses, filters, and presents **Google Cloud BigQuery release notes** in a clean, interactive interface.

Built to make technical product updates easier to discover, search, and share.

## ✨ Features

* 📡 **Live Release Feed** — Fetches official BigQuery release updates.
* 🧩 **Release Parsing** — Converts grouped Atom feed entries into individual release cards.
* 🔎 **Instant Search** — Search across release titles, descriptions, and categories.
* 🏷️ **Category Filters** — Organize updates by Feature, Announcement, Issue, Deprecated, and General.
* ⚡ **5-Minute Caching** — Reduces unnecessary requests while keeping information reasonably fresh.
* 🔄 **Manual Refresh** — Force a fresh fetch when required.
* 📱 **Responsive UI** — Designed for a clean experience across screen sizes.
* 𝕏 **Share to X** — Compose and share release updates through an interactive sharing modal.

## 🛠️ Tech Stack

**Backend**

* Python
* Flask
* Requests
* XML / Atom Feed Parsing

**Frontend**

* HTML5
* CSS3
* JavaScript

**Data Source**

* Official Google Cloud BigQuery Release Notes Atom Feed

## 🏗️ Project Structure

```text
bigquery-release-notes-hub/
│
├── app.py
├── README.md
├── .gitignore
│
├── screenshots/
│   └── dashboard.png
│
├── templates/
│   └── index.html
│
└── static/
    ├── css/
    │   └── style.css
    └── js/
        └── app.js
```

## ⚙️ How It Works

```text
Google Cloud BigQuery Release Feed
                ↓
        Flask Backend
                ↓
        XML / Atom Parsing
                ↓
       Release Normalization
                ↓
          5-Minute Cache
                ↓
          JSON API
                ↓
       Interactive Frontend
                ↓
       Search / Filter / Share
```

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/namratha31/bigquery-release-notes-hub.git
cd bigquery-release-notes-hub
```

### 2. Install dependencies

```bash
pip install flask requests
```

### 3. Run the application

```bash
python app.py
```

### 4. Open in your browser

```text
http://127.0.0.1:5000
```

## 🔌 API

### `GET /api/releases`

Returns parsed BigQuery release updates.

Optional parameter:

```text
/api/releases?refresh=true
```

Using `refresh=true` bypasses the existing cache and fetches the latest available release feed.

## 💡 What I Learned

This project helped me practice:

* Building a Flask backend
* Consuming external data feeds
* Parsing XML / Atom data
* Designing a simple caching mechanism
* Creating frontend filtering and search interactions
* Connecting frontend interfaces with backend APIs
* Structuring a small full-stack application

## 🔮 Future Improvements

* Add persistent caching with Redis or SQLite
* Add pagination for large release histories
* Add date-range filtering
* Add automated tests
* Deploy the application publicly
* Add scheduled background feed updates

## 📄 License

This project is licensed under the MIT License.
