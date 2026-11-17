# Task 3: 20 Advanced Search Operators Cheat Sheet (Google & Bing)

**Investigator:** Alhasan Mohammed Turki

**Track:** Nexlevr OSINT Investigator Internship (Beginner Track)

**Purpose:** Open-source intelligence (OSINT) and market research reference guide for competitor tracking, customer sentiment discovery, and public document enumeration.

## 1. The 20 Advanced Search Operators

| \# | Operator | Engine | Market Research Use Case | Ready-to-Run Example Query | 
| ----- | ----- | ----- | ----- | ----- | 
| 1 | `"exact phrase"` | Google & Bing | Track exact brand names, slogans, or product mentions without fuzzy word substitutions. | `"Dade Restaurant" "Duhok"` | 
| 2 | `site:` | Google & Bing | Restrict searches to a specific website, competitor domain, or social media platform. | `site:instagram.com "daderestaurant"` | 
| 3 | `filetype:` / `ext:` | Google & Bing | Discover public PDFs, market research reports, price lists, and pitch decks. | `"Kurdistan" "restaurant market" filetype:pdf` | 
| 4 | `intitle:` | Google & Bing | Find comparison reviews or articles featuring a target keyword directly in the page title. | `intitle:"best restaurants in Duhok"` | 
| 5 | `allintitle:` | Google & Bing | Require every listed keyword to appear inside the HTML title tag for high-relevance pages. | `allintitle:SaaS pricing benchmark report 2026` | 
| 6 | `inurl:` | Google & Bing | Locate specific page types such as `/pricing`, `/menu`, `/case-study`, or `/careers`. | `site:hubspot.com inurl:case-study` | 
| 7 | `allinurl:` | Google & Bing | Require multiple structural keywords inside the URL path to map site architecture. | `allinurl:blog enterprise security guide` | 
| 8 | `intext:` / `inbody:` | Google (`intext:`) / Bing (`inbody:`) | Force target keywords to appear inside the main body text rather than menus or sidebars. | `intext:"annual recurring revenue" "fintech"` | 
| 9 | `allintext:` | Google & Bing | Ensure all listed terms appear together within the page body for deep niche research. | `allintext:customer churn survey B2B SaaS` | 
| 10 | `-` (Exclusion) | Google & Bing | Exclude a brand's own domain to isolate independent third-party reviews and press. | `"Shopify" review -site:shopify.com` | 
| 11 | `OR` / `|` | Google & Bing | Monitor multiple competitors, product categories, or regional spellings in a single query. | `("Duhok" OR "Dohuk") "German doner"` | 
| 12 | `AROUND(X)` / `near:X` | Google (`AROUND`) / Bing (`near`) | Proximity search finding two terms within `X` words of each other for sentiment analysis. | `"Stripe" AROUND(5) "fees"` | 
| 13 | `*` (Wildcard) | Google & Bing | Fill in unknown words in common buyer discovery, migration, or comparison phrases. | `"switched from * to" "PostgreSQL"` | 
| 14 | `before:` | Google | Inspect historical announcements, legacy pricing, or pre-pivot positioning before a date. | `"OpenAI" "enterprise" before:2024-01-01` | 
| 15 | `after:` | Google | Capture recent product launches, funding rounds, or post-release customer feedback. | `"cybersecurity startup" "Series A" after:2026-01-01` | 
| 16 | `..` (Numeric Range) | Google & Bing | Filter results containing numbers within a specific price bracket, year, or headcount range. | `"CRM software" "$20..$100" per user` | 
| 17 | `inanchor:` | Google & Bing | Find pages linked to with specific anchor text to see how external sites describe a brand. | `inanchor:"best OSINT tools"` | 
| 18 | `site:*.domain.com -www` | Google & Bing | Enumerate public subdomains (e.g., `docs.`, `status.`, `app.`) to map a company's tech stack. | `site:*.vercel.app "daderestaurant"` | 
| 19 | `loc:` | Bing | Restrict market research results to a specific country or region for local competitor mapping. | `"döner kebab" loc:IQ` | 
| 20 | `contains:` | Bing | Find web pages that link directly to specific file types (such as downloadable PDFs or CSVs). | `"ecommerce trends" contains:pdf` | 

## 2. Combined OSINT Query Chains for Market Research

* **1. Competitor Customer Pain-Point Discovery:**

  ```
  (site:reddit.com OR site:g2.com) "CompetitorName" ("too expensive" OR "switched from" OR "issue") -site:competitorname.com
  
  ```

* **2. Local Business Cross-Platform Footprint Lookup:**

  ```
  ("Dade Restaurant" OR "daderestaurant") ("Duhok" OR "Dohuk") -site:instagram.com
  
  ```

* **3. Unlisted Whitepapers & Industry Benchmarks:**

  ```
  "market report" "cybersecurity" (filetype:pdf OR filetype:xlsx) after:2025-01-01
  
  ```