# 📅 스케줄 플래너 — PWA 설치 가이드

## 파일 목록
```
scheduler.html   ← 앱 본체
manifest.json    ← PWA 설정
sw.js            ← 오프라인 캐시 (Service Worker)
icon-192.png     ← 앱 아이콘 (소)
icon-512.png     ← 앱 아이콘 (대)
```

---

## ✅ 가장 빠른 방법 — GitHub Pages로 무료 배포 (5분)

### 1단계 — GitHub 계정 만들기
https://github.com 에서 무료 가입

### 2단계 — 새 저장소(repository) 만들기
1. 우상단 `+` → `New repository`
2. Repository name: `planner` (아무 이름이나 OK)
3. **Public** 선택
4. `Create repository` 클릭

### 3단계 — 파일 올리기
1. 저장소 페이지에서 `Add file` → `Upload files`
2. 아래 5개 파일을 모두 끌어다 놓기
   - `scheduler.html`
   - `manifest.json`
   - `sw.js`
   - `icon-192.png`
   - `icon-512.png`
3. `Commit changes` 클릭

### 4단계 — GitHub Pages 켜기
1. 저장소 → `Settings` → 왼쪽 메뉴 `Pages`
2. Source: `Deploy from a branch`
3. Branch: `main` / `/ (root)` 선택 → `Save`
4. 1~2분 후 주소 생성: `https://[내아이디].github.io/planner/`

### 5단계 — 앱 설치
접속 후 브라우저가 "홈 화면에 추가" 배너를 자동으로 띄워줘요.

| 기기 | 설치 방법 |
|------|-----------|
| **안드로이드 (크롬)** | 화면 하단 배너 → "설치" 탭 |
| **아이폰 (사파리)** | 하단 공유버튼 → "홈 화면에 추가" |
| **PC 크롬** | 주소창 오른쪽 설치 아이콘 (⊕) 클릭 |
| **PC 엣지** | 주소창 오른쪽 앱 설치 아이콘 클릭 |

---

## 데이터 저장 위치
- 모든 데이터는 **브라우저 로컬 스토리지**에 저장돼요
- 같은 브라우저·기기에서는 데이터 유지
- 기기를 바꾸면 데이터가 없어요 (동기화 미지원)
- 브라우저 캐시를 지우면 데이터도 삭제될 수 있으니 **중요한 데이터는 메모로 백업** 해두세요

---

## 오프라인 사용
Service Worker가 앱을 캐시해뒤서 **인터넷 없이도** 앱이 실행돼요.
단, 첫 방문은 인터넷 연결이 필요해요.
