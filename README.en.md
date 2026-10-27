**English** | [한국어](README.md)

# Hi, I'm Daun Kim 👋

### AI Service Developer — I build fast and verify with numbers

I build quickly with AI, then **verify the results with code rules and tests**.  
I raised a RAG chatbot's accuracy from **80% → 100%** by using rules to stop the LLM from inventing numbers and dates,  
and I keep fixing issues after release, **logging every version**.

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

**Frontend**  
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS-1572B6?style=flat-square&logo=css3&logoColor=white)

**Backend**  
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)
![aiohttp](https://img.shields.io/badge/aiohttp-2C5BB4?style=flat-square&logo=aiohttp&logoColor=white)
![Spring](https://img.shields.io/badge/Spring-6DB33F?style=flat-square&logo=spring&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)

**Database**  
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=flat-square&logo=mariadb&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)

**AI · XR**  
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white)
![RAG](https://img.shields.io/badge/RAG-FF6F00?style=flat-square)
![ComfyUI](https://img.shields.io/badge/ComfyUI%20%2F%20Comfy%20Cloud-222222?style=flat-square)
![Unity](https://img.shields.io/badge/Unity-000000?style=flat-square&logo=unity&logoColor=white)
![Meta Quest](https://img.shields.io/badge/Meta%20Quest%203-0467DF?style=flat-square&logo=meta&logoColor=white)

**Tools**  
![VS Code](https://img.shields.io/badge/VS%20Code-007ACC?style=flat-square&logo=visualstudiocode&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)
![FFmpeg](https://img.shields.io/badge/FFmpeg-007808?style=flat-square&logo=ffmpeg&logoColor=white)

---

## 📂 Projects

### 📰 [news_Moa](https://github.com/naluteo89-sketch/news_Moa) · Naver News Tone Analysis `🆕 2026.10.26`
A web service that collects Naver News search results and shows each article's **positive/negative tone, key words and key sentences** at a glance.

**Stack**: Python · Flask · Naver News API · OpenAI (`gpt-6-luna`) · kiwipiepy · KNU Sentiment Lexicon · trafilatura

- **Why**: Headlines that differ from the body, tone you can't see at a glance, floods of same-direction articles, and comments written from headlines alone. The goal is to let readers see **content and evidence before the headline**.
- **Thinking**: Calling the LLM per article means 10 calls and tens of thousands of tokens per page → the only place AI is really needed is the overall page mood.
- **How**
  - Send only titles + summaries in **one call per page**; the model returns only IDs and positive ratios; results are cached
  - Neutral thresholds drifted between models → **code decides the label** using a 35–65% band
  - Original articles showed blank in iframes → an inspection script **confirmed 7/20 were blocked**, so the server now extracts and expands article text directly
  - SSRF risk from fetching article URLs → allow public IPs only and re-check on every redirect

### 🥽 [Pano360 Studio](https://github.com/naluteo89-sketch/co_show_2026) · CO-SHOW 2026 360° XR Content `🆕 Phase 1 done · 2026.10.23`
A web studio + Unity viewer that turns a single photo into **360° images and 360° "event" videos for Meta Quest 3**.

**Stack**: Python · aiohttp · OpenAI · ComfyUI / Comfy Cloud · FLUX.2 Klein + 360 ERP LoRA · LTX-2.3 · FFmpeg · Unity 6 · Meta Quest 3

- **Why**: Let exhibition visitors expand one photo into a 360° space and experience an "event" inside it in VR
- **Thinking**: Designed by splitting what people decide (placement, prompts, motion area) from what code handles (node injection, seam scoring, compositing)
- **How**
  - The LLM analyzes scene, lighting, FOV and horizon to produce prompts and placement → FLUX.2 outpainting → seam repair → **8192×4096** upscale
  - Feeding full 4K 360 into the video model made motion tiny and ran out of server memory → **generate only the painted region at high resolution**, then composite into 4K 360
  - A fixed timeline in the prompt makes the last frame match the first, so photo ↔ video loops seamlessly
  - **Regression tests that run without keys or GPUs** using a fake ComfyUI backend; seam scores quantify quality

### 🏠 [BuBot](https://github.com/naluteo89-sketch/BuBot) · Real-Estate Price RAG Chatbot `v2 · 2026.10.19`
A chatbot for asking about and comparing average apartment prices across 245 regions × 176 months in natural language. Every answer includes **calculation details and sources**.

**Stack**: Python · OpenAI · RAG · SQLite + numpy vector store · public data

- **Why**: Remove the need to dig through complex price tables and calculate by hand
- **Thinking**: Inconsistent answers and made-up numbers came from letting the LLM do the math → restructured so the LLM never produces numbers
- **How**
  - Python does the calculations; the LLM only interprets and writes
  - Accuracy on a 30-question set went from **80% → 100%**; **191 automated tests** pass
  - Hallucination patterns found in a 48-question evaluation are handled by rules before the GPT call
  - Built the vector store and web server myself; budget and rate limits control cost

### 📸 [ImgPls](https://github.com/naluteo89-sketch/ImgPls) · AI Photo Compositing Studio `v2 · 2026.10.19`
A kiosk service for events: pick a portrait and a background theme, FLUX.2 blends them naturally, and a QR code sends the result to your phone.

**Stack**: Python · FastAPI · Jinja2 · ComfyUI / Comfy Cloud · FLUX.2 Klein · WebSocket · Playwright

- **Why**: Let a single PC at an event take a visitor's photo, composite it immediately and hand it off to their phone
- **Thinking**: When the local GPU server went down, every request failed with 504 → needed a structure that doesn't depend on on-site hardware
- **How**
  - Heavy generation moved to **Comfy Cloud**; the FastAPI server only relays, stores and shares
  - Checked the Cloud `/api/object_info` response and replaced unsupported nodes with built-in ones
  - 10 API tests (extension/25 MB limits, blocking paths outside `results/`), plus a mock server to verify the pipeline

### 🐫 [Silkroad](https://github.com/naluteo89-sketch/silkroad) · Silk Road Painting Workshop
A cultural XR experience where generative AI turns drawings from a Unity paint app into Silk Road–style paintings.

**Stack**: Unity 6 · C# · ComfyUI / Comfy Cloud · SDXL / FLUX.2 workflows · Android tablet

- **Why**: Engage visitors with cultural content by turning their own drawings into Silk Road paintings
- **Thinking**: Without a server, the experience flow couldn't be tested at all → separated generation from the UI flow so each can be verified on its own
- **How**
  - Experience flow: draw → AI transform → before/after slider → save → QR share
  - A **dummy mode** for testing without a server, plus pipeline checks and style-preset quality comparison tools
  - Inspected and documented that built APKs still contain the API key, and outlined the move to server-side key management

---

## 📌 How I Work
- 🔢 **Verifiable AI**: Move what the AI would guess into code rules, and attach evidence to answers
- 🧪 **Decide by measurement**: Confirm results in numbers with tests and answer comparisons
- 📝 **Improve through records**: Log symptom, cause and fix for every issue and maintenance task

---

## 📫 Contact
- Email: naluteo89@gmail.com
