<!-- Banner -->
<p align="center">
  <a href="https://ut.edu.vn/" title="University of Transport Ho Chi Minh City" style="border: none;">T
    <img src="https://portal.ut.edu.vn/images/logo_full.png" alt="University of Transport Ho Chi Minh City">
  </a>
</p>

<h1 align="center"><b>SOFTWARE TECHNOLOGY</b></h1>

# Members
| Order  | Full Name              |Role       | Github                                                  | Email                   |
| ------ |-----------------------:|----------:|--------------------------------------------------------:|-------------------------:
| 1      |Huỳnh Võ Hiền Nhân      |Team leader|[Hien-Nhan](https://github.com/Hien-Nhan)                |nhanhvh7835@ut.edu.vn    |
| 2      |Phạm Trí Nguyên         |Member     |[Tri-Nguyen](https://github.com/phamtringuyen66-lgtm)    |nguyenpt8807@ut.edu.vn   |
| 3      |Phạm Lê Ngọc Hân        |Member     |[kemm144](https://github.com/kemm144)                    |hanpln4560@ut.edu.vn     |
| 4      |Kiên Hoàng Duy          |Member     |[hoangduy2301](https://github.com/hoangduy2301)          |duykh0074@ut.edu.vn      |
| 5      |Lưu Minh Huy            |Member     |[huii68](https://github.com/huii68)                      |huylm3938@ut.edu.vn      |
| 6      |Võ Anh Duy              |Member     |[duyva99](https://github.com/duyva99)                    |duyva1608@ut.edu.vn      |
| 7      |Nguyễn Vũ Thuận         |Member     |[vux311](https://github.com/vux311)                      |thuannv2510@ut.edu.vn    |

* **Class Name:** SOFTWARE TECHNOLOGY
* **Class Code:** Update Sau
* **Teacher**: Ths: Nguyễn Văn Chiến

# Syllabus Management and Digitalization System (SMD)

![Project Status](https://img.shields.io/badge/Status-In_Development-blue?style=flat-square)
![Platform](https://img.shields.io/badge/Platform-Web_|_Mobile-orange?style=flat-square)
![Tech Stack](https://img.shields.io/badge/Stack-Python_|_ReactJS_|_AI-green?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-lightgrey?style=flat-square)

## 📖 Introduction

**SMD (Syllabus Management and Digitalization System)** is a comprehensive solution developed to address the challenges in managing university course syllabuses. 

Traditionally, universities struggle with decentralized storage (PDF/Word files), inconsistent formatting, and a lack of version control. **SMD** solves this by providing a centralized **Web & Mobile Platform** that digitizes the entire lifecycle of a syllabus. Key innovations include **AI-powered automation** for content validation (CLO-PLO mapping), semantic change detection, and automated summarization.

## 🎯 Project Goals

* **Centralization:** Unified storage for all academic content.
* **Standardization:** Ensure consistency in CLOs, PLOs, and assessment weights.
* **Transparency:** Clear, multi-tier approval workflows (Draft → Review → Approval).
* **Efficiency:** Reduce manual workload using AI and real-time notifications.

---

## 🚀 Key Features & Solutions

### 1. Centralized Syllabus Management
* **Digital Input:** Lecturers input content directly into the Web App (replacing static files).
* **Metadata Management:** Standardized fields for CLO (Input Standards), PLO (Output Standards), and prerequisites.
* **Version Control:** Git-like tracking (Replace, Update, New Version) organized by academic year.

### 2. Flexible Workflow Engine
* **Process:** `Draft` → `Pending Review` → `Pending Approval` → `Approved` → `Published`.
* **Roles:** Distinct workflows for Lecturers, Heads of Department (Reviewers), and Academic Affairs (Approvers).
* **Audit Logs:** Full history of edits and approval decisions for accreditation purposes.

### 3. AI & Automation 🤖
* **Semantic Change Detection:** AI detects meaningful changes between versions (Semantic Diff).
* **Logic Checking:** Validates consistency between Course Learning Outcomes (CLO) and Program Learning Outcomes (PLO).
* **Auto-Summarization:** Generates concise course summaries for students using GenAI.

### 4. Advanced Search & Visualization
* **Deep Search:** Filter by Subject Code, Lecturer, or Keywords within specific sections.
* **Visual Maps:** View CLO-PLO mapping tables and Subject Relationship Trees (Prerequisite/Parallel/Complementary).

### 5. Real-time Notifications
* **Subscription:** Students and staff can "Follow" subjects to receive updates via Email/App.
* **Alerts:** Immediate notifications for review deadlines or rejection status.

---

## 🛠 Technology Stack

The system is built on a **Service-Oriented / Microservices Architecture**, separating the core management logic from heavy AI processing.

### Core System
| Component | Technology | Description |
| :--- | :--- | :--- |
| **Backend API** | **Python** | Core business logic and API Gateway. |
| **Web Client** | **ReactJS / Next.js** | Interface for Admin, Lecturers, and Approvers. |
| **Mobile Client** | **React Native** | Optimized interface for Students. |
| **Database** | **MySQL** | Transactional data (Users, Workflow, Syllabus metadata). |
| **Cache** | **Redis** | Session management and high-speed caching. |

### AI & Data Processing Microservice
| Component | Technology | Description |
| :--- | :--- | :--- |
| **Architecture** | **FastAPI + Celery** | Event-driven async processing (via RabbitMQ/Redis). |
| **Vector DB** | **PostgreSQL + pgvector** | Storage for vector embeddings and relational AI data. |
| **Search Engine**| **Elasticsearch** | Full-text search engine for syllabus content. |
| **NLP Models** | **PhoBERT / ViBERT** | Vietnamese language processing. |
| **GenAI** | **Llama 3 / Gemini API** | Summarization and content generation. |
| **Orchestration**| **LangChain** | Managing AI flows and context. |
| **Crawler/OCR** | **Selenium / Tesseract** | Data collection and PDF digitization. |

---

## 👥 User Roles (RBAC)

1.  **System Admin:** User management, system configuration, parameter setup.
2.  **Lecturer:** Create/Update syllabus, map CLO-PLO, submit for review.
3.  **Head of Department (HoD):** **Level 1 Approval**. Verifies academic content and technical correctness.
4.  **Academic Affairs (AA):** **Level 2 Approval**. Verifies compliance with institutional standards (PLO mapping, Credits).
5.  **Principal:** **Strategic Approval**. Final sign-off for high-level documents and reports.
6.  **Student:** View public syllabus, see AI summaries, track subject roadmap.

---

## 📂 Development Roadmap

The project is divided into 9 core task packages:

* [ ] **Task 1:** System Admin Web App (User Mgmt, Config).
* [ ] **Task 2:** Lecturer Web App (Syllabus Creation & Updates).
* [ ] **Task 3:** Reviewer & Approver Web App (HoD & AA Workflow).
* [ ] **Task 4:** Internal Lookup & Analysis Tools (Comparison & Reports).
* [ ] **Task 5:** Student Web & Mobile App.
* [ ] **Task 6:** AI & Crawler Microservice (Logic Check, Semantic Diff, Summary).
* [ ] **Task 7:** Core Web API Development.
* [ ] **Task 8:** System Integration, Testing (Performance, Security) & Deployment.
* [ ] **Task 9:** Documentation (SRS, URD, User Manuals).

---

## 🔧 Installation (For Developers)

### Prerequisites
* Docker & Docker Compose
* Python 3.9+
* Node.js 18+

### Setup Steps
1.  **Clone the repository**
    ```bash
    git clone [https://github.com/your-org/smd-system.git](https://github.com/your-org/smd-system.git)
    cd smd-system
    ```

2.  **Environment Configuration**
    Create a `.env` file in the root directory based on `.env.example`.

3.  **Run with Docker Compose**
    ```bash
    docker-compose up -d --build
    ```

4.  **Access the System**
    * Web App: `http://localhost:3000`
    * API Docs: `http://localhost:8000/docs`
    * Kibana (Logs): `http://localhost:5601`

---

## 📄 License

This project is a group project of students from **[Ho Chi Minh City University of Transport]**.
Unauthorized copying of this file, via any medium is strictly prohibited.
