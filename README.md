[English](README.en.md) | **한국어**

# 안녕하세요, AI 서비스 개발자 김다운입니다 👋

> **"AI가 틀릴 수 있는 부분은 코드로 막고, 결과는 숫자로 확인합니다."**

생성형 AI를 활용해 서비스를 빠르게 만들되, AI가 임의로 숫자를 지어내거나 답이 흔들리는 문제는 규칙과 테스트로 해결해 왔습니다.  
부동산 시세 챗봇에서는 이 방식으로 **답변 정확도를 80%에서 100%로** 높였습니다.  
서비스를 공개한 뒤에도 문제를 찾아 개선하고, 그 과정을 버전별로 기록하고 있습니다.

---

## 📌 핵심 역량

| 역량 | 내용 |
|---|---|
| **신뢰할 수 있는 AI 서비스 설계** | 계산·판정처럼 정확해야 하는 일은 코드가, 설명·요약은 AI가 맡도록 역할을 나눠 AI의 오답(환각)을 줄입니다 |
| **데이터로 판단하는 개발** | 평가 문항과 자동 테스트를 먼저 만들고, 개선 여부를 수치로 확인합니다 |
| **비용과 운영을 고려한 구조** | AI 호출 횟수를 줄이고, 장비 장애에도 서비스가 멈추지 않도록 클라우드로 전환하는 등 실제 운영 환경을 고려합니다 |
| **기획부터 완성까지** | 문제 정의 → 기획 → 개발 → 테스트 → 문서화까지 직접 진행합니다 |

---

## 💡 문제 해결 과정

프로젝트마다 아래 순서로 문제에 접근합니다.

1. **불편함 정의** — 실제 사용자가 겪는 문제를 글로 정리하고, 기존 서비스가 해결하지 못하는 이유를 비교합니다.
2. **AI와 코드의 역할 분담** — 틀리면 안 되는 부분은 코드로, 사람처럼 해석해야 하는 부분만 AI에 맡깁니다.
3. **측정 후 설계 변경** — 추측으로 정하지 않고, 점검 스크립트와 평가 문항으로 먼저 확인한 뒤 방향을 정합니다.
4. **구조로 한계 극복** — 장비 성능이나 비용의 한계를 만나면 처리 방식 자체를 바꿉니다.
5. **기록과 재검증** — 문제의 증상·원인·조치를 기록하고, 테스트로 같은 문제가 반복되지 않게 합니다.

---

## 📂 프로젝트

### 📰 [news_Moa](https://github.com/naluteo89-sketch/news_Moa) — 네이버 뉴스 논조 분석 서비스 `2026.10`

> 뉴스 검색 결과를 모아 기사별 **긍정·부정 분위기, 핵심 키워드, 핵심 문장**을 한눈에 보여 주는 웹 서비스

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

### 🥽 [Pano360 Studio](https://github.com/naluteo89-sketch/co_show_2026) — CO-SHOW 2026 전시용 360° VR 콘텐츠 제작 도구 `2026.10 · 1차 완료`

> 사진 한 장으로 **VR 기기(Meta Quest 3)에서 볼 수 있는 360° 이미지와 영상**을 만드는 웹 제작 도구와 VR 뷰어

- **기획 배경**  
  전시장 방문객이 고른 사진 한 장을 360° 공간으로 넓히고, 그 안에서 일어나는 장면을 VR로 체험할 수 있게 하는 것이 목표였습니다.
- **고민한 점**  
  사람이 판단해야 할 부분(배치, 장면 설명, 움직일 영역 선택)과 프로그램이 자동으로 처리할 부분(이미지 생성 설정, 품질 점검, 영상 합성)을 먼저 표로 나눠 설계했습니다.
- **해결 과정**
  - AI가 사진의 장면·조명·화각을 분석해 생성 설정값을 만들고, 이미지 생성 AI로 360° 이미지를 완성한 뒤 **8K(8192×4096) 해상도**로 높였습니다.
  - 360° 영상 전체를 한 번에 만들면 움직임이 작게 나오고 서버 메모리가 부족했습니다. 그래서 **사용자가 지정한 영역만 고화질로 생성한 뒤 전체 영상에 합성**하는 방식으로 바꿔 해결했습니다.
  - 실제 AI 서버나 GPU 없이도 돌아가는 테스트 환경을 만들고, 이미지 이음새 품질을 점수로 측정했습니다.
- **사용 기술**: Python, aiohttp, OpenAI, ComfyUI / Comfy Cloud, FLUX.2, LTX-2.3, FFmpeg, Unity 6, Meta Quest 3

### 🏠 [BuBot](https://github.com/naluteo89-sketch/BuBot) — 아파트 매매가 조회 AI 챗봇 `2026.10 · v2`

> 전국 245개 지역, 176개월치 아파트 평균 매매가를 **대화로 묻고 비교**할 수 있고, 모든 답변에 **계산 근거와 출처**를 함께 보여 주는 챗봇

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

### 📸 [ImgPls](https://github.com/naluteo89-sketch/ImgPls) — AI 사진 합성 키오스크 `2026.10 · v2`

> 인물 사진과 배경을 고르면 AI가 자연스럽게 합성하고, **QR 코드로 휴대폰에 바로 전달**하는 행사장용 서비스

- **기획 배경**  
  행사장 PC 한 대만으로 방문객 사진을 찍어 즉석에서 합성하고, 결과물을 휴대폰으로 받아 갈 수 있게 하고자 했습니다.
- **고민한 점**  
  처음에는 현장 GPU 서버를 사용했는데, 서버가 꺼지면 모든 요청이 실패했습니다. 현장 장비 상태와 관계없이 동작하는 구조가 필요했습니다.
- **해결 과정**
  - 무거운 이미지 생성은 **클라우드 서비스(Comfy Cloud)로 옮기고**, 웹 서버는 요청 전달·저장·공유만 담당하게 했습니다.
  - 클라우드에서 지원하지 않는 기능을 직접 확인해 대체 기능으로 교체했습니다.
  - 파일 형식·용량 제한, 허용되지 않은 경로 접근 차단 등 **API 테스트 10종**을 만들고, 가상 서버로 전체 흐름을 검증했습니다.
- **사용 기술**: Python, FastAPI, Jinja2, ComfyUI / Comfy Cloud, FLUX.2, WebSocket, Playwright

### 🐫 [Silkroad](https://github.com/naluteo89-sketch/silkroad) — 실크로드 그림 공방 (문화 XR 체험 콘텐츠) `2026.10`

> 태블릿 그림판에 그린 그림을 생성형 AI가 **실크로드 회화풍 작품으로 바꿔 주는** 체험 콘텐츠

- **기획 배경**  
  관람객이 직접 그린 그림이 실크로드 회화로 바뀌는 경험을 통해 문화 콘텐츠에 자연스럽게 참여하도록 하고자 했습니다.
- **고민한 점**  
  AI 서버가 없으면 체험 흐름 전체를 확인할 수 없었습니다. 그래서 이미지 생성과 화면 흐름을 분리해 각각 검증할 수 있게 했습니다.
- **해결 과정**
  - 그리기 → AI 변환 → 원본과 비교 → 저장 → QR 공유로 이어지는 체험 흐름을 구현했습니다.
  - 서버 없이도 테스트할 수 있는 **더미 모드**와 화풍 품질 비교 도구를 만들었습니다.
  - 배포용 앱에 인증 키가 남는 보안 문제를 직접 점검해 문서로 정리하고, 개선 방향(서버에서 키 관리)을 제시했습니다.
- **사용 기술**: Unity 6, C#, ComfyUI / Comfy Cloud, SDXL, FLUX.2, Android 태블릿

---

## 🛠 기술 스택

**언어**  
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Java](https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black)
![C#](https://img.shields.io/badge/C%23-512BD4?style=flat-square&logo=dotnet&logoColor=white)

**프론트엔드**  
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS-1572B6?style=flat-square&logo=css3&logoColor=white)

**백엔드**  
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)
![aiohttp](https://img.shields.io/badge/aiohttp-2C5BB4?style=flat-square&logo=aiohttp&logoColor=white)
![Spring](https://img.shields.io/badge/Spring-6DB33F?style=flat-square&logo=spring&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)

**데이터베이스**  
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=flat-square&logo=mariadb&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)

**AI · XR**  
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white)
![RAG](https://img.shields.io/badge/RAG-FF6F00?style=flat-square)
![ComfyUI](https://img.shields.io/badge/ComfyUI%20%2F%20Comfy%20Cloud-222222?style=flat-square)
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
