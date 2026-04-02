# 📚 포트폴리오 사이트 정보 추가 설명서

이 문서는 포트폴리오 사이트에 새로운 프로젝트, 이미지, 정보를 추가하는 방법을 안내합니다.

---

## 📁 폴더 구조

```
Second_Portfolio/
├── index.html                 # 메인 페이지
├── css/
│   └── style.css             # 스타일시트 (색상, 레이아웃 등)
├── js/
│   └── main.js               # 자바스크립트 (애니메이션, 인터랙션)
├── images/
│   └── projects/             # 프로젝트 이미지를 이 폴더에 추가
│       └── placeholder.svg   # 기본 플레이스홀더 이미지
├── projects/
│   ├── project-template.html # 새 프로젝트 작성용 템플릿
│   └── sample-tower-defense.html # 샘플 프로젝트
└── README.md                 # 이 파일
```

---

## 🎮 새 프로젝트 추가하기

### 1단계: 프로젝트 이미지 준비

1. `images/projects/` 폴더에 이미지를 추가합니다.
2. **권장 이미지 크기**:
   - 메인 이미지: 1920x1080 또는 1280x720
   - 스크린샷: 800x600 또는 640x480
3. **권장 파일 형식**: PNG, JPG, WEBP (GIF도 가능)
4. **파일명 규칙**: 프로젝트명-기능.png
   ```
   예: tower-defense-main.png
       tower-defense-gameplay.png
       tower-defense-ui.png
   ```

### 2단계: 프로젝트 상세 페이지 만들기

1. `projects/project-template.html` 파일을 복사합니다.
2. 새 파일명으로 저장합니다 (예: `my-new-game.html`).
3. 파일 내용을 수정합니다:

```html
<!-- 수정할 부분들 -->

<title>프로젝트 이름 - Portfolio</title>

<h1>프로젝트 이름</h1>

<div class="project-meta">
    <span><i class="far fa-calendar"></i> 2026-01-01 ~ 2026-01-31</span>
    <span><i class="fas fa-user"></i> 개인 프로젝트</span>
    <span><i class="fas fa-code-branch"></i> Unity, C#</span>
</div>

<!-- 이미지 경로 수정 -->
<img src="../images/projects/tower-defense-main.png" alt="Project Main Image" class="main-image">
<div class="image-gallery">
    <img src="../images/projects/tower-defense-1.png" alt="Screenshot 1">
    <img src="../images/projects/tower-defense-2.png" alt="Screenshot 2">
    <img src="../images/projects/tower-defense-3.png" alt="Screenshot 3">
</div>

<!-- 내용 수정 -->
<h2>프로젝트 소개</h2>
<p>프로젝트 설명을 여기에 작성하세요.</p>

<!-- 기술 스택 수정 -->
<div class="tech-stack">
    <span class="tag">Unity</span>
    <span class="tag">C#</span>
    <span class="tag">추가기술</span>
</div>

<!-- 링크 수정 -->
<a href="https://github.com/username/repo" class="btn btn-primary" target="_blank">
    <i class="fab fa-github"></i> GitHub 저장소
</a>
```

### 3단계: 메인 페이지에 프로젝트 카드 추가

`index.html` 파일의 `<div class="projects-grid">` 섹션에 새 프로젝트 카드를 추가합니다:

```html
<!-- 새 프로젝트 카드 추가 -->
<div class="project-card fade-in" data-category="unity">
    <div class="project-image">
        <img src="images/projects/프로젝트메인이미지.png" alt="프로젝트명">
        <div class="project-overlay">
            <a href="projects/프로젝트파일명.html" class="btn btn-small">상세보기</a>
        </div>
    </div>
    <div class="project-info">
        <h3>프로젝트 이름</h3>
        <p>프로젝트에 대한 간단한 설명 (한 줄)</p>
        <div class="project-tags">
            <span class="tag">Unity</span>
            <span class="tag">C#</span>
        </div>
    </div>
</div>
```

**data-category 옵션**:
- `unity`: Unity 프로젝트
- `web`: 웹 프로젝트
- `tool`: 툴/유틸리티
- `all`: 모든 카테고리

---

## 👤 개인 정보 수정하기

### 메인 페이지 (`index.html`)

#### 1. Hero 섹션 수정
```html
<h1 class="hero-title">Unity Game Developer</h1>
<p class="hero-subtitle">C#과 Unity로 게임을 만듭니다</p>
<p class="hero-description">게임 개발에 열정을 가진 개발자입니다...</p>
```

#### 2. About 섹션 수정
```html
<div class="about-text">
    <h3>안녕하세요!</h3>
    <p>자기소개를 작성하세요.</p>
</div>
```

#### 3. 통계 수치 수정
```html
<!-- data-target에 원하는 숫자 입력 -->
<p class="stat-number" data-target="10">0</p>
```
그리고 `js/main.js`에서도 초기값을 수정할 수 있습니다.

#### 4. Skills 섹션 수정
```html
<div class="skill-card fade-in">
    <div class="skill-icon">
        <i class="fab fa-unity"></i>
    </div>
    <h3>Unity</h3>
    <div class="skill-bar">
        <!-- data-progress에 0~100 사이 값 입력 -->
        <div class="skill-progress" data-progress="85"></div>
    </div>
</div>
```

#### 5. Contact 섹션 수정
```html
<div class="contact-item">
    <i class="fas fa-envelope"></i>
    <div>
        <h4>Email</h4>
        <p>your.email@example.com</p>
    </div>
</div>
<div class="contact-item">
    <i class="fab fa-github"></i>
    <div>
        <h4>GitHub</h4>
        <p><a href="https://github.com/yourusername" target="_blank">github.com/yourusername</a></p>
    </div>
</div>
```

---

## 🎨 색상 및 스타일 수정하기

### 색상 변경 (`css/style.css`)

`style.css` 파일 상단의 `:root` 섹션에서 색상을 변경할 수 있습니다:

```css
:root {
    --pastel-yellow: #FFF9C4;   /* 파스텔 노랑 */
    --pastel-pink: #F8BBD0;      /* 파스텔 분홍 */
    --pastel-purple: #E1BEE7;   /* 파스텔 보라 */
    --pastel-blue: #BBDEFB;     /* 파스텔 블루 (추가 가능) */
    --text-dark: #333333;        /* 어두운 텍스트 */
    --text-light: #666666;       /* 밝은 텍스트 */
}
```

**파스텔 색상 추천**:
- 연한 민트: `#B2DFDB`
- 연한 복숭아: `#FFCCBC`
- 연한 라벤더: `#D1C4E9`
- 연한 하늘: `#B3E5FC`
- 연한 라임: `#F0F4C3`

### 폰트 변경

Google Fonts에서 원하는 폰트를 선택하고 `<head>` 태그의 링크를 변경합니다:

```html
<link href="https://fonts.googleapis.com/css2?family=원하는폰트&display=swap" rel="stylesheet">
```

그리고 `style.css`에서:
```css
body {
    font-family: '원하는폰트', sans-serif;
}
```

---

## 📸 이미지 추가 가이드

### 이미지 최적화

1. **파일 크기 줄이기**
   - 온라인 도구 사용: [TinyPNG](https://tinypng.com/), [Squoosh](https://squoosh.app/)
   - 권장 크기: 메인 이미지 500KB 이하

2. **이미지 포맷 선택**
   - **PNG**: 스크린샷, UI (선명함)
   - **JPG**: 게임 플레이 장면 (작은 파일 크기)
   - **WEBP**: 최신 포맷 (작은 크기 + 고품질)
   - **GIF**: 움직이는 이미지 (게임플레이 GIF)

3. **이미지 크기 권장사항**
   - 메인 이미지: 1920x1080 (16:9 비율)
   - 스크린샷: 800x600
   - 썸네일: 400x300

### GIF 만들기

게임플레이 GIF를 만들려면:

1. **Unity Recorder** (Unity 패키지)
   - Window > General > Recorder
   - GIF 형식으로 녹화

2. **ScreenToGif** (무료 도구)
   - 다운로드: https://www.screentogif.com/
   - 화면 녹화 후 GIF로 저장

3. **OBS Studio + 변환**
   - 동영상 녹화 후 [ezgif.com](https://ezgif.com/video-to-gif)에서 변환

---

## 🚀 GitHub Pages에 배포하기

### 1. GitHub 저장소 생성

1. GitHub에서 새 저장소 생성
2. 저장소 이름: `username.github.io` (또는 원하는 이름)

### 2. 파일 업로드

```bash
# Git 초기화
git init

# 파일 추가
git add .

# 커밋
git commit -m "Initial commit: Portfolio website"

# GitHub 원격 저장소 연결
git remote add origin https://github.com/username/username.github.io.git

# 푸시
git push -u origin main
```

### 3. GitHub Pages 활성화

1. GitHub 저장소 > Settings > Pages
2. Source: `main` 브랜치 선택
3. Save 클릭
4. 몇 분 후 `https://username.github.io`에서 접속 가능

### 4. 업데이트 방법

```bash
# 파일 수정 후
git add .
git commit -m "Update: 새 프로젝트 추가"
git push
```

---

## 💡 유용한 팁

### 프로필 사진 추가

`images/` 폴더에 `profile.jpg`를 넣고, `index.html`의 Hero 섹션에 추가:

```html
<div class="hero-content">
    <img src="images/profile.jpg" alt="Profile" class="profile-image">
    <div class="hero-text">
        <h1 class="hero-title">Unity Game Developer</h1>
        ...
    </div>
</div>
```

`style.css`에 추가:
```css
.profile-image {
    width: 150px;
    height: 150px;
    border-radius: 50%;
    object-fit: cover;
    margin-bottom: 1rem;
    border: 4px solid white;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}
```

### 연락처 폼 활성화

무료 폼 서비스 사용:

1. **Formspree** (https://formspree.io/)
   - 가입 후 폼 엔드포인트 받기
   - `index.html` 수정:
   ```html
   <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```

2. **EmailJS** (https://www.emailjs.com/)
   - 자세한 내용은 EmailJS 문서 참조

### 애니메이션 추가 효과

새로운 애니메이션을 추가하려면 `css/style.css`에:

```css
@keyframes 새로운애니메이션 {
    from { opacity: 0; transform: scale(0.9); }
    to { opacity: 1; transform: scale(1); }
}

.적용할클래스 {
    animation: 새로운애니메이션 0.5s ease;
}
```

### 반응형 디자인 확인

다양한 화면 크기에서 테스트:
- 브라우저 개발자 도구 (F12) > Toggle Device Toolbar
- 모바일, 태블릿, 데스크톱 크기 확인

---

## 📞 도움이 필요할 때

### 자주 묻는 질문

**Q: 이미지가 안 보여요**
- 파일 경로가 올바른지 확인
- 이미지 파일명에 공백이나 한글이 있는지 확인 (영문 권장)
- 브라우저 캐시 삭제 (Ctrl+F5)

**Q: 애니메이션이 작동하지 않아요**
- `js/main.js` 파일이 올바르게 연결되었는지 확인
- 브라우저 콘솔에서 에러 확인 (F12 > Console)

**Q: 모바일에서 레이아웃이 깨져요**
- `style.css`의 `@media` 쿼리 확인
- 뷰포트 메타 태그 확인

**Q: GitHub Pages에 배포했는데 안 보여요**
- Settings > Pages에서 Source가 올바른 브랜치인지 확인
- 파일명이 `index.html`인지 확인
- 최대 10분 대기 (GitHub 배포 시간)

---

## ✅ 체크리스트

새 프로젝트 추가 시:

- [ ] `images/projects/` 폴더에 이미지 추가
- [ ] `projects/` 폴더에 HTML 파일 생성
- [ ] `index.html`에 프로젝트 카드 추가
- [ ] 모든 링크가 올바르게 작동하는지 확인
- [ ] 이미지가 제대로 표시되는지 확인
- [ ] 모바일에서도 잘 보이는지 확인
- [ ] GitHub에 커밋 및 푸시

---

마지막 업데이트: 2026-04-02