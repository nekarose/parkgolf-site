# 지금, 파크골프 — 공개 사이트

앱 **지금, 파크골프**가 읽는 공개 파일을 두는 저장소입니다.

| 파일 | 용도 |
|---|---|
| `app_version_config.json` | 새 버전 안내와 원격 조절값. 앱이 켤 때마다 raw 주소로 읽습니다 |
| `privacy/` · `privacy/en/` | 개인정보 처리방침 (스토어 등록·앱 설정 화면 링크) |
| `support/` · `support/en/` | 고객지원 (스토어 등록·앱 설정 화면 링크) |

앱이 읽는 주소:

    https://raw.githubusercontent.com/nekarose/parkgolf-site/main/app_version_config.json

- 이 파일을 고치고 푸시하면 **새 빌드 없이** 반영됩니다(원본 주소 캐시 몇 분).
- 형식이 깨지거나 파일이 없어도 앱은 조용히 넘어갑니다. 그래도 푸시 전에 `python3 -m json.tool app_version_config.json` 로 확인합니다.
- 열쇠와 운영 규칙은 앱 저장소의 `docs/store/UPDATE-CONFIG.md` 에 있습니다.
- 커밋 메시지에 **무엇을 왜** 바꿨는지 적습니다(예: `안내: 0.2.0+3 — 양 스토어 노출 확인`). 이 저장소의 git log 가 운영 이력입니다.

페이지 주소(GitHub Pages):

- https://nekarose.github.io/parkgolf-site/privacy/
- https://nekarose.github.io/parkgolf-site/support/

**개인정보 처리방침은 앱이 실제로 하는 일과 같아야 합니다.** 앱에 새 SDK·권한·전송이 생기면
(분석 도구, 로그인, 서버 저장 등) 출시 전에 이 페이지부터 고치고 시행일을 바꿉니다.
