# EZGHBlog

EZGHBlog는 GitHub Pages와 Jekyll 블로그의 글 작성, 수정, 미리보기, 빌드 확인 및 GitHub 게시 과정을 한 화면에서 관리하는 데스크톱 도구입니다.

Windows에서는 WebView2, macOS에서는 WKWebView를 사용하며 컨트롤 화면과 에디터, 블로그 미리보기를 앱 내부 탭으로 제공합니다.

## 다운로드

[최신 릴리스에서 운영체제에 맞는 설치 파일을 다운로드하세요.](https://github.com/Bakcoding/EZGHBlog/releases/latest)

- Windows: `EZGHBlogSetup.exe`
- macOS: `EZGHBlog-mac.dmg`
- 무결성 확인: `SHA256SUMS.txt`

## 시스템 요구사항

EZGHBlog는 블로그 프로젝트의 기존 Ruby/Jekyll 환경을 이용합니다. 다음 도구가 필요합니다.

- Windows 10/11 x64 또는 macOS 12 이상
- Ruby와 Bundler
- Git
- GitHub CLI (`gh`)
- 관리할 Jekyll 블로그의 Gem 의존성
- Windows의 Microsoft Edge WebView2 Runtime

GitHub에 게시하려면 GitHub CLI 로그인이 필요합니다.

```bash
gh auth login
```

블로그 저장소에서는 먼저 의존성을 설치하세요.

```bash
bundle install
```

## 설치

### Windows

1. `EZGHBlogSetup.exe`를 실행합니다.
2. 설치가 끝나면 시작 메뉴 또는 바탕화면의 EZGHBlog를 실행합니다.
3. 처음 실행할 때 관리할 Jekyll 블로그 폴더를 선택합니다.

### macOS

1. `EZGHBlog-mac.dmg`를 엽니다.
2. `EZGHBlog.app`을 Applications 폴더로 드래그합니다.
3. 앱을 실행하고 관리할 Jekyll 블로그 폴더를 선택합니다.

현재 초기 릴리스는 Apple Developer ID 서명과 notarization이 적용되지 않았습니다. macOS에서 실행을 차단하면 시스템 설정의 개인정보 보호 및 보안 화면에서 앱 열기를 허용해야 할 수 있습니다.

## 주요 기능

- 신규 글 작성 및 기존 글 수정·삭제
- 카테고리와 템플릿 기반 글 생성
- Markdown 실시간 미리보기
- Jekyll 블로그 미리보기와 빌드 확인
- Git 변경사항 확인
- 커밋 메시지 작성, 커밋 및 GitHub push
- 컨트롤·에디터·미리보기 통합 탭

## 체크섬 확인

Windows PowerShell:

```powershell
Get-FileHash .\EZGHBlogSetup.exe -Algorithm SHA256
```

macOS:

```bash
shasum -a 256 EZGHBlog-mac.dmg
```

계산된 값이 릴리스에 첨부된 `SHA256SUMS.txt`의 값과 일치하는지 확인하세요.

## 문제 제보

오류가 발생하면 운영체제, EZGHBlog 버전, Ruby 버전과 재현 절차를 포함해 [Issues](https://github.com/Bakcoding/EZGHBlog/issues)에 등록해 주세요.
