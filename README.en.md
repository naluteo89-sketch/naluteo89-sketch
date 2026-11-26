**English** | [한국어](README.md)

# Hi, I'm Daun Kim 👋

### AI Service Developer — I build fast and verify with numbers

I build quickly with AI, then **verify the results with code rules and tests**.  
I raised a RAG chatbot's accuracy from **80% → 100%** by using rules to stop the LLM from inventing numbers and dates,  
and I keep fixing issues after release, **logging every version**.

### 📂 [Notion portfolio](https://kimdaun98y.notion.site/3cd651db82fb801392cff0e96b79994c) — detailed project write-ups and daily learning log (in Korean)

---

## 📂 Projects at a Glance

| Project | What it is | Key result |
|---|---|---|
| 🛍️ [you_HOWMUCH](https://github.com/naluteo89-sketch/I_sell_a_store) `In progress` · [🔗 Live demo](https://youhowmuch.beefalo-tiaki.ts.net/) | A shop built around products shown in YouTube review videos (web + app) | 13,709 products collected from 2,488 videos, list page 10.7MB → 116KB |
| 🎬 [5·18 Insert Cut](https://kimdaun98y.notion.site/415651db82fb81e0a09ac7adc62003b8) `Work` `In progress` | Empty-classroom 4K footage with the student removed | 8,362 frames matched, flicker 0.138 → 0.116, blackboard kept pixel-identical |
| 🧴 [Beauty AI Platform](https://kimdaun98y.notion.site/40d651db82fb814484c2d8554f49d0e4) `Work` | Two AI APIs for skin analysis and cosmetic label reading | Blemish agreement (rank correlation) 0.55 → 0.78, cost cut to 1/20 |
| 🏠 [BuBot](https://github.com/naluteo89-sketch/BuBot) ⭐ | Apartment price chatbot that shows its sources | Accuracy 80% → 100%, 191 automated tests |
| 📰 [news_Moa](https://github.com/naluteo89-sketch/news_Moa) | Naver news sentiment and keyword analysis | 1 AI call per page, 7/7 article body extraction |
| 🥽 [Pano360](https://github.com/naluteo89-sketch/co_show_2026) | A single photo to an 8K 360° image for Meta Quest 3 | 8192×4096, seam color gap 4.5× → 1.23× |
| 🐫 [Silkroad](https://github.com/naluteo89-sketch/Silkroad) | XR experience that turns your own drawing into a Silk Road style painting | 6-step flow, dummy mode for testing without a server |
| 📸 [ImgPls](https://github.com/naluteo89-sketch/ImgPls) | Kiosk that composites a portrait onto a new background and delivers it by QR | Moved to cloud, 10 API tests |
| 🕷️ [Smart Crawler](https://github.com/naluteo89-sketch/smart-crawler-extension) | One-click web data collection: Chrome extension + crawler | 1–2 LLM calls even for thousands of records |

---

## 💪 Strengths

| Strength | Detail |
|---|---|
| **Fast design from past experience** | For similar projects I reuse earlier experience for a stable, quick design and build in a day. The "code calculates, LLM interprets" structure proven in BuBot was reused for the Beauty AI scoring server |
| **Applying new technology** | I compare and measure unfamiliar models and platforms myself and carry them through to working results: an 8K 360° image for Quest 3 with FLUX.2, 8,362 frames of 4K background compositing, a web + Android app |
| **Maintainability** | I put tests in place first and then fix, changing structure and performance without breaking existing features: BuBot 191 tests, ImgPls cloud move and 10 API tests, list page 10.7MB → 116KB |

---

## 🧠 How I Solve Problems

| Step | What I do | Example |
|---|---|---|
| 1. Start from a real pain point | Write the problem down and compare why existing services fall short | news_Moa: existing tools focus on search-volume numbers, not on what articles actually say |
| 2. Split work between AI and code | Calculations and decisions that must be right go to code; interpretation and wording go to the LLM | BuBot: Python calculates prices, the LLM only explains / news_Moa: the model returns a ratio, code decides the label |
| 3. Measure first, then redesign | Check assumptions with inspection scripts and evaluation sets | news_Moa: confirmed 7/20 sites block iframes → switched to extracting article text directly |
| 4. Solve bottlenecks with structure | When hitting hardware or cost limits, change where or how much is processed | Pano360: generate only the moving region instead of full 4K / ImgPls: local GPU → Comfy Cloud |
| 5. Log and re-verify | Record symptom, cause and fix; prevent regressions with tests | BuBot: 191 tests, Pano360: regression tests against a fake backend |

---

## 🛠 Tech Stack

**Languages**  
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Java](https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black)
![C#](https://img.shields.io/badge/C%23-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat-square&logo=kotlin&logoColor=white)

**Frontend**  
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![Android](https://img.shields.io/badge/Android%20(Compose)-3DDC84?style=flat-square&logo=android&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS-1572B6?style=flat-square&logo=css3&logoColor=white)

**Backend**  
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)
![aiohttp](https://img.shields.io/badge/aiohttp-2C5BB4?style=flat-square&logo=aiohttp&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)

**Database**  
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=flat-square&logo=mariadb&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)

**AI · XR**  
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white)
![RAG](https://img.shields.io/badge/RAG-FF6F00?style=flat-square)
![ComfyUI](https://img.shields.io/badge/ComfyUI%20%2F%20Comfy%20Cloud-222222?style=flat-square)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![MediaPipe](https://img.shields.io/badge/MediaPipe-0097A7?style=flat-square)
![Unity](https://img.shields.io/badge/Unity-000000?style=flat-square&logo=unity&logoColor=white)
![Meta Quest](https://img.shields.io/badge/Meta%20Quest%203-0467DF?style=flat-square&logo=meta&logoColor=white)

**Tools**  
![VS Code](https://img.shields.io/badge/VS%20Code-007ACC?style=flat-square&logo=visualstudiocode&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)
![FFmpeg](https://img.shields.io/badge/FFmpeg-007808?style=flat-square&logo=ffmpeg&logoColor=white)

---

## 🔎 Project Details

Open **Details** under each project for the background and how I solved it.

### 🛍️ [you_HOWMUCH](https://github.com/naluteo89-sketch/I_sell_a_store) · YouTube Review Video Shop `In progress · 2026.11` · [🔗 Live demo](https://youhowmuch.beefalo-tiaki.ts.net/)

> A shop that automatically collects the products shown in YouTube review videos, so you can **watch the review and add the product to your cart on one screen** (web + Android app)

<details>
<summary><b>Details</b> · background, challenge, what I did, tech</summary>

- **Background**: People watch review videos before buying, but the product page and the review live in different places.
- **Challenge**: The YouTube API has a daily quota, so it can't be called per visitor. And simply translating the UI would show Korean creators and Korean products to English-speaking users.
- **What I did**
  - Built an automatic collector that finds products in video descriptions: **13,709 products from 2,488 videos**. Visitors only read the stored data.
  - Treated language as a **market switch**, not a translation: the English site shows only products collected from English-language videos, priced in dollars.
  - Changed the product list to send 40 items per page from the server, cutting the **page size from 10.7MB to 116KB**.
  - Login uses server sessions with CSRF checks, and failure messages don't reveal whether an account exists.
- **Tech**: Next.js 15, Spring Boot 3.5 (Java 21), MySQL 8, YouTube Data API, Android (Kotlin, Jetpack Compose)  
- **Details**: [Notion project page](https://kimdaun98y.notion.site/415651db82fb8199af20cb5a4e5b2c1e) (in Korean)

</details>

### 🕷️ Smart Crawler · One-Click Web Data Collection `2026.11`

> A Chrome extension and Python crawler: click one item in the browser and it **finds every similar item and downloads them as structured data**

<details>
<summary><b>Details</b> · background, challenge, what I did, tech</summary>

- **Background**: Collecting job posts or product lists meant hand-writing CSS selectors every time.
- **Challenge**: Letting an LLM find the items would be slow and costly. The only place an LLM is really needed is deciding what to name each value.
- **What I did**
  - Found records with a **rule-based method** (walk up from the clicked element and pick the most repeated sibling shape), so it works instantly without AI.
  - Sent only 6 sample records to the LLM for a field plan and applied that plan in the browser, so **thousands of records still take only 1–2 LLM calls**.
  - Handled JS-rendered pages and infinite scroll, and applied robots.txt compliance and request delays by default.
- **Tech**: Python, Playwright, pandas, Chrome Extension (Manifest V3), JavaScript, OpenAI

</details>

### 🧴 [Beauty AI Platform — AI Analysis](https://kimdaun98y.notion.site/40d651db82fb814484c2d8554f49d0e4) `Work project · 2026.10–11`

> Two AI analysis APIs: one **scores skin condition from a selfie**, the other **reads the full ingredient list from a cosmetic label photo** (client names withheld, code in a private repository)

<details>
<summary><b>Details</b> · background, challenge, what I did, tech</summary>

- **Background**: The goal was "analyze faces and labels with AI", but there was no standard for what counts as which score.
- **Challenge**: When the LLM gave scores directly, the same photo got different scores on each call, with no way to explain why.
- **What I did**
  - The LLM only reports what it sees per face zone; **scores and pass/caution decisions are computed by server rules**.
  - Compared against expert ratings for 107 people in a public dataset (AI Hub) and raised blemish rank correlation from **0.55 to 0.78**.
  - Compared models on the same validation set and cut **analysis cost to 1/20**; label ingredients were read **29 out of 29** on public samples.
- **Maintenance after close (Nov 19–23)**
  - Switched the label OCR helper from EasyOCR to PaddleOCR: dictionary-matched ingredients went from **8 to 364**, and time per image from 17.1 s to 3.7 s.
  - Added a concurrency cap with an immediate 503 (`Retry-After`) to the API: median response at 40 concurrent requests went from 29.6 s to 14.2 s, and batch analysis in the research web became **4.45–5.76×** faster.
  - Connected the in-house local LLM (vLLM) and cross-checked it against the current model on 100 face and 100 label images: **the same accuracy** against ground truth at zero cost, but about 5× slower, so it will be swapped in after recalibrating score tables and prompts.
- **Tech**: Python, Flask, OpenAI (vision), OpenCV, MediaPipe, PaddleOCR, vLLM (local LLM), AI Hub public data

</details>

### 🎬 [5·18 Insert Cut — 4K Video Editing](https://kimdaun98y.notion.site/415651db82fb81e0a09ac7adc62003b8) `Work project · 2026.10–`

> For a scene where a student turns into an AR character, I produce an **empty-classroom version of the 4K footage with only the student removed** (client and footage withheld)

<details>
<summary><b>Details</b> · background, challenge, what I did, tech</summary>

- **Background**: To add a new 3D character, the area the student walks through had to be cleanly emptied in the original footage.
- **Challenge**: Redrawing with AI also changed the blackboard writing, which must not change, and the camera moves slightly.
- **What I did**
  - Built the empty classroom **only from real frames** where the student is absent, and moved it with the camera, keeping the blackboard pixel-identical.
  - Measured and reduced brightness flicker and jitter in the covered area (flicker 0.138 → 0.116, jitter under 0.1px).
  - Fixed a length mismatch from stitching split clips by compositing directly onto the single original file and comparing frame counts first.
- **Tech**: FFmpeg, ComfyUI, Python, OpenCV

</details>

### 📰 [news_Moa](https://github.com/naluteo89-sketch/news_Moa) · Naver News Tone Analysis `2026.10.26`
A web service that collects Naver News search results and shows each article's **positive/negative tone, key words and key sentences** at a glance.

**Stack**: Python · Flask · Naver News API · OpenAI (`gpt-6-luna`) · kiwipiepy · KNU Sentiment Lexicon · trafilatura

<details>
<summary><b>Details</b> · background, challenge, what I did, tech</summary>

- **Why**: Headlines that differ from the body, tone you can't see at a glance, floods of same-direction articles, and comments written from headlines alone. The goal is to let readers see **content and evidence before the headline**.
- **Thinking**: Calling the LLM per article means 10 calls and tens of thousands of tokens per page → the only place AI is really needed is the overall page mood.
- **How**
  - Send only titles + summaries in **one call per page**; the model returns only IDs and positive ratios; results are cached
  - Neutral thresholds drifted between models → **code decides the label** using a 35–65% band
  - Original articles showed blank in iframes → an inspection script **confirmed 7/20 were blocked**, so the server now extracts and expands article text directly
  - SSRF risk from fetching article URLs → allow public IPs only and re-check on every redirect

</details>

### 🥽 [Pano360](https://github.com/naluteo89-sketch/co_show_2026) · CO-SHOW 2026 360° XR Content `Phase 1 done · 2026.10.23`
A web studio + Unity viewer that turns a single photo into **360° images and 360° "event" videos for Meta Quest 3**.

**Stack**: Python · aiohttp · OpenAI · ComfyUI / Comfy Cloud · FLUX.2 Klein + 360 ERP LoRA · LTX-2.3 · FFmpeg · Unity 6 · Meta Quest 3

<details>
<summary><b>Details</b> · background, challenge, what I did, tech</summary>

- **Why**: Let exhibition visitors expand one photo into a 360° space and experience an "event" inside it in VR
- **Thinking**: Designed by splitting what people decide (placement, prompts, motion area) from what code handles (node injection, seam scoring, compositing)
- **How**
  - The LLM analyzes scene, lighting, FOV and horizon to produce prompts and placement → FLUX.2 outpainting → seam repair → **8192×4096** upscale
  - Feeding full 4K 360 into the video model made motion tiny and ran out of server memory → **generate only the painted region at high resolution**, then composite into 4K 360
  - A fixed timeline in the prompt makes the last frame match the first, so photo ↔ video loops seamlessly
  - **Regression tests that run without keys or GPUs** using a fake ComfyUI backend; seam scores quantify quality

</details>

### 🏠 [BuBot](https://github.com/naluteo89-sketch/BuBot) · Real-Estate Price RAG Chatbot `v2 · 2026.10.19`
A chatbot for asking about and comparing average apartment prices across 245 regions × 176 months in natural language. Every answer includes **calculation details and sources**.

**Stack**: Python · OpenAI · RAG · SQLite + numpy vector store · public data

<details>
<summary><b>Details</b> · background, challenge, what I did, tech</summary>

- **Why**: Remove the need to dig through complex price tables and calculate by hand
- **Thinking**: Inconsistent answers and made-up numbers came from letting the LLM do the math → restructured so the LLM never produces numbers
- **How**
  - Python does the calculations; the LLM only interprets and writes
  - Accuracy on a 30-question set went from **80% → 100%**; **191 automated tests** pass
  - Hallucination patterns found in a 48-question evaluation are handled by rules before the GPT call
  - Built the vector store and web server myself; budget and rate limits control cost

</details>

### 📸 [ImgPls](https://github.com/naluteo89-sketch/ImgPls) · AI Photo Compositing Studio `v2 · 2026.10.19`
A kiosk service for events: pick a portrait and a background theme, FLUX.2 blends them naturally, and a QR code sends the result to your phone.

**Stack**: Python · FastAPI · Jinja2 · ComfyUI / Comfy Cloud · FLUX.2 Klein · WebSocket · Playwright

<details>
<summary><b>Details</b> · background, challenge, what I did, tech</summary>

- **Why**: Let a single PC at an event take a visitor's photo, composite it immediately and hand it off to their phone
- **Thinking**: When the local GPU server went down, every request failed with 504 → needed a structure that doesn't depend on on-site hardware
- **How**
  - Heavy generation moved to **Comfy Cloud**; the FastAPI server only relays, stores and shares
  - Checked the Cloud `/api/object_info` response and replaced unsupported nodes with built-in ones
  - 10 API tests (extension/25 MB limits, blocking paths outside `results/`), plus a mock server to verify the pipeline

</details>

### 🐫 [Silkroad](https://github.com/naluteo89-sketch/Silkroad) · Silk Road Painting Workshop
A cultural XR experience where generative AI turns drawings from a Unity paint app into Silk Road–style paintings.

**Stack**: Unity 6 · C# · ComfyUI / Comfy Cloud · SDXL / FLUX.2 workflows · Android tablet

<details>
<summary><b>Details</b> · background, challenge, what I did, tech</summary>

- **Why**: Engage visitors with cultural content by turning their own drawings into Silk Road paintings
- **Thinking**: Without a server, the experience flow couldn't be tested at all → separated generation from the UI flow so each can be verified on its own
- **How**
  - Experience flow: draw → AI transform → before/after slider → save → QR share
  - A **dummy mode** for testing without a server, plus pipeline checks and style-preset quality comparison tools
  - Inspected and documented that built APKs still contain the API key, and outlined the move to server-side key management

</details>

---

## 📌 How I Work
- 🔢 **Verifiable AI**: Move what the AI would guess into code rules, and attach evidence to answers
- 🧪 **Decide by measurement**: Confirm results in numbers with tests and answer comparisons
- 📝 **Improve through records**: Log symptom, cause and fix for every issue and maintenance task

---

## 📫 Contact
- Email: naluteo89@gmail.com
