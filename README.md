# 📧 Profile Email Finder

**Profile Email Finder** is a Python-based tool that uses the Google Custom Search API to discover publicly listed email addresses from online professional profiles (e.g., LinkedIn, academic pages) and exports the results to a clean Excel `.xlsx` file.

> ⚠️ This tool is intended for educational, academic research, or ethical recruiting purposes. Please **do not use it to scrape or spam**. Respect privacy and platform terms of service.

---

## 🚀 Features

- 🔎 Search public profiles using a Google CSE query
- 📬 Automatically extracts email addresses using regex
- 📊 Outputs Name, Profile Link, Snippet, Email, Organization, Location, and Role
- 📁 Exports all data into a timestamped `.xlsx` spreadsheet
- 🔐 Uses `.env` for secure API key storage

---

## 🛠️ Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/profile-email-finder.git
cd profile-email-finder
```

### 2. Create a Virtual Environment (optional but recommended)
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Set Up Your `.env` File
Create a `.env` file in the root directory with your Google API credentials:
```env
GOOGLE_API_KEY=your_google_api_key_here
GOOGLE_CSE_ID=your_custom_search_engine_id_here
```

📘 [How to create a CSE + API Key](https://developers.google.com/custom-search/v1/overview)

---

## ✅ Example Usage

### Basic:
```bash
python email_finder.py "site:linkedin.com/in AND 'data scientist' AND 'Tesla'" --requests 2
```

This will:
- Run 2 batches (10 results each) = 20 profile searches
- Search for public profiles that match your query
- Extract and save emails into `results_YYYYMMDD_HHMMSS.xlsx`

---

## 📂 Output Example

| Name             | Profile Link                | Snippet         | Org     | Location | Role        | Email              |
|------------------|-----------------------------|------------------|----------|-----------|--------------|---------------------|
| Jane Doe         | linkedin.com/in/janedoe     | ...              | Meta     | NYC       | Data Scientist | jane.doe@example.com |

---

## 📌 Notes and Limitations

- Google API free quota: **100 searches/day**
- Emails are only found if **publicly listed** in the profile/snippet
- CSE must be configured to search `linkedin.com` or other sites
- This tool does **not** scrape LinkedIn directly — it uses Google

---

## 🙏 Disclaimer

This tool is meant for **ethical and educational purposes** only.  
You are responsible for how you use the data. Respect privacy, platform rules, and people’s inboxes.

---

## 👨‍💻 Author

**Atharva Prakash Patil**  
📫 apatil23@binghamton.edu  
🔗 [LinkedIn](https://linkedin.com/in/your-link) | [GitHub](https://github.com/yourusername)

---

## 📄 License

This project is licensed under the MIT License. See `LICENSE` file for details.
