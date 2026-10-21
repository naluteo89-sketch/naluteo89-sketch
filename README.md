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
