# 🚀 Collabity

<div align="center">
  <p><b>통합 클라우드 스토리지와 매끄러운 워크플로우를 제공하는 차세대 협업 플랫폼</b></p>
  <br />
</div>

---

## 📌 프로젝트 개요
**Collabity**는 팀 협업을 효율적으로 지원하는 협업 플랫폼입니다.  
**Spring Boot** 기반 백엔드와 **Next.js** 프론트엔드를 결합하여 문서 관리, 실시간 협업, 안전한 자산 저장(AWS S3)을 하나의 환경에서 제공합니다.

---

## ✨ 주요 기능
- **📂 S3 기반 자산 관리**  
  AWS S3를 활용한 확장 가능하고 안정적인 파일 저장 전략
- **⚡ 인터랙티브 워크스페이스**  
  드래그 앤 드롭(DnD Kit)과 풍부한 텍스트 편집(Toast UI Editor) 지원
- **🔐 엔터프라이즈급 보안**  
  JWT와 Spring Security를 통한 안전한 인증 및 권한 관리
- **🚀 고성능 처리**  
  Redis 캐싱과 최적화된 JPA 쿼리를 통한 빠른 데이터 접근
- **🔄 데이터 무결성 보장**  
  Flyway를 활용한 신뢰성 있는 DB 마이그레이션 및 버전 관리

---

## 🛠 기술 스택

### 🟦 백엔드
| 구분 | 기술 |
| :--- | :--- |
| **프레임워크** | ![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.5.8-6DB33F?logo=springboot&logoColor=white) |
| **언어** | ![Java](https://img.shields.io/badge/Java-17-007396?logo=openjdk&logoColor=white) |
| **DB / 캐시** | ![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?logo=mysql&logoColor=white) ![Redis](https://img.shields.io/badge/Redis-7.0-DC382D?logo=redis&logoColor=white) |
| **스토리지** | ![AWS S3](https://img.shields.io/badge/AWS_S3-Storage-FF9900?logo=amazons3&logoColor=white) |
| **기타** | ![JWT](https://img.shields.io/badge/JWT-Authentication-000000?logo=jsonwebtokens&logoColor=white) ![Flyway](https://img.shields.io/badge/Flyway-Migrations-CC0202?logo=flyway&logoColor=white) |

### 🟥 프론트엔드
| 구분 | 기술 |
| :--- | :--- |
| **프레임워크** | ![Next.js](https://img.shields.io/badge/Next.js-16.1.1-000000?logo=nextdotjs&logoColor=white) |
| **라이브러리** | ![React](https://img.shields.io/badge/React-18.3.1-61DAFB?logo=react&logoColor=white) |
| **언어** | ![TypeScript](https://img.shields.io/badge/TypeScript-5.0-3178C6?logo=typescript&logoColor=white) |
| **스타일링** | ![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.4-06B6D4?logo=tailwindcss&logoColor=white) |
| **편집기 / UI** | ![Toast UI](https://img.shields.io/badge/Toast_UI-Editor-007AFF) ![DnD Kit](https://img.shields.io/badge/DnD_Kit-Interactive-FF4081) |

---

## 📂 프로젝트 구조

```bash
collabity/
├── collabity-backend/        # Spring Boot 백엔드
│   ├── src/main/java/        # Java 소스 코드
│   ├── src/main/resources/   # 설정 파일 (S3, Redis, DB)
│   └── build.gradle          # 백엔드 의존성
├── collabity-frontend/       # Next.js 프론트엔드
│   ├── src/                  # React 컴포넌트 & 페이지
│   ├── public/               # 정적 자원
│   └── package.json          # 프론트엔드 의존성
└── .github/                  # CI/CD 워크플로우

```
---

## 🏗 심화 내용

<details>
<summary><b>🗄 데이터베이스 ERD</b></summary>
<p>데이터베이스는 Spring Data JPA로 관리되며 Flyway로 버전 관리됩니다. 주요 엔티티는 Users, Projects, Documents, Attachments 등입니다.</p>
<!-- ERD 이미지 삽입 가능 -->
</details>

<details>
<summary><b>📄 상세 API 문서 보기 (Click)</b></summary>
<p>백엔드 실행 후 Swagger UI를 통해 상호작용 가능한 API 문서 확인 가능</p>
<pre><code>http://localhost:8080/swagger-ui/index.html</code></pre>

| 분류 | 주요 기능 | 
| :--- | :--- | 
| **Board** | 게시판/게시글/댓글 CRUD 및 조회 | 
| **Chat** | 채팅방 생성/관리 및 메시지 송수신 | 
| **Task** | 팀별 작업 생성, 상태/기간별 조회 및 로그 | 
| **User/Team** | 회원가입, 팀 관리 및 멤버 초대 |
| **Auth** | 로그인/로그아웃, 토큰 재발급 | 
| **File** | 파일/폴더 업로드, 다운로드, 스토리지 관리 | 

👉 [전체 API 명세서 상세 보기](./DOCS_API.md)
</details>

---

<div align="center">
  <p>© 2026 Collabity 팀. 모든 권리 보유.</p>
</div>
