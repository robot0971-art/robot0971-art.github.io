# Unity 게임 개발자 포트폴리오

GitHub Pages로 배포할 수 있는 정적 포트폴리오 사이트입니다. Unity/C# 게임 프로젝트를 정리하고, 프로젝트별 상세 페이지와 스크린샷을 함께 보여주는 구조입니다.

## 폴더 구조

```text
robot0971-art.github.io/
├── index.html
├── css/
│   └── style.css
├── js/
│   └── main.js
├── images/
│   └── projects/
│       └── placeholder.svg
├── projects/
│   ├── project-template.html
│   └── sunnyside-island.html
├── .editorconfig
└── README.md
```

## 프로젝트 추가 방법

1. `images/projects/` 폴더에 프로젝트 이미지를 추가합니다.
   - 권장 크기: 1280x720 또는 1920x1080
   - 권장 형식: PNG, JPG, WEBP
   - 파일명 예시: `tower-defense-main.png`, `tower-defense-gameplay.png`

2. `projects/project-template.html` 파일을 복사합니다.
   - 예: `projects/my-new-game.html`
   - 프로젝트 이름, 기간, 설명, 기능, 기술 스택, 링크를 수정합니다.

3. `index.html`의 `<div class="projects-grid">` 안에 프로젝트 카드를 추가합니다.

```html
<div class="project-card fade-in" data-category="unity">
    <div class="project-image">
        <img src="images/projects/my-new-game-main.png" alt="My New Game">
        <div class="project-overlay">
            <a href="projects/my-new-game.html" class="btn btn-small">상세보기</a>
        </div>
    </div>
    <div class="project-info">
        <h3>My New Game</h3>
        <p>프로젝트를 한두 문장으로 소개합니다.</p>
        <div class="project-tags">
            <span class="tag">Unity</span>
            <span class="tag">C#</span>
        </div>
    </div>
</div>
```

## 개인 정보 수정 위치

`index.html`에서 아래 영역을 수정하면 됩니다.

- Hero: 첫 화면 제목, 한 줄 소개, 설명
- About: 자기소개 문단
- Skills: 기술 이름과 숙련도 `data-progress`
- Projects: 프로젝트 카드 목록
- Contact: 이메일, GitHub 주소

## 인코딩 안내

이 저장소의 모든 텍스트 파일은 UTF-8로 저장합니다.

- HTML 파일에는 `<meta charset="UTF-8">`가 들어 있습니다.
- `.editorconfig`에 `charset = utf-8`을 추가해 두었습니다.
- VS Code를 쓴다면 오른쪽 아래 인코딩 표시가 `UTF-8`인지 확인하세요.
- 파일을 열었을 때 한글이 깨져 보이면 저장하지 말고, `Reopen with Encoding`에서 UTF-8로 다시 열어야 합니다.
- Windows 메모장이나 오래된 편집기에서 저장할 때는 인코딩을 UTF-8로 선택하세요.

## GitHub Pages 배포

저장소 이름이 `username.github.io` 형식이면 `main` 브랜치에 푸시한 뒤 GitHub Pages에서 바로 배포할 수 있습니다.

일반 저장소라면 GitHub에서 다음 순서로 설정합니다.

1. Settings
2. Pages
3. Source를 `Deploy from a branch`로 선택
4. Branch를 `main` / `/root`로 선택
5. Save

배포 후 몇 분 뒤 사이트 주소에서 확인할 수 있습니다.
