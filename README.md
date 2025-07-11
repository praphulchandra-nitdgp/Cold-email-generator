
# 📧 Cold Email Generator

A smart AI-powered tool that scrapes job listings from company career pages, extracts essential job information, and generates **personalized cold emails** tailored to company services — helping you approach potential clients with relevance and efficiency.

---

## 🚀 Features

- 🔍 **Web Scraping**: Extracts job data directly from company career URLs.
- 🤖 **AI Job Extraction**: Parses scraped content to extract job title, experience, description, and required skills.
- 🧠 **Smart Portfolio Matching**: Queries your own portfolio using [ChromaDB](https://docs.trychroma.com/) to find relevant work.
- ✉️ **Cold Email Generation**: Generates custom cold emails positioning your company as the best solution provider.
- 🖼️ **Streamlit Interface**: Simple and clean web UI for entering job URLs and getting emails.

---

## 📌 Use Cases

- **Sales Teams**: Automate tailored outreach to hiring companies.
- **Freelancers / Agencies**: Market your services based on job postings.
- **Job Hunters**: Generate personalized messages to recruiters (with minor tweaks).
- **Developers**: Learn how LLMs and vector DBs can be used together in real-world use cases.

---

## 🧩 Problem Statement

> Reaching out to potential clients via cold email is a powerful business tool — but writing customized emails that reflect the client's needs takes **time and research**.

This project **automates** that by:
1. **Scraping** job openings.
2. **Extracting** skills & requirements.
3. **Matching** your project portfolio.
4. **Generating** emails to pitch your company as a solution provider.

---

## ⚙️ Tech Stack

- **Frontend**: [Streamlit](https://streamlit.io)
- **Backend**: [LangChain](https://www.langchain.com), [Groq](https://groq.com/)
- **Vector Store**: [ChromaDB](https://www.trychroma.com/)
- **LLM**: `llama3-70b-8192` via `ChatGroq`
- **Web Scraping**: `WebBaseLoader` from LangChain
- **Data Storage**: CSV-based portfolio

---

## 🛠️ Getting Started

### 1. **Clone the Repo**

```bash
git clone https://github.com/praphulchandra-nitdgp/Cold-email-generator.git
cd Cold-email-generator/app
```

---

### 2. **Set Up Python Environment**

Make sure Python 3.9+ is installed.

```bash
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows
pip install -r requirements.txt
```

---

### 3. **Set Up Environment Variables**

Create a `.env` file in `/app` directory:

```
GROQ_API_KEY=your_groq_api_key_here
```

> 🔐 You can get a Groq API key from: https://console.groq.com/keys

---

### 4. **Add Your Portfolio**

Edit the file:

```
/app/resource/my_portfolio.csv
```

With the following format:

| Techstack                  | Links                                  |
|---------------------------|----------------------------------------|
| Python, NLP, Flask        | https://github.com/your/project1       |
| React, Node.js, Tailwind  | https://github.com/your/project2       |

This file is used for similarity search using ChromaDB.

---

### 5. **Run the App**

```bash
streamlit run main.py
```

---

## 💡 Example Workflow

1. Paste a career/job page URL.
2. App scrapes & parses job info.
3. App queries your portfolio for matching tech stack.
4. App generates a cold email from [YOUR NAME] - [YOUR POSITION] with your work links embedded.

---

## 🔐 ChromaDB Storage (Vectorstore)

ChromaDB persists embeddings of your portfolio locally.

- Storage Path: `vectorstore/`
- You don’t need a public API key — it’s all local.
- If starting fresh: Chroma will auto-ingest the CSV.

---

## 📸 Screenshots

> _Add a screenshot here by placing the image in the repo and linking it like below:_

```markdown
![Cold Email Output](screenshots/email_output.png)
```

---

## 🧠 Future Improvements

- [ ] Add support for multiple email templates
- [ ] Email preview with Gmail-style UI
- [ ] Auto-send option via SMTP
- [ ] Portfolio management interface

---

## 🤝 Acknowledgments

- [LangChain](https://www.langchain.com)
- [Streamlit](https://streamlit.io)
- [Groq](https://groq.com)
- [ChromaDB](https://www.trychroma.com)

---

## 🧑‍💻 Author

Made with ❤️ by [Ganapathri Praphul Chandra](https://www.linkedin.com/in/praphul-chandra-ganapathri-018a692a8/)
