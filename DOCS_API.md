# 📖 API Specification

본 프로젝트에서 제공하는 전체 API 목록입니다.

---

## 📋 1. 게시판 (Board)

| 기능 | 경로 | 메서드 |
| :--- | :--- | :---: |
| 전체 게시판 목록 조회 | `/post-boards` | GET |
| 게시판 상세 조회 | `/post-boards/{id}` | GET |
| 게시판 생성 | `/post-boards` | POST |
| 게시판별 게시글 목록 조회 | `/post-boards/{id}/posts` | GET |
| 게시판 수정 | `/post-boards/{id}` | PUT |
| 게시판 삭제 | `/post-boards/{id}` | DELETE |
| 게시글 상세 조회 | `/posts/{id}` | GET |
| 게시글 댓글 목록 조회 | `/posts/{id}/comments` | GET |
| 게시글 작성 | `/posts` | POST |
| 게시글 수정 | `/posts/{id}` | PUT |
| 게시글 삭제 | `/posts/{id}` | DELETE |
| 내가 쓴 게시글 조회 | `/posts/me` | GET |
| 최신 게시글 조회 | `/posts/latest` | GET |
| 댓글 작성 | `/comments` | POST |
| 댓글 수정 | `/comments/{id}` | PUT |
| 댓글 삭제 | `/comments/{id}` | DELETE |
| 내가 쓴 댓글 조회 | `/comments/me` | GET |

---

## 💬 2. 채팅 (Chat)

| 기능 | 경로 | 메서드 |
| :--- | :--- | :---: |
| 채팅방 생성 | `/chat/rooms` | POST |
| 채팅방 목록 조회 | `/chat/rooms` | GET |
| 채팅방 상세 조회 | `/chat/rooms/{roomId}` | GET |
| 채팅 참여자 조회 | `/chat/rooms/{roomId}/participants` | GET |
| 채팅방 이름 수정 | `/chat/rooms/{roomId}` | PATCH |
| 채팅방 삭제 | `/chat/rooms/{roomId}` | DELETE |
| 메시지 전송 | `/chat/messages` | POST |
| 메시지 조회 | `/chat/messages` | GET |

---

## ✅ 3. 작업 (Task)

| 기능 | 경로 | 메서드 |
| :--- | :--- | :---: |
| 작업 생성 | `/tasks` | POST |
| 작업 상세 조회 | `/tasks/{taskId}` | GET |
| 팀 작업 목록 조회 | `/tasks/team/{teamId}` | GET |
| 작업 수정 | `/tasks/{taskId}` | PUT |
| 작업 삭제 | `/tasks/{taskId}` | DELETE |
| 작업 로그 조회 | `/tasks/{taskId}/logs` | GET |
| 작업 댓글 목록 조회 | `/tasks/{taskId}/comments` | GET |
| 작업 댓글 작성 | `/tasks/{taskId}/comments` | POST |
| 담당자별 작업 조회 | `/tasks/assignee/{assigneeId}` | GET |
| 상태별 작업 조회 | `/tasks/team/{teamId}/status/{status}` | GET |
| 기간별 작업 조회 | `/tasks/team/{teamId}/date-range` | GET |
| 이번 주 작업 조회 | `/tasks/team/{teamId}/this-week` | GET |
| 작업 댓글 수정 | `/tasks/comments/{commentId}` | PUT |
| 작업 댓글 삭제 | `/tasks/comments/{commentId}` | DELETE |

---

## 👤 4. 사용자 및 팀 (User & Team)

| 기능 | 경로 | 메서드 |
| :--- | :--- | :---: |
| 회원가입 | `/api/user/signup` | POST |
| 회원가입 메일 인증 | `/api/user/signup-mail` | POST |
| 내 팀 조회 | `/api/user/team` | GET |
| 팀 가입 요청 | `/api/user/request` | POST |
| 팀 조회 | `/api/team` | GET |
| 팀 생성 | `/api/team` | POST |
| 팀 수정 | `/api/team` | PUT |
| 팀 삭제 | `/api/team` | DELETE |
| 팀 초대 | `/api/team/invite` | POST |
| 팀 멤버 조회 | `/api/team/members` | GET |

---

## 🔑 5. 인증 (Auth)

| 기능 | 경로 | 메서드 |
| :--- | :--- | :---: |
| 로그인 | `/api/auth/login` | POST |
| 내 정보 조회 | `/api/auth/me` | GET |
| 로그아웃 | `/api/auth/logout` | POST |
| 팀 전환 | `/api/auth/team` | POST |
| 토큰 재발급 | `/api/auth/refresh` | POST |

---

## 📁 6. 스토리지 (Storage)

| 기능 | 경로 | 메서드 |
| :--- | :--- | :---: |
| 파일 업로드 | `/api/storage/file` | POST |
| 폴더 업로드 | `/api/storage/folder` | POST |
| 폴더 내 목록 조회 | `/api/storage` | GET |
| 단일 노드 조회 | `/api/storage/{id}` | GET |
| 노드 삭제 | `/api/storage/{id}` | DELETE |
| 이름 변경 | `/api/storage/{id}/rename` | PATCH |
| 파일 이동 | `/api/storage/{id}/move` | PATCH |
| 다운로드 URL 생성 | `/api/storage/{id}/download` | GET |
| 저장소 사용량 조회 | `/api/storage/usage` | GET |
