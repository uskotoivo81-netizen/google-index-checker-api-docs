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

### 2\. Task Creation

Create a new bulk task for indexing or checking.

**Method:** POST**Endpoint:** /v2/task/{SEARCH\_ENGINE}/{TASK\_TYPE}/create

**Path Parameters:**

*   SEARCH\_ENGINE: google or yandex
    
*   TASK\_TYPE: indexer (for indexing) or checker (for status check)
    

**Request Body:**

*   title (string, optional): Task name.
    
*   urls (array of strings): List of links (Max 10,000 per request).
    

**Example Request:**

codeBash

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   curl -X POST -H 'Authorization: YOUR_API_KEY' -H 'Content-Type: application/json' \  -d '{"title":"Campaign_1", "urls":["https://google.com","https://google.ru"]}' \  https://api.speedyindex.com/v2/task/google/indexer/create   `

**Response Codes:**

*   0: Success
    
*   1: Insufficient funds
    
*   2: Server overloaded (retry later)

