[English](README.en.md) | **한국어**

# 안녕하세요, AI 서비스 개발자 김다운입니다 👋

> **"AI가 틀릴 수 있는 부분은 코드로 막고, 결과는 숫자로 확인합니다."**

생성형 AI를 활용해 서비스를 빠르게 만들되, AI가 임의로 숫자를 지어내거나 답이 흔들리는 문제는 규칙과 테스트로 해결해 왔습니다.  
부동산 시세 챗봇에서는 이 방식으로 **답변 정확도를 80%에서 100%로** 높였습니다.  
서비스를 공개한 뒤에도 문제를 찾아 개선하고, 그 과정을 버전별로 기록하고 있습니다.

### 📂 [Notion 포트폴리오](https://kimdaun98y.notion.site/3cd651db82fb801392cff0e96b79994c) — 프로젝트별 상세 기록과 학습 일지(TIL)

---

## 📂 프로젝트 한눈에 보기

| 프로젝트 | 무엇을 만들었나 | 핵심 성과 |
|---|---|---|
| 🛍️  [🔗 하우머치](https://youhowmuch.beefalo-tiaki.ts.net/) | 유튜브 리뷰 영상 속 상품을 모아 보여 주는 쇼핑몰 (웹 + 앱) | 영상 2,488개에서 상품 13,709개 자동 수집, 목록 10.7MB → 116KB |
| 🎬 [5·18 인서트컷](https://kimdaun98y.notion.site/415651db82fb81e0a09ac7adc62003b8) `회사 업무`  | 4K 영상에서 학생만 지운 빈 교실 영상 | 8,362프레임 일치, 깜빡임 0.138 → 0.116, 칠판 글씨 원본 유지 |
| 🧴 [뷰티 AI 플랫폼](https://kimdaun98y.notion.site/40d651db82fb814484c2d8554f49d0e4) `회사 업무` | 피부 분석·화장품 라벨 인식 AI API 2종 | 잡티 판정 일치도 0.55 → 0.78, 비용 1/20 |
| 🏠 [BuBot](https://github.com/naluteo89-sketch/BuBot) ⭐ | 근거와 출처를 보여 주는 아파트 매매가 챗봇 | 정확도 80% → 100%, 자동 테스트 191개 |
| 📰 [news_Moa](https://github.com/naluteo89-sketch/news_Moa) | 네이버 뉴스 감성·키워드 분석 서비스 | 페이지당 AI 호출 1번, 본문 추출 7/7 |
| 🥽 [Pano360](https://github.com/naluteo89-sketch/co_show_2026) | 사진 한 장으로 만드는 Quest 3용 8K 360° 이미지 | 8192×4096, 이음새 색 차이 4.5배 → 1.23배 |
| 🐫 [Silkroad](https://github.com/naluteo89-sketch/Silkroad) | 직접 그린 그림을 실크로드 회화풍으로 바꾸는 XR 체험 | 6단계 체험 흐름, 서버 없이 검증하는 더미 모드 |
| 📸 [ImgPls](https://github.com/naluteo89-sketch/ImgPls) | 인물 사진을 새 배경에 합성해 QR로 전달하는 키오스크 | 클라우드 전환, API 테스트 10종 |
| 🕷️ [스마트 크롤러](https://github.com/naluteo89-sketch/smart-crawler-extension) | 클릭 한 번으로 웹 데이터를 모으는 Chrome 확장 + 크롤러 | 수천 건이어도 AI 호출 1~2회 |

---

## 💪 강점

| 강점 | 내용 |
|---|---|
| **이전 경험을 통한 빠른 설계** | 비슷한 프로젝트는 이전 경험을 살린 안정적이고 빠른 설계로 하루 만에 제작합니다. BuBot에서 검증한 ‘코드가 계산, LLM은 해석’ 구조를 뷰티 AI 점수 서버에 재사용했습니다 |
| **새로운 기술 적용** | 처음 다루는 모델·플랫폼도 직접 비교·측정해 실제 결과물까지 연결합니다. FLUX.2로 Quest 3용 8K 360° 이미지, 4K 배경판 합성 8,362프레임, 웹 + Android 앱을 만들었습니다 |
| **유지보수** | 테스트를 먼저 갖춰 두고 고쳐, 기존 기능을 깨지 않고 구조와 성능을 바꿉니다. BuBot 테스트 191개, ImgPls 클라우드 전환·API 테스트 10종, 목록 10.7MB → 116KB |

---

## 💡 문제 해결 과정

프로젝트마다 아래 순서로 문제에 접근합니다.

1. **불편함 정의** — 실제 사용자가 겪는 문제를 글로 정리하고, 기존 서비스가 해결하지 못하는 이유를 비교합니다.
2. **AI와 코드의 역할 분담** — 틀리면 안 되는 부분은 코드로, 사람처럼 해석해야 하는 부분만 AI에 맡깁니다.
3. **측정 후 설계 변경** — 추측으로 정하지 않고, 점검 스크립트와 평가 문항으로 먼저 확인한 뒤 방향을 정합니다.
4. **구조로 한계 극복** — 장비 성능이나 비용의 한계를 만나면 처리 방식 자체를 바꿉니다.
5. **기록과 재검증** — 문제의 증상·원인·조치를 기록하고, 테스트로 같은 문제가 반복되지 않게 합니다.

---

## 🔎 프로젝트 상세

각 프로젝트의 **자세히 보기**를 누르면 기획 배경과 해결 과정이 펼쳐집니다.

### 🛍️ [you_HOWMUCH](https://github.com/naluteo89-sketch/I_sell_a_store_demo) — 유튜브 리뷰 영상 쇼핑몰 `2026.11 · 진행 중` · [🔗 데모](https://youhowmuch.beefalo-tiaki.ts.net/)

> 유튜브 리뷰 영상에 나온 상품을 자동으로 모아, **영상과 상품을 한 화면에서 보고 바로 담는** 쇼핑몰 (웹 + 안드로이드 앱)

<details>
<summary><b>자세히 보기</b> · 기획 배경, 고민한 점, 해결 과정, 사용 기술</summary>

- **기획 배경**  
  물건을 사기 전에 리뷰 영상부터 찾아보지만, 쇼핑몰 상세 페이지와 리뷰 영상은 서로 다른 곳에 흩어져 있습니다. "이 영상에 나온 그 상품, 얼마야?"라는 질문에서 출발했습니다.
- **고민한 점**  
  유튜브 API는 하루 사용량이 정해져 있어 방문자가 올 때마다 호출할 수 없습니다. 또 언어만 영어로 바꾸면 영미권 사용자에게 한국 유튜버와 한국 상품이 그대로 보여 의미가 없었습니다.
- **해결 과정**
  - 영상 설명란에서 상품을 찾아 등록하는 자동 수집을 만들어 **영상 2,488개에서 상품 13,709개**를 모았고, 방문자는 저장된 데이터만 읽도록 했습니다.
  - 언어를 번역이 아닌 **시장 전환**으로 설계해, 영어 화면에는 영미권 영상에서 수집한 상품만 달러 가격으로 보여 줍니다.
  - 전체 상품을 한 번에 내려받던 목록을 서버에서 40개씩 나눠 보내도록 바꿔 **페이지 크기를 10.7MB에서 116KB로** 줄였습니다.
  - 로그인은 서버 세션과 CSRF 검사를 적용하고, 실패 문구로 가입 여부가 드러나지 않게 했습니다.
- **사용 기술**: Next.js 15, Spring Boot 3.5(Java 21), MySQL 8, YouTube Data API, Android(Kotlin, Jetpack Compose)  
- **상세 기록**: [Notion 프로젝트 페이지](https://kimdaun98y.notion.site/415651db82fb8199af20cb5a4e5b2c1e)

</details>

### 🕷️ 스마트 크롤러 — 클릭 한 번으로 웹 데이터 수집 `2026.11`

> 브라우저에서 항목 하나를 클릭하면 **비슷한 항목 전체를 찾아 정리된 데이터로 내려받는** Chrome 확장 프로그램과 Python 크롤러

<details>
<summary><b>자세히 보기</b> · 기획 배경, 고민한 점, 해결 과정, 사용 기술</summary>

- **기획 배경**  
  채용 공고나 상품 목록을 반복해서 모을 때마다 수집 규칙(CSS 셀렉터)을 직접 짜야 하는 불편이 있었습니다.
- **고민한 점**  
  항목을 찾는 일까지 AI에 맡기면 느리고 비용이 듭니다. AI가 꼭 필요한 곳은 "값에 어떤 이름을 붙일지" 정하는 일뿐이라고 판단했습니다.
- **해결 과정**
  - 클릭한 요소에서 위로 올라가며 같은 모양이 가장 많이 반복되는 단위를 찾는 **규칙 기반 방식**으로, AI 없이도 바로 동작하게 했습니다.
  - AI에는 샘플 6개만 보내 정리 계획만 받고 전체 데이터에는 브라우저가 적용해, **수천 건이어도 AI 호출은 1~2회**입니다.
  - 화면이 늦게 그려지는 사이트와 무한 스크롤을 처리하고, robots.txt 준수와 요청 간격 제한을 기본으로 적용했습니다.
- **사용 기술**: Python, Playwright, pandas, Chrome Extension(Manifest V3), JavaScript, OpenAI

</details>

### 🧴 [뷰티 AI 플랫폼 — AI 분석 파트](https://kimdaun98y.notion.site/40d651db82fb814484c2d8554f49d0e4) `2026.10 ~ 11 · 회사 업무`

> 셀피로 **피부 상태를 점수화**하고 화장품 라벨 사진에서 **전성분을 읽어 내는** AI 분석 API 2종 (기관·업체명 비공개, 코드는 비공개 저장소)

<details>
<summary><b>자세히 보기</b> · 기획 배경, 고민한 점, 해결 과정, 사용 기술</summary>

- **기획 배경**  
  "AI로 얼굴과 라벨을 분석해 결과를 내라"는 목표만 있고, 무엇을 몇 점으로 볼지 판정 기준이 없었습니다.
- **고민한 점**  
  AI에 점수를 직접 맡기면 같은 사진도 호출할 때마다 점수가 달라지고, 왜 그 점수인지 설명할 수 없었습니다.
- **해결 과정**
  - AI는 부위별로 보이는 것만 답하고, **점수와 판정은 서버가 정해진 규칙으로 계산**하게 했습니다.
  - 공공 데이터(AI Hub) 107명의 전문가 판정과 비교해 잡티 판정 일치도(순위 상관)를 **0.55에서 0.78로** 높였습니다.
  - 같은 검증 데이터로 모델을 비교해 **분석 비용을 1/20로** 줄였고, 라벨 성분은 공공 데이터 샘플 **29개 중 29개**를 읽었습니다.
- **종료 후 유지보수 (11/19 ~ 11/23)**
  - 라벨 OCR 보조 엔진을 EasyOCR에서 PaddleOCR로 바꿔 사전에 맞는 성분을 **8개에서 364개로** 늘리고, 장당 17.1초를 3.7초로 줄였습니다.
  - API에 동시 처리 상한과 즉시 503(`Retry-After`) 응답을 넣어 동시 40건 응답 중앙값을 29.6초에서 14.2초로 줄였고, 연구용 웹의 일괄 분석은 **4.45~5.76배** 빨라졌습니다.
  - 사내 로컬 LLM(vLLM)을 연결하고 기존 모델과 얼굴·라벨 각 100장을 교차 검증했습니다. 정답 대비 정확도는 **동등**하고 비용은 0원, 속도는 약 5배 느려 점수 기준표와 지시문을 보정한 뒤 교체할 계획입니다.
- **사용 기술**: Python, Flask, OpenAI(이미지 입력), OpenCV, MediaPipe, PaddleOCR, vLLM(로컬 LLM), AI Hub 공공 데이터

</details>

### 🎬 [5·18 인서트컷 — 4K 영상 편집](https://kimdaun98y.notion.site/415651db82fb81e0a09ac7adc62003b8) `2026.10 ~ · 회사 업무`

> 교실 장면의 학생이 AR 캐릭터로 바뀌는 장면을 위해, **4K 원본에서 학생만 지운 빈 교실 영상**을 만드는 작업 (발주처·원본 비공개)

<details>
<summary><b>자세히 보기</b> · 기획 배경, 고민한 점, 해결 과정, 사용 기술</summary>

- **기획 배경**  
  캐릭터를 3D로 새로 넣으려면, 원본 영상에서 학생이 지나가는 자리를 자연스럽게 비워야 했습니다.
- **고민한 점**  
  AI로 화면을 다시 그리면 바뀌면 안 되는 칠판 글씨까지 바뀌었고, 카메라도 조금씩 움직였습니다.
- **해결 과정**
  - 학생이 없는 순간의 **실제 화면만 조합해 빈 교실 배경을 만들고**, 카메라 움직임에 맞춰 덮어 칠판 글씨를 원본 그대로 지켰습니다.
  - 덮은 영역의 밝기 깜빡임과 흔들림을 수치로 측정하며 개선했습니다(깜빡임 0.138 → 0.116, 흔들림 0.1픽셀 이하).
  - 영상을 조각으로 나눠 합칠 때 길이가 어긋나는 문제를, 원본 한 파일에 직접 합성하고 합성 전에 길이를 비교하는 방식으로 막았습니다.
- **사용 기술**: FFmpeg, ComfyUI, Python, OpenCV

</details>

### 📰 [news_Moa](https://github.com/naluteo89-sketch/news_Moa) — 네이버 뉴스 감성·키워드 분석 서비스 `2026.10`

> 뉴스 검색 결과를 모아 기사별 **긍정·부정 분위기, 핵심 키워드, 핵심 문장**을 한눈에 보여 주는 웹 서비스

<details>
<summary><b>자세히 보기</b> · 기획 배경, 고민한 점, 해결 과정, 사용 기술</summary>

- **기획 배경**  
  제목과 본문 내용이 다른 기사, 한눈에 알기 어려운 논조, 같은 방향의 기사가 한꺼번에 쏟아지는 현상, 제목만 보고 다는 댓글 등의 문제에서 출발했습니다. 기존 분석 서비스는 검색량 위주라 "기사에 실제로 어떤 내용이 담겼는지" 알기 어려웠습니다.
- **고민한 점**  
  기사마다 AI를 호출하면 한 페이지(10건)에 10번 호출해야 해 비용이 크게 늘어납니다. AI가 꼭 필요한 곳은 "페이지 전체의 분위기 판단"뿐이라고 판단했습니다.
- **해결 과정**
  - 기사 제목과 요약만 묶어 **페이지당 AI 호출을 1회로 줄이고**, 이미 분석한 기사는 저장해 다시 호출하지 않도록 했습니다.
  - AI 모델마다 '중립' 기준이 달라지는 문제가 있어, AI는 긍정 비율(%)만 답하고 **긍정·부정·중립 분류는 코드가 정해진 기준으로 결정**하도록 했습니다.
  - 원본 기사를 화면에 띄우는 방식이 빈 화면으로 나오는 문제를 점검 스크립트로 조사해, 20건 중 7건이 외부 표시를 막고 있음을 확인했습니다. 이후 서버가 본문을 직접 가져와 보여 주는 방식으로 바꿨습니다.
  - 외부 주소를 요청할 때 내부망에 접근될 수 있는 보안 위험(SSRF)을 막기 위해 공인 IP만 허용했습니다.
- **사용 기술**: Python, Flask, 네이버 뉴스 검색 API, OpenAI, 한국어 형태소 분석(kiwipiepy), KNU 한국어 감성사전

</details>

### 🥽 [Pano360](https://github.com/naluteo89-sketch/co_show_2026) — CO-SHOW 2026 전시용 360° VR 콘텐츠 제작 도구 `2026.10 · 1차 완료`

> 사진 한 장으로 **VR 기기(Meta Quest 3)에서 볼 수 있는 360° 이미지와 영상**을 만드는 웹 제작 도구와 VR 뷰어

<details>
<summary><b>자세히 보기</b> · 기획 배경, 고민한 점, 해결 과정, 사용 기술</summary>

- **기획 배경**  
  전시장 방문객이 고른 사진 한 장을 360° 공간으로 넓히고, 그 안에서 일어나는 장면을 VR로 체험할 수 있게 하는 것이 목표였습니다.
- **고민한 점**  
  사람이 판단해야 할 부분(배치, 장면 설명, 움직일 영역 선택)과 프로그램이 자동으로 처리할 부분(이미지 생성 설정, 품질 점검, 영상 합성)을 먼저 표로 나눠 설계했습니다.
- **해결 과정**
  - AI가 사진의 장면·조명·화각을 분석해 생성 설정값을 만들고, 이미지 생성 AI로 360° 이미지를 완성한 뒤 **8K(8192×4096) 해상도**로 높였습니다.
  - 360° 영상 전체를 한 번에 만들면 움직임이 작게 나오고 서버 메모리가 부족했습니다. 그래서 **사용자가 지정한 영역만 고화질로 생성한 뒤 전체 영상에 합성**하는 방식으로 바꿔 해결했습니다.
  - 실제 AI 서버나 GPU 없이도 돌아가는 테스트 환경을 만들고, 이미지 이음새 품질을 점수로 측정했습니다.
- **사용 기술**: Python, aiohttp, OpenAI, ComfyUI / Comfy Cloud, FLUX.2, LTX-2.3, FFmpeg, Unity 6, Meta Quest 3

</details>

### 🏠 [BuBot](https://github.com/naluteo89-sketch/BuBot) — 아파트 매매가 조회 AI 챗봇 `2026.10 · v2`

> 전국 245개 지역, 176개월치 아파트 평균 매매가를 **대화로 묻고 비교**할 수 있고, 모든 답변에 **계산 근거와 출처**를 함께 보여 주는 챗봇

<details>
<summary><b>자세히 보기</b> · 기획 배경, 고민한 점, 해결 과정, 사용 기술</summary>

- **기획 배경**  
  복잡한 부동산 가격 통계표를 직접 찾아 계산해야 하는 번거로움을 줄이고자 했습니다.
- **고민한 점**  
  같은 질문에도 답이 달라지고 AI가 없는 숫자를 지어내는 문제가 있었습니다. 원인을 분석해 보니 **계산까지 AI에 맡긴 구조**가 문제였습니다.
- **해결 과정**
  - 가격 계산은 모두 Python 코드가 하고, AI는 결과를 설명하는 문장만 작성하도록 구조를 바꿨습니다.
  - 30개 평가 문항으로 정확도를 측정해 **80% → 100%** 로 개선했고, 자동 테스트 **191개**를 모두 통과했습니다.
  - 48개 문항 평가에서 발견한 오답 유형은 AI에 질문하기 전에 규칙으로 먼저 처리하도록 했습니다.
  - 검색용 데이터 저장소와 웹 서버를 직접 구현하고, 사용 예산과 호출 횟수 제한으로 비용을 관리했습니다.
- **사용 기술**: Python, OpenAI, RAG(검색 기반 AI 답변), SQLite, numpy, 공공데이터

</details>

### 📸 [ImgPls](https://github.com/naluteo89-sketch/ImgPls) — AI 사진 합성 키오스크 `2026.10 · v2`

> 인물 사진과 배경을 고르면 AI가 자연스럽게 합성하고, **QR 코드로 휴대폰에 바로 전달**하는 행사장용 서비스

<details>
<summary><b>자세히 보기</b> · 기획 배경, 고민한 점, 해결 과정, 사용 기술</summary>

- **기획 배경**  
  행사장 PC 한 대만으로 방문객 사진을 찍어 즉석에서 합성하고, 결과물을 휴대폰으로 받아 갈 수 있게 하고자 했습니다.
- **고민한 점**  
  처음에는 현장 GPU 서버를 사용했는데, 서버가 꺼지면 모든 요청이 실패했습니다. 현장 장비 상태와 관계없이 동작하는 구조가 필요했습니다.
- **해결 과정**
  - 무거운 이미지 생성은 **클라우드 서비스(Comfy Cloud)로 옮기고**, 웹 서버는 요청 전달·저장·공유만 담당하게 했습니다.
  - 클라우드에서 지원하지 않는 기능을 직접 확인해 대체 기능으로 교체했습니다.
  - 파일 형식·용량 제한, 허용되지 않은 경로 접근 차단 등 **API 테스트 10종**을 만들고, 가상 서버로 전체 흐름을 검증했습니다.
- **사용 기술**: Python, FastAPI, Jinja2, ComfyUI / Comfy Cloud, FLUX.2, WebSocket, Playwright

</details>

### 🐫 [Silkroad](https://github.com/naluteo89-sketch/Silkroad) — 실크로드 그림 공방 (문화 XR 체험 콘텐츠) `2026.10`

> 태블릿 그림판에 그린 그림을 생성형 AI가 **실크로드 회화풍 작품으로 바꿔 주는** 체험 콘텐츠

<details>
<summary><b>자세히 보기</b> · 기획 배경, 고민한 점, 해결 과정, 사용 기술</summary>

- **기획 배경**  
  관람객이 직접 그린 그림이 실크로드 회화로 바뀌는 경험을 통해 문화 콘텐츠에 자연스럽게 참여하도록 하고자 했습니다.
- **고민한 점**  
  AI 서버가 없으면 체험 흐름 전체를 확인할 수 없었습니다. 그래서 이미지 생성과 화면 흐름을 분리해 각각 검증할 수 있게 했습니다.
- **해결 과정**
  - 그리기 → AI 변환 → 원본과 비교 → 저장 → QR 공유로 이어지는 체험 흐름을 구현했습니다.
  - 서버 없이도 테스트할 수 있는 **더미 모드**와 화풍 품질 비교 도구를 만들었습니다.
  - 배포용 앱에 인증 키가 남는 보안 문제를 직접 점검해 문서로 정리하고, 개선 방향(서버에서 키 관리)을 제시했습니다.
- **사용 기술**: Unity 6, C#, ComfyUI / Comfy Cloud, SDXL, FLUX.2, Android 태블릿

</details>

---

## 🛠 기술 스택

**언어**  
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Java](https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black)
![C#](https://img.shields.io/badge/C%23-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat-square&logo=kotlin&logoColor=white)

**프론트엔드 · 모바일**  
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![Android](https://img.shields.io/badge/Android%20(Compose)-3DDC84?style=flat-square&logo=android&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS-1572B6?style=flat-square&logo=css3&logoColor=white)

**백엔드**  
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)
![aiohttp](https://img.shields.io/badge/aiohttp-2C5BB4?style=flat-square&logo=aiohttp&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)

**데이터베이스**  
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

**도구**  
![VS Code](https://img.shields.io/badge/VS%20Code-007ACC?style=flat-square&logo=visualstudiocode&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)
![FFmpeg](https://img.shields.io/badge/FFmpeg-007808?style=flat-square&logo=ffmpeg&logoColor=white)

---

## 📫 연락처
- 이메일: naluteo89@gmail.com
- 포트폴리오: [Notion 포트폴리오](https://kimdaun98y.notion.site/3cd651db82fb801392cff0e96b79994c)
