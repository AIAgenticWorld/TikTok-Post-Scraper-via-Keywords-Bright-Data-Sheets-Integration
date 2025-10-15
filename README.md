<img width="713" height="146" alt="image" src="https://github.com/user-attachments/assets/e72c66e3-fb13-4fe1-bfe3-eb19bd714bf0" />

# 🔍 TikTok Scraper Workflow (via n8n + Bright Data + Google Sheets)

Easily automate keyword-based TikTok post scraping and store results in Google Sheets using this powerful workflow powered by **n8n**, **Bright Data**, and **Google Sheets API**.

---

## 🔄 How It Works

This workflow operates through a simple, automated process:

1. 📝 **Keyword Input**: User submits search keywords via a web form
2. 📡 **Data Scraping**: Bright Data searches TikTok for posts matching keywords
3. 🔁 **Processing Loop**: Monitors scraping progress until complete
4. 📂 **Data Storage**: Extracted post data is saved into Google Sheets
5. 📬 **Result Delivery**: Provides full post data including metrics, user info, and media URLs

---

## ⏱️ Setup Information

**Estimated Setup Time**: *10-15 minutes*  
Most of the process is automated once credentials and IDs are configured.

---

## ✨ Key Features

- 🔍 **Keyword-Based Search** – Scrape TikTok content by keyword
- 📊 **Comprehensive Data Extraction** – Post stats, captions, user info, video URLs
- 📋 **Google Sheets Integration** – Auto-populates a spreadsheet with results
- 🔁 **Automated Workflow** – Fully monitored progress and error handling
- 🛠️ **Powered by Bright Data** – Reliable scraping infrastructure
- ⚡ **Live Updates** – Real-time progress and completion detection

---

## 📊 Data Extracted

| Field | Description | Example |
|-------|-------------|---------|
| `url` | TikTok post URL | `https://www.tiktok.com/@user/video/123456` |
| `post_id` | Unique post ID | `7234567890123456789` |
| `description` | Post caption | `Check out this amazing content! #viral` |
| `digg_count` | Likes | `15400` |
| `share_count` | Shares | `892` |
| `comment_count` | Comments | `1250` |
| `play_count` | Views | `125000` |
| `profile_username` | Creator handle | `@creativity_master` |
| `profile_followers` | Follower count | `50000` |
| `hashtags` | Hashtags used | `#viral #trending #fyp` |
| `create_time` | Timestamp | `2025-01-15T10:30:00Z` |
| `video_url` | Direct video URL | `https://video.tiktok.com/tos/...` |

---

## 🚀 Setup Instructions

### Step 1: ✅ Prerequisites

- n8n instance (self-hosted or cloud)
- Bright Data account with TikTok scraping access
- Google account with Sheets access
- Basic knowledge of n8n workflows

### Step 2: 📥 Import Workflow

1. Copy the provided JSON code  
2. In n8n: **Workflows → + Add workflow → Import from JSON**  
3. Paste and **Import**

---

### Step 3: 🔐 Configure Bright Data

- Go to **n8n → Credentials → + Add Credential → Bright Data API**
- Add your Bright Data API key
- Test connection to verify
- Update the workflow node:
  - Replace `BRIGHT_DATA_API_KEY` with your key
  - Dataset ID: `gd_lu702nij2f790tmv9h`

---

### Step 4: 📗 Connect Google Sheets

- Create or use an existing Google Sheet
- Copy the **Sheet ID** from the URL
- In n8n: **Credentials → + Add Credential → Google Sheets OAuth2 API**
- Complete OAuth setup and test
- Update workflow:
  - Sheet ID = your copied ID
  - Tab name must be: `Tiktok by keyword`

---

### Step 5: 🧪 Test the Workflow

1. **Activate** the workflow using the toggle
2. Visit the **Form Trigger URL**
3. Enter a test keyword (e.g., `viral dance`)
4. Wait 2-5 minutes for scraping and processing
5. Check Google Sheet for results 🎉

---

## ⚙️ Configuration Details

### Bright Data API

- **Dataset ID**: `gd_lu702nij2f790tmv9h`
- **Discovery Type**: `discover_new`
- **Search Method**: `keyword`
- **Results per Input**: `2`
- **Include Errors**: `true`

### Workflow Parameters

- **Wait Time**: `1 minute`
- **Status Checks**: Repeats until complete
- **Error Handling**: Auto-retry if incomplete

---

## 🧠 Usage Guide

### How to Run

1. Access the **Form Trigger URL**
2. Submit your keyword(s)
3. Wait for workflow execution
4. View results in your Google Sheet

### Best Practices

- 🎯 Use relevant keywords for accuracy
- 📉 Monitor Bright Data credit usage
- 📤 Backup Google Sheets regularly
- 🧪 Test with simple keywords first
- ✅ Validate extracted data manually

---

## 🛠️ Troubleshooting

| Issue | Solution |
|-------|----------|
| ❌ Scraping not starting | Check Bright Data credentials, dataset ID, and credit balance |
| ❌ No data in Google Sheets | Verify credentials, Sheet ID, and sheet tab name |
| ⏳ Workflow timeout | Increase wait time; confirm scraping is progressing on Bright Data |

---

## 📈 Use Cases

- 📌 **Content Research** – Find trending TikTok topics
- 🕵️ **Competitor Analysis** – Monitor others’ content and engagement
- 💼 **Influencer Discovery** – Identify creators in specific niches
- 📊 **Market Intelligence** – Track trends and hashtag performance

---

## 🔒 Security Notes

- Keep API credentials **private**
- Use strict sharing settings on Google Sheets
- Monitor Bright Data API usage
- Rotate API keys periodically
- Always comply with TikTok’s **Terms of Service**

---

## 🎉 You're Ready!

Your TikTok scraping workflow is now live! 🚀  
Use it to gather insights, discover trends, or analyze the TikTok landscape.

---
