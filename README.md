# Mardocle 웹사이트

Mardocle의 제품 소개와 공식 다운로드 안내를 제공하는 정적 웹사이트입니다.

- 운영 예정 주소: `https://mardocle.pages.dev`
- 앱 저장소: <https://github.com/dpnzdy/mardocle>
- 배포: Cloudflare Pages
- 현재 직접 다운로드: <https://mardocle.pages.dev/downloads/MardocleSetup-0.1.0.exe>

## 로컬 미리보기

```powershell
python -m http.server 8000
```

이 폴더에서 명령을 실행한 뒤 <http://localhost:8000>을 엽니다.

## Cloudflare Pages 설정

| 항목 | 값 |
| --- | --- |
| 프로젝트 이름 | `mardocle` |
| Production branch | `main` |
| Build command | `exit 0` |
| Build output directory | `.` |

`_headers`는 Cloudflare Pages가 응답 보안 헤더로 사용합니다. `downloads/`에는 버전별 Windows 설치 파일을 두고, 기존 파일을 덮어쓰지 않습니다. 새 버전은 새 파일명으로 추가하고 `index.html`의 다운로드 링크·파일 크기·SHA-256 값을 함께 갱신합니다.
