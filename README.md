# 안녕하세요, 김다운입니다 👋

### AI의 답을 코드와 테스트로 검증하는 주니어 AI 서비스 개발자

LLM이 숫자·기간을 지어내는 문제를 **코드 규칙과 테스트**로 줄입니다.
부동산 RAG 챗봇에서 계산과 문장 생성의 역할을 분리해, **실제 API 평가 30문항의 정답률을 80% → 100%로 개선**했습니다.

기획부터 데이터 처리, 백엔드, 프론트엔드, 테스트까지 서비스 전체 흐름을 직접 구현합니다.

---

## 🛠 Tech Stack

**Languages**  
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Java](https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black)

**Frontend**  
![CSS](https://img.shields.io/badge/CSS-663399?style=flat-square&logo=css&logoColor=white)

**Backend**  
![Spring](https://img.shields.io/badge/Spring-6DB33F?style=flat-square&logo=spring&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)

**Database**  
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=flat-square&logo=mariadb&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)

**AI**  
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white)
![RAG](https://img.shields.io/badge/RAG-FF6F00?style=flat-square)
![ComfyUI](https://img.shields.io/badge/ComfyUI-222222?style=flat-square)

---

## 📂 Projects

### 🏠 [BuBot](https://github.com/naluteo89-sketch/BuBot) · 부동산 매매가 RAG 챗봇

자연어 질문으로 **전국 245개 지역 × 176개월의 아파트 평균 매매가**를 조회·비교하고, 계산 근거와 출처를 함께 보여주는 챗봇입니다.

- **정확도 개선**: 숫자는 Python이 계산하고, GPT는 해석과 문장 생성을 담당하도록 역할 분리
- **검증**: 실제 API 평가 30문항의 정답률 **80% → 100%** 개선, 자동 테스트 **191개** 통과
- **직접 구현**: SQLite + NumPy 기반 벡터 저장소와 웹 서버 구현
- **비용 제어**: 예산 및 API 호출 제한 적용

### 📸 [ImgPls](https://github.com/naluteo89-sketch/ImgPls) · AI 이미지 합성 스튜디오

인물 사진과 배경 테마를 선택하면 **ComfyUI(FLUX.2)로 이미지를 합성**하고, QR 코드로 휴대폰에 전달하는 행사장용 키오스크 서비스입니다.

- **역할 분리**: GPU 서버가 이미지 생성을 담당하고, FastAPI 웹 서버는 중계·저장·공유 처리
- **흐름 검증**: 모의 ComfyUI 서버로 생성 파이프라인 전체 검증
- **API 테스트**: API 테스트 10종으로 동작 확인

---

## 📌 How I Work

- 🔢 **검증 가능한 AI**: 숫자와 기간처럼 정확해야 하는 정보는 코드 규칙으로 처리하고, 답변에 근거를 붙입니다.
- 🧪 **측정으로 판단**: 테스트와 정답 비교로 개선 효과를 확인합니다.
- 📝 **기록으로 개선**: 이슈마다 증상·원인·조치를 남겨 다음 문제 해결에 활용합니다.

---

## 📫 Contact

- Email: [naluteo89@gmail.com](mailto:naluteo89@gmail.com)
