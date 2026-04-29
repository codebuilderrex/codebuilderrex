<img width="159" height="150" alt="backend_layer_architecture" src="https://github.com/user-attachments/assets/e0e47ff8-7d6f-4bab-9e26-9269fc98948b" />

  <!-- Layer 2: Application -->
  
  




<img width="94" height="150" alt="file_ia_structure" src="https://github.com/user-attachments/assets/0bde3ef0-b01c-4756-88cc-a0a6c2b3f1a6" />



<img width="165" height="150" alt="jarvis_system_architecture" src="https://github.com/user-attachments/assets/fe1c6f47-945e-43fc-8e3b-22b425a45e73" />




# 🤖 JARVIS: AI-Powered Desktop Automation & HUD System

JARVIS는 **MediaPipe 기반의 제스처 인식**과 **LLM(Claude API)**을 결합하여 사용자의 데스크탑 환경을 지능적으로 제어하고, **Three.js 기반의 HUD(Head-Up Display)**를 통해 실시간 피드백을 제공하는 차세대 자동화 시스템입니다.

---

## 🏗️ System Architecture

사용자의 입력부터 외부 서비스 연동, 그리고 시각적 출력까지의 전체적인 흐름입니다.

| 단계 | 구성 요소 | 기술 스택 |
| :--- | :--- | :--- |
| **Input** | 카메라 / USB 입력 | OpenCV, MediaPipe |
| **Processing** | 제스처 분석 및 명령 처리 | FastAPI, WebSocket, pyautogui |
| **Intelligence** | AI 에이전트 (JARVIS) | Claude API, LangChain |
| **Integration** | 외부 서비스 연동 | Google Calendar API, Notion API |
| **Output** | 실시간 시각화 (HUD) | Electron, React, Three.js |

---

## 💻 Backend Layered Architecture

백엔드는 유지보수와 확장성을 고려하여 **계층화된 아키텍처(Layered Architecture)**를 채택했습니다.

1.  **Presentation Layer (`api/`)**
    * FastAPI 라우터 및 WebSocket 핸들러 관리
    * Pydantic을 활용한 Request/Response 스키마 정의
2.  **Application Layer (`services/`)**
    * 비즈니스 로직 및 유즈케이스 오케스트레이션
    * `GestureService`, `AIService`, `WindowService` 등
3.  **Domain Layer (`domain/`)**
    * 시스템의 핵심 모델 및 비즈니스 규칙
    * `GestureEvent`, `AIResponse`, `WindowCommand` 등
4.  **Infrastructure Layer (`infrastructure/`)**
    * 외부 라이브러리 및 하드웨어 제어를 위한 어댑터
    * MediaPipe, Claude API Client, pyautogui, SQLite/Redis 연동
5.  **Data & External Layer**
    * 데이터 지속성 및 외부 API 인터페이스

---

## 📂 Project Structure (IA)

```text
jarvis-backend/
├── app/
│   ├── api/             # Presentation: Routes, Schemas
│   ├── services/        # Application: Business Logic
│   ├── domain/          # Domain: Models, Entities
│   ├── infrastructure/  # Infrastructure: Adapters, Repositories
│   └── core/            # Core: Config, Dependencies, Database
├── tests/               # Unit & Integration Tests (pytest)
├── migrations/          # DB Migration (Alembic)
└── scripts/             # Dev/Seed/Deploy Scripts



올려주신 이미지들(IA 구조, 시스템 아키텍처, 백엔드 레이어 아키텍처)을 바탕으로, 조직(Organization)이나 프로젝트 메인에 바로 사용하실 수 있는 고품질의 README.md 파일을 작성해 드립니다.

이 내용은 GitHub의 마크다운 형식을 따르며, 시각적으로 깔끔하게 구성되었습니다.

Markdown
# 🤖 JARVIS: AI-Powered Desktop Automation & HUD System

JARVIS는 **MediaPipe 기반의 제스처 인식**과 **LLM(Claude API)**을 결합하여 사용자의 데스크탑 환경을 지능적으로 제어하고, **Three.js 기반의 HUD(Head-Up Display)**를 통해 실시간 피드백을 제공하는 차세대 자동화 시스템입니다.

---

## 🏗️ System Architecture

사용자의 입력부터 외부 서비스 연동, 그리고 시각적 출력까지의 전체적인 흐름입니다.

| 단계 | 구성 요소 | 기술 스택 |
| :--- | :--- | :--- |
| **Input** | 카메라 / USB 입력 | OpenCV, MediaPipe |
| **Processing** | 제스처 분석 및 명령 처리 | FastAPI, WebSocket, pyautogui |
| **Intelligence** | AI 에이전트 (JARVIS) | Claude API, LangChain |
| **Integration** | 외부 서비스 연동 | Google Calendar API, Notion API |
| **Output** | 실시간 시각화 (HUD) | Electron, React, Three.js |

---

## 💻 Backend Layered Architecture

백엔드는 유지보수와 확장성을 고려하여 **계층화된 아키텍처(Layered Architecture)**를 채택했습니다.

1.  **Presentation Layer (`api/`)**
    * FastAPI 라우터 및 WebSocket 핸들러 관리
    * Pydantic을 활용한 Request/Response 스키마 정의
2.  **Application Layer (`services/`)**
    * 비즈니스 로직 및 유즈케이스 오케스트레이션
    * `GestureService`, `AIService`, `WindowService` 등
3.  **Domain Layer (`domain/`)**
    * 시스템의 핵심 모델 및 비즈니스 규칙
    * `GestureEvent`, `AIResponse`, `WindowCommand` 등
4.  **Infrastructure Layer (`infrastructure/`)**
    * 외부 라이브러리 및 하드웨어 제어를 위한 어댑터
    * MediaPipe, Claude API Client, pyautogui, SQLite/Redis 연동
5.  **Data & External Layer**
    * 데이터 지속성 및 외부 API 인터페이스

---

## 📂 Project Structure (IA)

```text
jarvis-backend/
├── app/
│   ├── api/             # Presentation: Routes, Schemas
│   ├── services/        # Application: Business Logic
│   ├── domain/          # Domain: Models, Entities
│   ├── infrastructure/  # Infrastructure: Adapters, Repositories
│   └── core/            # Core: Config, Dependencies, Database
├── tests/               # Unit & Integration Tests (pytest)
├── migrations/          # DB Migration (Alembic)
└── scripts/             # Dev/Seed/Deploy Scripts
🛠️ Tech Stack
Backend: Python 3.x, FastAPI, SQLAlchemy, Alembic

AI/ML: MediaPipe Hands, Claude API (Anthropic), LangChain

Automation: pyautogui, win32api

Frontend/HUD: React, Three.js, Electron

Database/Cache: SQLite, Redis

🚀 Getting Started
Prerequisites
Python 3.10+

Webcam (제스처 인식용)

Anthropic API Key (AI 기능 사용 시)


Installation
git clone [https://github.com/your-org/jarvis-backend.git](https://github.com/your-org/jarvis-backend.git)
pip install -r requirements.txt
cp .env.example .env
uvicorn app.main:app --reload


올려주신 이미지들(IA 구조, 시스템 아키텍처, 백엔드 레이어 아키텍처)을 바탕으로, 조직(Organization)이나 프로젝트 메인에 바로 사용하실 수 있는 고품질의 README.md 파일을 작성해 드립니다.

이 내용은 GitHub의 마크다운 형식을 따르며, 시각적으로 깔끔하게 구성되었습니다.

Markdown
# 🤖 JARVIS: AI-Powered Desktop Automation & HUD System

JARVIS는 **MediaPipe 기반의 제스처 인식**과 **LLM(Claude API)**을 결합하여 사용자의 데스크탑 환경을 지능적으로 제어하고, **Three.js 기반의 HUD(Head-Up Display)**를 통해 실시간 피드백을 제공하는 차세대 자동화 시스템입니다.

---

## 🏗️ System Architecture

사용자의 입력부터 외부 서비스 연동, 그리고 시각적 출력까지의 전체적인 흐름입니다.

| 단계 | 구성 요소 | 기술 스택 |
| :--- | :--- | :--- |
| **Input** | 카메라 / USB 입력 | OpenCV, MediaPipe |
| **Processing** | 제스처 분석 및 명령 처리 | FastAPI, WebSocket, pyautogui |
| **Intelligence** | AI 에이전트 (JARVIS) | Claude API, LangChain |
| **Integration** | 외부 서비스 연동 | Google Calendar API, Notion API |
| **Output** | 실시간 시각화 (HUD) | Electron, React, Three.js |

---

## 💻 Backend Layered Architecture

백엔드는 유지보수와 확장성을 고려하여 **계층화된 아키텍처(Layered Architecture)**를 채택했습니다.

1.  **Presentation Layer (`api/`)**
    * FastAPI 라우터 및 WebSocket 핸들러 관리
    * Pydantic을 활용한 Request/Response 스키마 정의
2.  **Application Layer (`services/`)**
    * 비즈니스 로직 및 유즈케이스 오케스트레이션
    * `GestureService`, `AIService`, `WindowService` 등
3.  **Domain Layer (`domain/`)**
    * 시스템의 핵심 모델 및 비즈니스 규칙
    * `GestureEvent`, `AIResponse`, `WindowCommand` 등
4.  **Infrastructure Layer (`infrastructure/`)**
    * 외부 라이브러리 및 하드웨어 제어를 위한 어댑터
    * MediaPipe, Claude API Client, pyautogui, SQLite/Redis 연동
5.  **Data & External Layer**
    * 데이터 지속성 및 외부 API 인터페이스

---

## 📂 Project Structure (IA)

```text
jarvis-backend/
├── app/
│   ├── api/             # Presentation: Routes, Schemas
│   ├── services/        # Application: Business Logic
│   ├── domain/          # Domain: Models, Entities
│   ├── infrastructure/  # Infrastructure: Adapters, Repositories
│   └── core/            # Core: Config, Dependencies, Database
├── tests/               # Unit & Integration Tests (pytest)
├── migrations/          # DB Migration (Alembic)
└── scripts/             # Dev/Seed/Deploy Scripts
🛠️ Tech Stack
Backend: Python 3.x, FastAPI, SQLAlchemy, Alembic

AI/ML: MediaPipe Hands, Claude API (Anthropic), LangChain

Automation: pyautogui, win32api

Frontend/HUD: React, Three.js, Electron

Database/Cache: SQLite, Redis

🚀 Getting Started
Prerequisites
Python 3.10+

Webcam (제스처 인식용)

Anthropic API Key (AI 기능 사용 시)

Installation
Repository 클론

Bash
git clone [https://github.com/your-org/jarvis-backend.git](https://github.com/your-org/jarvis-backend.git)
가상환경 설정 및 패키지 설치

Bash
pip install -r requirements.txt
환경 변수 설정 (.env.example 참고)

Bash
cp .env.example .env
서버 실행

Bash
uvicorn app.main:app --reload
© 2026 JARVIS Project. Built with ❤️ for intelligent automation.


---

### 💡 작성 팁
* **이미지 삽입:** 만약 위 README에 올려주신 이미지들을 직접 넣고 싶으시다면, GitHub 레포지토리에 이미지 파일을 업로드한 뒤 마크다운 내에 `![alt text](이미지경로)` 형식으로 추가하시면 됩니다.
* **Organization 적용:** 이전 답변에서 안내해 드린 것처럼, 조직의 `.github` 레포지토리 내 `pro
