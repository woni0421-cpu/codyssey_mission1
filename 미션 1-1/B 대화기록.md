# 🎬 영화 티어리스트 웹페이지 기획 및 구현 대화 기록

## 👤 사용자 (기획서 전달 및 구현 요청)

**영화 티어리스트 웹페이지 기획서**를 바탕으로 HTML, CSS, JavaScript가 모두 들어있는 HTML 파일 하나를 만들어줘. 외부 파일이나 서버 없이 브라우저에서 바로 열리게 하고, 화면 문구는 한국어로 써줘. 완성된 .html파일로 제공해줘.

### [기획서 요약]
1. **누가 쓰나**: 영화 평가를 기록하고 티어리스트를 공유하고 싶은 불특정 다수 (소셜 로그인 사용)
2. **무엇을 하려고**: 본 영화 기록, 별점/한줄평 남기기, 별점에 따른 자동 티어 분류, 장르 기반 추천 등
3. **화면과 동작**: 
   - 메인 화면 (내 티어리스트)
   - 소셜 로그인
   - 영화 검색 (TMDB API 활용)
   - 별점 입력 (5점 만점, 0.5점 단위)
   - 티어 자동 분류 (1점 단위 내림 처리, 5점=S ~ 0점대=E)
   - 공개/비공개, 팔로우, 공유, 추천 기능
4. **완성 기준**: API 없이 동작하는 프로토타입 형태의 단일 HTML 구현

---

## 🤖 AI 튜터 (HTML 코드 구현 및 제공)

요청하신 기획서를 바탕으로 **단일 HTML 파일(HTML + CSS + JavaScript)**을 작성했습니다. 

외부 서버나 API 키 없이 브라우저에서 바로 동작하도록 **TMDB API 검색 결과와 소셜 로그인은 가상의 데이터(Mock Data)로 구현**했습니다. 코드를 복사하여 `index.html`로 저장한 뒤, 크롬 등의 브라우저에서 열면 바로 실행됩니다.

### 💻 구현된 코드 (`index.html`)

```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>내 영화 티어리스트</title>
    <style>
        /* CSS 스타일 생략 (실제 파일에는 전체 CSS 포함) */
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="logo">MovieTier</div>
        <div class="header-controls">
            <input type="text" id="searchInput" placeholder="영화 검색 (예: 인셉션)">
            <button id="searchBtn">검색</button>
            
            <div id="userMenu" class="hidden">
                <label style="font-size: 12px; margin-right: 10px;">
                    <input type="checkbox" id="privacyToggle"> 비공개
                </label>
                <button class="btn-secondary" onclick="alert('티어리스트 링크가 클립보드에 복사되었습니다!')">공유</button>
                <button class="btn-secondary" onclick="alert('팔로우 기능은 준비 중입니다.')">팔로우</button>
                <button id="logoutBtn" class="btn-secondary">로그아웃</button>
            </div>
            <button id="loginBtn">소셜 로그인</button>
        </div>
    </header>

    <!-- Tier List Board -->
    <main class="tier-board">
        <!-- S ~ E 티어 UI 생략 -->
    </main>

    <!-- Recommendations -->
    <section class="recommendations hidden" id="recSection">
        <h2>취향 저격 추천 영화</h2>
        <div class="rec-list" id="recList"></div>
    </section>

    <!-- Modals (Search & Rating) 생략 -->

    <script>
        // 가상 데이터 및 핵심 로직 (검색, 별점 평가, 티어 자동 분류, 추천 등)
        // JavaScript 코드 생략 (실제 파일에는 전체 JS 포함)
    </script>
</body>
</html>