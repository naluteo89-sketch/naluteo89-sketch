[English](README.en.md) | **한국어**

# 안녕하세요, 김다운입니다 👋

### AI 서비스 개발자 — 빠르게 만들고, 숫자로 검증합니다

AI와 함께 빠르게 만들되, 결과는 **코드 규칙과 테스트로 검증**합니다.  
LLM이 숫자·기간을 지어내는 문제를 규칙으로 막아 RAG 챗봇 정확도를 **80% → 100%** 로 끌어올렸고,  
출시 후에도 문제를 찾아 고친 과정을 **버전별로 기록**합니다.

---

## 🧠 문제를 푸는 방식

| 단계 | 하는 일 | 예시 |
|---|---|---|
| 1. 불편함에서 출발 | 실제로 겪는 문제를 문장으로 정리하고, 기존 서비스가 왜 부족한지 비교 | news_Moa: 기존 분석 서비스는 검색량 숫자 위주라 "기사가 무슨 이야기를 하는지"는 알 수 없음 |
| 2. AI가 할 일과 코드가 할 일 나누기 | 틀리면 안 되는 계산·판정은 코드로, 해석·문장은 LLM으로 | BuBot: 가격 계산은 Python, LLM은 설명만 / news_Moa: 모델은 비율만, 라벨은 코드가 결정 |
| 3. 먼저 측정하고 설계 바꾸기 | 가정 대신 점검 스크립트와 평가셋으로 확인 | news_Moa: iframe 차단 7/20 확인 → 본문 직접 추출로 전환 |
| 4. 병목은 구조로 해결 | 장비·비용 한계를 만나면 처리 위치나 범위를 바꿈 | Pano360: 4K 전체 대신 움직이는 범위만 생성 / ImgPls: 로컬 GPU → Comfy Cloud |
| 5. 기록하고 다시 검증 | 증상·원인·조치를 남기고, 테스트로 회귀를 막음 | BuBot 테스트 191개, Pano360 가짜 백엔드 회귀 테스트 |

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

### 📰 [news_Moa](https://github.com/naluteo89-sketch/news_Moa) · 네이버 뉴스 분위기 분석 `🆕 2026.10.26`
네이버 뉴스 검색 결과를 모아 기사마다 **긍정·부정 분위기와 핵심 키워드·핵심 문장**을 바로 보여 주는 웹 서비스입니다.

**기술**: Python · Flask · Naver News API · OpenAI(`gpt-6-luna`) · kiwipiepy · KNU 감성사전 · trafilatura

- **기획**: 제목과 다른 본문, 한눈에 안 보이는 논조, 같은 방향으로 쏟아지는 기사, 제목만 보고 다는 댓글. 독자가 **제목이 아니라 내용과 근거를 먼저** 보게 하자는 생각에서 시작
- **생각 과정**: 기사마다 LLM을 부르면 10건에 10번 호출·수만 토큰 → 정말 AI가 필요한 곳은 "페이지 전체 분위기"뿐이라고 판단
- **해결 방식**
  - 제목+요약만 묶어 **페이지당 1회 호출**, 출력은 번호·긍정 비율만, 판정 결과는 캐시
  - 모델마다 중립 기준이 흔들림 → 라벨은 **코드가 35~65% 기준으로 결정**
  - 원본 기사 iframe이 빈 화면 → 점검 스크립트로 **차단 7/20 확인** 후 본문을 직접 추출해 펼치는 방식으로 전환
  - 기사 주소로 내부망 접근 위험(SSRF) → 공인 IP만 허용, 리다이렉트마다 재검사

### 🥽 [Pano360 Studio](https://github.com/naluteo89-sketch/co_show_2026) · CO-SHOW 2026 360° XR 콘텐츠 `🆕 1차 완료 · 2026.10.23`
사진 한 장으로 **Meta Quest 3용 360° 이미지와 "사건" 360 영상**을 만드는 웹 스튜디오 + Unity 뷰어입니다.

**기술**: Python · aiohttp · OpenAI · ComfyUI / Comfy Cloud · FLUX.2 Klein + 360 ERP LoRA · LTX-2.3 · FFmpeg · Unity 6 · Meta Quest 3

- **기획**: 전시장에서 방문객이 고른 사진 한 장을 360° 공간으로 넓히고, 그 안에서 일어나는 "사건"을 VR로 체험하게 하기
- **생각 과정**: 사람이 판단할 것(배치·프롬프트·움직일 범위)과 코드가 처리할 것(노드 값 주입·이음새 점수·합성)을 표로 나눠 설계
- **해결 방식**
  - LLM이 장면·조명·화각·수평선을 분석해 프롬프트와 배치값 생성 → FLUX.2로 아웃페인트 → 좌우 이음새 복원 → **8192×4096** 업스케일
  - 4K 360 전체를 영상 모델에 넣으면 움직임이 작고 서버 메모리 부족 → **칠한 범위만 잘라 고해상도 생성** 후 4K 360에 합성
  - 마지막 프레임이 첫 화면과 같도록 프롬프트에 시간표를 고정해 사진 ↔ 영상이 자연스럽게 이어지게 함
  - 가짜 ComfyUI 백엔드로 **키·GPU 없이 도는 회귀 테스트**, 이음새 점수로 품질 수치화

### 🏠 [BuBot](https://github.com/naluteo89-sketch/BuBot) · 부동산 매매가 RAG 챗봇 `v2 · 2026.10.19`
전국 245개 지역 × 176개월의 아파트 평균 매매가를 자연어로 묻고 비교할 수 있는 챗봇입니다. 모든 답변에 **계산 근거와 출처**를 함께 보여 줍니다.

**기술**: Python · OpenAI · RAG · SQLite + numpy 벡터 저장소 · 공공데이터

- **기획**: 복잡한 가격 통계표를 직접 찾아 계산해야 하는 과정을 줄이기
- **생각 과정**: 같은 질문에 답이 달라지고 숫자를 지어내는 원인은 "LLM에게 계산을 맡긴 것" → 숫자는 절대 LLM이 만들지 않게 구조를 바꿈
- **해결 방식**
  - 숫자는 Python이 계산하고, LLM은 해석과 문장 작성만 담당
  - 30문항 평가셋으로 정확도 **80% → 100%**, 자동 테스트 **191개** 통과
  - 48문항 평가에서 찾은 환각 유형을 GPT 호출 전 규칙으로 처리
  - 벡터 저장소·웹 서버 직접 구현, 예산·호출 제한으로 비용 관리

### 📸 [ImgPls](https://github.com/naluteo89-sketch/ImgPls) · AI 이미지 합성 스튜디오 `v2 · 2026.10.19`
인물 사진과 배경 테마를 고르면 FLUX.2로 자연스럽게 합성하고, QR 코드로 휴대폰에 바로 전달하는 행사장용 키오스크 서비스입니다.

**기술**: Python · FastAPI · Jinja2 · ComfyUI / Comfy Cloud · FLUX.2 Klein · WebSocket · Playwright

- **기획**: 행사장 PC 한 대로 방문객 사진을 찍어 바로 합성하고, 휴대폰으로 받아 가게 하기
- **생각 과정**: 로컬 GPU 서버가 꺼지면 모든 요청이 504로 실패 → 현장 장비에 의존하지 않는 구조가 필요
- **해결 방식**
  - 무거운 생성은 **Comfy Cloud**로, FastAPI 서버는 중계·저장·공유만 담당
  - Cloud 미지원 노드를 `/api/object_info` 응답으로 확인해 기본 노드로 교체
  - 업로드 확장자·25MB 제한, `results/` 밖 경로 차단 등 API 테스트 10종, 모의 서버로 파이프라인 검증

### 🐫 [Silkroad](https://github.com/naluteo89-sketch/silkroad) · 실크로드 그림 공방
Unity 그림판에 그린 그림을 생성형 AI가 실크로드 회화풍 이미지로 바꿔 주는 문화 XR 체험 콘텐츠입니다.

**기술**: Unity 6 · C# · ComfyUI / Comfy Cloud · SDXL / FLUX.2 워크플로 · Android 태블릿

- **기획**: 관람객이 직접 그린 그림이 실크로드 회화가 되는 경험으로 문화 콘텐츠에 참여하게 하기
- **생각 과정**: 서버가 없으면 체험 흐름 자체를 확인할 수 없음 → 생성과 화면 흐름을 분리해 따로 검증
- **해결 방식**
  - 그리기 → AI 변환 → 원본 비교 슬라이더 → 저장 → QR 공유의 체험 흐름
  - 서버 없이 테스트하는 **더미 모드**, 파이프라인 점검·스타일 프리셋 품질 비교 도구
  - 빌드된 APK에 API 키가 남는 문제를 직접 점검해 문서화하고, 서버 측 키 관리로의 전환 필요성 정리

---

## 📌 How I Work
- 🔢 **검증 가능한 AI**: AI가 추측하던 부분을 코드 규칙으로 옮기고, 답변에 근거를 붙입니다
- 🧪 **측정으로 판단**: 테스트와 정답 비교로 결과를 숫자로 확인합니다
- 📝 **기록으로 개선**: 이슈와 유지보수마다 증상·원인·조치를 남깁니다

---

## 📫 Contact
- Email: naluteo89@gmail.com
# 안녕하세요, 김다운입니다 👋

### "AI서비스 개발자

AI와 함께 빠르게 만들고, **코드 규칙과 테스트로 결과를 검증**합니다.  
LLM이 숫자·기간을 지어내는 문제를 규칙으로 막아 RAG 챗봇 정확도를 **80% → 100%** 로 끌어올렸고,  
출시 후에도 문제를 찾아 고치며 **버전별로 기록**합니다.

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

**Tools**  
![VS Code](https://img.shields.io/badge/VS%20Code-007ACC?style=flat-square&logo=visualstudiocode&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)

---

## 📂 Projects

### 🏠 [BuBot](https://github.com/naluteo89-sketch/BuBot) · 부동산 매매가 RAG 챗봇 `🆕 v2 · 2026.10.19`
자연어 질문으로 전국 245개 지역 × 176개월 아파트 평균 매매가를 조회·비교하고, **계산 근거와 출처**를 함께 보여주는 챗봇
- 숫자는 Python이 계산, LLM은 해석·문장만 담당하도록 역할 분리
- 30문항 정확도 **80% → 100%**, 자동 테스트 **191개** 통과
- 벡터 저장소(SQLite + numpy)·웹 서버 직접 구현, 예산·호출 제한으로 비용 제어

### 📸 [ImgPls](https://github.com/naluteo89-sketch/ImgPls) · AI 이미지 합성 스튜디오 `🆕 v2 · 2026.10.19`
인물 사진과 배경 테마를 고르면 FLUX.2로 자연스럽게 합성하고, QR로 휴대폰에 전달하는 행사장용 키오스크 서비스
- 무거운 생성은 외부(Comfy Cloud)에, 웹 서버(FastAPI)는 중계·저장·공유만 담당
- 입력 검증·경로 차단 등 API 테스트 10종, 모의 서버로 생성 파이프라인 검증

### 🐫 Silkroad · 실크로드 그림 공방
Unity 그림판에서 그린 그림을 생성형 AI로 실크로드 회화풍 이미지로 바꿔 주는 문화 XR 체험 콘텐츠
- 그리기 → AI 변환 → 원본 비교 슬라이더 → 저장 → QR 공유 6단계 체험
- 서버 없이 테스트하는 더미 모드, 파이프라인 점검·스타일 품질 비교 도구

---

## 🔧 Maintenance Log

| 날짜 | 프로젝트 | 문제 | 조치 |
|---|---|---|---|
| 2026.10.19 | BuBot v2 | 자료에 없는 개별 거래가를 지역 평균으로 대신 답하는 등 **환각** | LLM `gpt-4o-mini` → `gpt-6-luna`, 48문항 평가로 찾은 질문 유형을 GPT 전 규칙으로 고정 |
| 2026.10.19 | ImgPls v2 | 로컬 GPU 서버가 꺼지면 생성 전부 실패(504) | **Comfy Cloud API** 전환, Cloud 미지원 노드 교체·경량 모델 재구성 |

---

## 📌 How I Work
- 🔢 **검증 가능한 AI**: AI가 추측하는 부분을 코드 규칙으로 옮기고 답에 근거를 붙입니다
- 🧪 **측정으로 판단**: 테스트와 정답 비교로 결과를 숫자로 확인합니다
- 📝 **기록으로 개선**: 이슈와 유지보수마다 증상·원인·조치를 남깁니다

---

## 📫 Contact
- Email: naluteo89@gmail.com
