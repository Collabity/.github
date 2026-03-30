# 📖 Full API Specification

이 문서는 프로젝트에서 제공하는 모든 API 명세를 상세히 기술합니다. (총 63개 API)

---

## 📋 1. 게시판 (Board)
[cite_start]게시판 생성, 게시글 관리 및 댓글 관련 API입니다. [cite: 4]

| 기능 | 경로 | 메서드 | 설명 |
| :--- | :--- | :---: | :--- |
| 전체 게시판 목록 조회 | `/post-boards` | [cite_start]GET | [cite: 4] |
| 게시판 상세 조회 | `/post-boards/{id}` | [cite_start]GET | [cite: 4] |
| 게시판 추가 | `/post-boards` | [cite_start]POST | [cite: 4] |
| 게시판 별 게시글 목록 조회 | `/post-boards/{id}/posts` | [cite_start]GET | [cite: 4] |
| 게시판 수정 | `/post-boards/{id}` | [cite_start]PUT | [cite: 4] |
| 게시판 삭제 | `/post-boards/{id}` | [cite_start]DELETE | [cite: 4] |
| 게시글 상세 조회 | `/posts/{id}` | [cite_start]GET | [cite: 4] |
| 게시글 별 댓글 목록 조회 | `/posts/{id}/comments` | [cite_start]GET | [cite: 4] |
| 게시글 작성 | `/posts` | [cite_start]POST | [cite: 4] |
| 게시글 수정 | `/posts/{id}` | [cite_start]PUT | [cite: 4] |
| 게시글 삭제 | `/posts/{id}` | [cite_start]DELETE | [cite: 4] |
| 내가 쓴 게시글 목록 조회 | `/posts/me` | [cite_start]GET | [cite: 4] |
| 최신 게시글 목록 조회 | `/posts/latest` | [cite_start]GET | [cite: 4] |
| 댓글 작성 | `/comments` | [cite_start]POST | [cite: 4] |
| 댓글 수정 | `/comments/{id}` | [cite_start]PUT | [cite: 4] |
| 댓글 삭제 | `/comments/{id}` | [cite_start]DELETE | [cite: 7] |
| 내가 쓴 댓글 목록 조회 | `/comments/me` | [cite_start]GET | [cite: 7] |

## 💬 2. 채팅 (Chat)
[cite_start]실시간 소통을 위한 채팅방 및 메시지 관리 API입니다. [cite: 7]

| 기능 | 경로 | 메서드 | 설명 |
| :--- | :--- | :---: | :--- |
| 채팅방 생성 | `/chat/rooms` | POST | [cite_start]방 타입, 이름, 참여자 등 포함 [cite: 7] |
| 채팅방 조회 | `/chat/rooms` | GET | [cite_start]사용자가 참여 중인 방만 조회 [cite: 7] |
| 채팅방 상세 조회 | `/chat/rooms/{roomId}` | [cite_start]GET | [cite: 7] |
| 채팅 참여자 조회 | `/chat/rooms/{roomId}/participants` | [cite_start]GET | [cite: 7] |
| 채팅방 이름 수정 | `/chat/rooms/{roomId}` | PATCH | [cite_start]새 이름 전달 [cite: 7] |
| 채팅방 삭제 | `/chat/rooms/{roomId}` | [cite_start]DELETE | [cite: 7] |
| 메시지 전송 | `/chat/messages` | [cite_start]POST | [cite: 7] |
| 메시지 조회 | `/chat/messages` | GET | [cite_start]`roomId`, `page`, `size` 파라미터 사용 [cite: 7] |

## ✅ 3. 작업 (Task)
[cite_start]팀 프로젝트 내의 할 일(Task) 및 로그 관리 API입니다. [cite: 7, 10]

| 기능 | 경로 | 메서드 | 설명 |
| :--- | :--- | :---: | :--- |
| 작업 생성 | `/tasks` | [cite_start]POST | [cite: 7] |
| 작업 상세 조회 | `/tasks/{taskId}` | [cite_start]GET | [cite: 7] |
| 팀의 전체 작업 목록 조회 | `/tasks/team/{teamId}` | [cite_start]GET | [cite: 7] |
| 작업 수정 | `/tasks/{taskId}` | [cite_start]PUT | [cite: 7] |
| 작업 삭제 | `/tasks/{taskId}` | [cite_start]DELETE | [cite: 10] |
| 작업 로그 조회 | `/tasks/{taskId}/logs` | [cite_start]GET | [cite: 10] |
| 작업 댓글 목록 조회 | `/tasks/{taskId}/comments` | [cite_start]GET | [cite: 10] |
| 작업 댓글 작성 | `/tasks/{taskId}/comments` | [cite_start]POST | [cite: 10] |
| 담당자별 작업 조회 | `/tasks/assignee/{assigneeId}` | [cite_start]GET | [cite: 10] |
| 상태별 작업 조회 | `/tasks/team/{teamId}/status/{status}` | [cite_start]GET | [cite: 10] |
| 기간별 작업 조회 | `/tasks/team/{teamId}/date-range` | [cite_start]GET | [cite: 10] |
| 이번주 작업 조회 | `/tasks/team/{teamId}/this-week` | [cite_start]GET | [cite: 10] |
| 작업 댓글 수정 | `/tasks/comments/{commentid}` | [cite_start]PUT | [cite: 10] |
| 작업 댓글 삭제 | `/tasks/comments/{commentId}` | [cite_start]DELETE | [cite: 10] |

## 👤 4. 사용자 및 팀 (User & Team)
[cite_start]회원 정보 및 소속 팀 관리 API입니다. [cite: 10, 13]

| 기능 | 경로 | 메서드 | 설명 |
| :--- | :--- | :---: | :--- |
| 회원가입 | `/api/user/signup` | POST | [cite_start]메일 인증 추가 예정 [cite: 10] |
| 회원가입 메일 인증 | `/api/user/signup-mail` | [cite_start]POST | [cite: 10] |
| 사용자가 속한 팀 조회 | `/api/user/team` | [cite_start]GET | team uuid 조회 (id 노출X) [cite: 10] |
| 팀 가입 요청 | `/api/user/request` | [cite_start]POST | [cite: 13] |
| 팀 정보 조회 | `/api/team` | [cite_start]GET | [cite: 13] |
| 팀 생성 | `/api/team` | [cite_start]POST | [cite: 13] |
| 팀 수정 | `/api/team` | [cite_start]PUT | [cite: 13] |
| 팀 삭제 | `/api/team` | [cite_start]DELETE | [cite: 13] |
| 팀 멤버 초대 | `/api/team/invite` | [cite_start]POST | [cite: 13] |
| 팀 전체 멤버 조회 | `/api/team/members` | [cite_start]GET | [cite: 13] |

## 🔑 5. 인증 및 인가 (Auth)
[cite_start]보안 및 세션 관리 API입니다. [cite: 13]

| 기능 | 경로 | 메서드 | 설명 |
| :--- | :--- | :---: | :--- |
| 로그인 | `/api/auth/login` | [cite_start]POST | [cite: 13] |
| 로그인 정보 확인 | `/api/auth/me` | [cite_start]GET | [cite: 13] |
| 로그아웃 | `/api/auth/logout` | [cite_start]POST | [cite: 13] |
| 팀 선택 및 전환 | `/api/auth/team` | POST | [cite_start]선택 시 JWT 토큰 업데이트 [cite: 13] |
| 토큰 재발급 | `/api/auth/refresh` | POST | [cite_start]401 에러 발생 시 재발급 [cite: 13] |

## 📁 6. 파일 및 스토리지 (Storage)
[cite_start]파일 업로드 및 클라우드 저장소 관리 API입니다. [cite: 13, 14]

| 기능 | 경로 | 메서드 | 설명 |
| :--- | :--- | :---: | :--- |
| 파일 업로드 | `/api/storage/file` | [cite_start]POST | [cite: 13] |
| 폴더 업로드 | `/api/storage/folder` | [cite_start]POST | [cite: 13] |
| 특정 폴더 내부 노드 목록 조회 | `/api/storage` | [cite_start]GET | [cite: 13] |
| 단일 노드 데이터 조회 | `/api/storage/{Id}` | [cite_start]GET | files_node id를 통해 참조 [cite: 13] |
| 단일 노드 데이터 삭제 | `/api/storage/{Id}` | [cite_start]DELETE | files_node id를 통해 삭제 [cite: 14] |
| 데이터 이름 변경 | `/api/storage/{Id}/rename` | [cite_start]PATCH | [cite: 14] |
| 파일 이동 | `/api/storage/{id}/move` | [cite_start]PATCH | [cite: 14] |
| 파일 다운로드 URL 생성 | `/api/storage/{id}/download` | [cite_start]GET | [cite: 14] |
| 팀 저장공간 사용량 조회 | `/api/storage/usage` | [cite_start]GET | [cite: 14] |
