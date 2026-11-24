# 🚀 Media Trend Analysis & AI Content Generation Agent

An AI-powered platform that discovers trending topics, analyzes social media discussions, and automatically generates engaging content and landing pages using intelligent scraping, Reinforcement Learning (RL), and Large Language Models (LLMs).

<p align="center">

**Discover Trends · Analyze Insights · Generate Content · Build Landing Pages**

</p>

---

## 📌 Overview

The **Media Trend Analysis & AI Content Generation Agent** automates the process of identifying trending topics and transforming them into actionable content strategies.

Users can enter a niche or keyword, select their preferred data sources, and initiate an intelligent pipeline that collects trend-related information, evaluates scraping strategies, identifies relevant trends, and generates social media content and landing pages.

The platform combines CrewAI, Reinforcement Learning-based scraping, machine learning, and hosted LLM inference to streamline content research and creation.

## ✨ Key Features

### 🔍 1. Intelligent Trend Discovery
- Collects trend-related information from YouTube and Twitter-related search results.
- Supports keyword-based trend research.
- Extracts relevant information for further analysis.

### 🤖 2. RL-Based Adaptive Scraping
- Uses an RL-based decision process to select scraping strategies.
- Evaluates scraping results using reward-based feedback.
- Adjusts subsequent scraping actions based on collected results.
- Supports multiple scraping strategies, including YouTube and Twitter search.

### 📊 3. Trend Analysis
- Processes collected information.
- Uses TF-IDF-based text feature extraction.
- Identifies relevant topics and potential trending subjects.
- Helps transform raw search results into meaningful insights.

### ✍️ 4. AI-Powered Content Generation
- Generates social media content based on identified trends.
- Uses CrewAI to organize content-generation workflows.
- Produces content tailored to the selected niche.

### 🌐 5. AI Landing Page Generation
- Generates landing page content using AI.
- Converts trend insights into structured marketing-oriented content.

### 💾 6. Database Integration
- Uses SQLite for storing application information.
- Maintains execution and generation logs.

### ☁️ 7. Cloud Deployment
- Deployed using Streamlit Community Cloud.
- Uses Groq-hosted LLM inference.
- Stores API credentials securely through Streamlit Secrets.

---

## 🏗️ System Architecture

```text
                 USER INPUT
                     |
                     v
          Streamlit User Interface
                     |
                     v
              Main Pipeline
                     |
                     v
          RL-Based Scraping Agent
                     |
          +----------+----------+
          |                     |
          v                     v
    YouTube Scraper       Twitter Search
          |                     |
          +----------+----------+
                     |
                     v
             Collected Results
                     |
                     v
               Trend Analysis
                     |
                     v
             TF-IDF Processing
                     |
                     v
              Identified Trends
                     |
          +----------+----------+
          |                     |
          v                     v
    Content Generation    Landing Page
       (CrewAI)             Generation
          |                     |
          v                     v
     Social Content       Landing Page
          |                     |
          +----------+----------+
                     |
                     v
               SQLite Database
```

---

## 🛠️ Technology Stack

| Category | Technologies |
|---|---|
| Programming Language | Python |
| Frontend | Streamlit |
| AI Framework | CrewAI |
| Large Language Model | GPT-OSS 20B via Groq |
| Machine Learning | Scikit-learn |
| Text Processing | TF-IDF |
| Data Collection | YouTube Data API, DuckDuckGo search |
| Database | SQLite |
| Deployment | Streamlit Community Cloud |
| Version Control | Git, GitHub |

---

## 📂 Project Structure

```text
MEDIA-TREND-ANALYSIS-AND-CONTENT-GENERATION-AI-AGENT/
│
├── app.py
│
├── main.py
│
├── trend_agent.py
│
├── rl_scraper.py
│
├── youtube_scraper.py
│
├── twitter_scraper.py
│
├── content_crew.py
│
├── landing_crew.py
│
├── db.py
│
├── requirements.txt
│
└── README.md
```

### File Descriptions

| File | Responsibility |
|---|---|
| `app.py` | Streamlit application and user interface |
| `main.py` | Coordinates the complete application pipeline |
| `trend_agent.py` | Analyzes collected data and identifies trends |
| `rl_scraper.py` | Manages adaptive scraping strategies |
| `youtube_scraper.py` | Collects YouTube-related trend information |
| `twitter_scraper.py` | Collects Twitter-related search information |
| `content_crew.py` | Generates AI-powered social media content |
| `landing_crew.py` | Generates landing page content |
| `db.py` | Handles SQLite database initialization and logging |
| `requirements.txt` | Contains project dependencies |

---

## ⚙️ How It Works

**Step 1: User Input**

The user enters a niche or keyword and selects the required data sources.

**Step 2: Intelligent Scraping**

The scraping agent selects appropriate scraping strategies to collect information from the selected sources.

**Step 3: Reward-Based Evaluation**

The RL-based scraping process evaluates the collected results and uses reward feedback to guide subsequent actions.

**Step 4: Trend Identification**

The collected information is processed using text analysis and TF-IDF feature extraction to identify relevant trends.

**Step 5: Content Generation**

CrewAI coordinates the content-generation workflow using the identified trends and a hosted LLM.

**Step 6: Landing Page Generation**

The landing page generation workflow transforms the identified trends into structured landing page content.

**Step 7: Database Logging**

Application execution and generation information are recorded using SQLite.

---

## 🚀 Installation & Local Setup

### 1. Clone the Repository

```bash
git clone https://github.com/Akshayreddy0910/MEDIA-TREND-ANALYSIS-AND-CONTENT-GENERATION-AI-AGENT.git
```

### 2. Navigate to the Project

```bash
cd MEDIA-TREND-ANALYSIS-AND-CONTENT-GENERATION-AI-AGENT
```

### 3. Create a Virtual Environment

```bash
python -m venv venv
```

Activate it:

**Windows:**
```bash
venv\Scripts\activate
```

**Linux / macOS:**
```bash
source venv/bin/activate
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

### 5. Configure Environment Secrets

The application requires API credentials for YouTube data collection and Groq-powered LLM inference.

For local execution, configure the required credentials securely. For Streamlit Cloud, use the application's Secrets settings.

Required secrets:

```toml
YOUTUBE_API_KEY = "your_youtube_api_key"
GROQ_API_KEY = "your_groq_api_key"
```

Never commit API keys or other sensitive credentials to GitHub.

### 6. Run the Application

```bash
streamlit run app.py
```

The application will be available locally at:

```text
http://localhost:8501
```

---

## ☁️ Deployment

The project is deployed using **Streamlit Community Cloud**.

Deployment process:

1. Push the project to GitHub.
2. Connect the GitHub repository to Streamlit Community Cloud.
3. Select `app.py` as the application entry point.
4. Configure the required API credentials in Streamlit Secrets.
5. Deploy the application.

The deployed application provides browser-based access without requiring users to install the project locally.

---

## 🔐 API Configuration

| API | Purpose |
|---|---|
| YouTube Data API | YouTube trend and video-related information |
| Groq API | Hosted LLM inference for content and landing page generation |

Twitter-related search collection uses the project's DuckDuckGo-based search implementation rather than requiring direct Twitter API authentication.

---

## 🎯 Project Objectives

- Automate trend discovery and content research.
- Reduce manual effort in social media content planning.
- Apply reward-based feedback to adaptive scraping decisions.
- Combine machine learning and LLMs in a unified application.
- Generate content and landing page material from identified trends.
- Provide an accessible cloud-based application.

---

## 🔮 Future Enhancements

- Integrate additional social media platforms.
- Improve trend ranking and relevance scoring.
- Introduce advanced trend visualization dashboards.
- Add sentiment analysis and audience engagement insights.
- Support scheduled trend monitoring.
- Enhance content personalization.
- Implement persistent cloud database storage.

---

## 👨‍💻 Author

**Akshay Reddy**

GitHub: [@Akshayreddy0910](https://github.com/Akshayreddy0910)

---

## ⭐ Support

If you find this project interesting, consider giving the repository a ⭐ on GitHub!

**Built with Python, AI, Machine Learning, CrewAI and LLMs.**
