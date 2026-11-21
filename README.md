# Naukri Job Scraper | India & Gulf Jobs: Naukri Scraper API for Python & Node.js (2026)

Scrape Naukri.com and Naukri Gulf job listings: title, company, salary, experience, skills, location and description. No login needed. Export to JSON or CSV.

**[▶ Try the Naukri Job Scraper | India & Gulf Jobs free on Scrapely](https://scrape.ly/store/openrole/naukri-job-scraper)** · [Compare Scrapely vs other scraping tools](https://scrape.ly/compare)

This repository shows how to scrape Naukri data with the [Naukri Job Scraper | India & Gulf Jobs](https://scrape.ly/store/openrole/naukri-job-scraper) using the official
**Scrapely SDKs for JavaScript and Python**. You pass the input, Scrapely runs the naukri scraper in the cloud
(proxies, retries, browser and scaling included) and returns clean, structured data as JSON, CSV or Excel.
No scraper code to maintain and no blocked requests to debug.

## Why use this Naukri scraper

- **No-code or API:** run it from the [Scrapely Store](https://scrape.ly/store/openrole/naukri-job-scraper) or from your code with the SDK.
- **Structured naukri data:** ready-to-use fields instead of raw HTML.
- **Pay per result:** $0.34 per 1,000 job listing results, no monthly subscription required.
- **Maintained and monitored:** scrapers are tested around the clock and fixed fast when Naukri changes.
- **Integrations:** n8n, Make, Zapier, LangChain, LlamaIndex, MCP (Claude, Cursor) and webhooks.

## What Naukri data can you extract?

Scrape Naukri.com and Naukri Gulf job listings: title, company, salary, experience, skills, location and description. No login needed. Export to JSON or CSV.

| Output field |
|---|
| `title` |
| `companyName` |
| `location` |
| `experienceText` |
| `salary` |
| `jdURL` |
| `createdDate` |
| `jobId` |
| `jobBoard` |

## Quick start

1. [Sign up for Scrapely](https://scrape.ly) (free plan available) and copy your API token from
   **Settings → API & Integrations**.
2. Clone this repo and set your token:

```bash
export SCRAPELY_TOKEN=your_token
```

### Node.js (JavaScript SDK)

```bash
npm install
node example.js
```

```js
const { ScrapelyClient } = require('scrapely-client');
const client = new ScrapelyClient({ token: process.env.SCRAPELY_TOKEN });

const run = await client.actor('openrole/naukri-job-scraper').call({"keyword": "software developer", "jobBoard": "naukri", "maxJobs": 10, "proxyConfiguration": {"useScrapelyProxy": true, "scrapelyProxyGroups": ["DATACENTER"]}});
const { items } = await client.dataset(run.defaultDatasetId).listItems();
```

### Python (Python SDK)

```bash
pip install -r requirements.txt
python example.py
```

```python
from scrapely_client import ScrapelyClient
client = ScrapelyClient(os.environ['SCRAPELY_TOKEN'])

run = client.actor('openrole/naukri-job-scraper').call(run_input={ "keyword": "software developer", "jobBoard": "naukri", "maxJobs": 10, "proxyConfiguration": { "useScrapelyProxy": True, "scrapelyProxyGroups": [ "DATACENTER" ] } })
items = list(client.dataset(run.default_dataset_id).iterate_items())
```

### REST API / cURL

```bash
curl -X POST "https://api.scrape.ly/v2/acts/openrole~naukri-job-scraper/run-sync-get-dataset-items?token=$SCRAPELY_TOKEN" \
  -H "Content-Type: application/json" \
  -d @input.json
```

## Example input

```json
{
  "keyword": "software developer",
  "jobBoard": "naukri",
  "maxJobs": 10,
  "proxyConfiguration": {
    "useScrapelyProxy": true,
    "scrapelyProxyGroups": [
      "DATACENTER"
    ]
  }
}
```

See every input option on the [Naukri Job Scraper | India & Gulf Jobs page](https://scrape.ly/store/openrole/naukri-job-scraper).

## Pricing

**$0.34 per 1,000 job listing results.** Free plan available, no credit card needed to start. Check current pricing on the
[Store page](https://scrape.ly/store/openrole/naukri-job-scraper) and see how Scrapely compares with other tools on [scrape.ly/compare](https://scrape.ly/compare).

## FAQ

**How do I scrape Naukri with Python?** Install `scrapely-client-python`, set `SCRAPELY_TOKEN` and run
`example.py`. The scraper runs on Scrapely and you read the results from the dataset.

**How do I scrape Naukri with Node.js?** Install `scrapely-client`, set `SCRAPELY_TOKEN` and run `example.js`.

**Is there a naukri scraper API?** Yes. Call `POST https://api.scrape.ly/v2/acts/openrole~naukri-job-scraper/runs`
or use `run-sync-get-dataset-items` to get results in one request.

**Do I need proxies?** No. Proxies, retries and browsers are handled by Scrapely.

**Is scraping Naukri legal?** This scraper collects publicly available data. Check Naukri's terms and the
laws that apply to you, especially for personal data (GDPR, CCPA).

**Can I schedule it or get results by webhook?** Yes. Use Scrapely schedules and webhooks, or n8n, Make and Zapier.

## Looking for an alternative?

Scrapely is an alternative to Apify, Bright Data, ScraperAPI, Firecrawl, Octoparse, PhantomBuster, SerpApi,
Zyte and others. See the side-by-side pricing on [scrape.ly/compare](https://scrape.ly/compare).

---

**Keywords:** naukri job scraper | india & gulf jobs, naukri scraper, naukri scraper api, naukri scraper python, naukri scraper node.js,
scrape naukri, naukri data extraction, naukri crawler, naukri api, export naukri data to csv, naukri-job-scraper

License: MIT. Example code only; the scraper runs on [Scrapely](https://scrape.ly/store/openrole/naukri-job-scraper).
