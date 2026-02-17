# SpeedyIndex.com API – Google Index Checker & Indexing Service

[![SpeedyIndex](https://speedyindex.com/assets/img/logo.svg)](https://en.speedyindex.com/)

**SpeedyIndex** is a service designed to accelerate the indexing of links and websites in Google and Yandex search engines. This repository contains documentation and usage examples for integrating the service into your projects.

## 🚀 Features

With the SpeedyIndex API, you can automate the following processes:

*   **Accelerate indexing** of links in Google.
*   **Accelerate indexing** of websites in Yandex.
*   **Check Google indexing status** of pages via our [Google Index Checker](https://en.speedyindex.com/google-index-checker/).
*   **Check Bing indexing status** of pages via our [Google Index Checker](https://en.speedyindex.com/bing-index-checker/).
*   **Check Yandex indexing status** of pages via our [Yandex Index Checker](https://en.speedyindex.com/google-index-checker/).
*   **Re-index** pages.
*   **Export links** from a Sitemap.

## 📋 Description

The API allows developers and SEO specialists to programmatically submit links for indexing and check their status without manually using the web interface or Telegram bot. This is the ideal solution for creating custom scripts, CMS plugins, or bulk link processing.

> **Bonus:** Get 100 free links to test the service upon registration.

## 🛠 Getting Started

All API requests require an API Key. You can find your API Key in the <a href="https://t.me/speedyindexbot" title="SpeedyIndex bot" rel="nofollow">Telegram bot settings</a> or <a href="https://app.speedyindex.com/" title="Web-version app SpeedyIndex" rel="nofollow">your personal cabinet</a>.

For full technical details, refer to the official documentation page:
[https://en.speedyindex.com/api.php](https://en.speedyindex.com/api.php)

### Usage Examples

#### 1. Submit Links for Indexing

**Endpoint:** `POST /add-task`

**Parameters:**
*   `key`: Your API Key.
*   `service`: Service type (e.g., `google`).
*   `links`: Array of links or text list.

**cURL Request:**
```bash
curl -X POST https://api.speedyindex.com/v1/add-task \
     -H "Content-Type: application/json" \
     -d '{
           "key": "YOUR_API_KEY",
           "service": "google",
           "links": [
             "https://example.com/page1",
             "https://example.com/page2"
           ]
         }'

2. Check Balance
Endpoint: GET /balance

Response Example:

JSON
{
  "status": "success",
  "balance": 1500,
  "currency": "links"
}

📦 SDK & Libraries
Official libraries are currently in development. You can use any HTTP client (Axios, Guzzle, Requests) to interact with the API.

Python Example
Python
import requests

url = "https://api.speedyindex.com/v1/add-task"
payload = {
    "key": "YOUR_API_KEY",
    "service": "google",
    "links": ["https://site.com/url1", "https://site.com/url2"]
}

response = requests.post(url, json=payload)
print(response.json())
📞 Support & Contacts
If you have any questions regarding the API or integration:

Telegram Support: @speedyindex
Official Website: en.speedyindex.com


📄 License
API usage is subject to the Terms of Service.
## 🔌 API Documentation

### Base URL
