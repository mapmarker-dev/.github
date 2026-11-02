# HANDOFF

> 최종 갱신: 2026-11-02 · 브랜치: main

## 지금 하는 일

1-1단계(서버 기본)를 진행한다. 서버 단위 "자체 JWT 인증 + Trip/Stop/Segment CRUD"를 서버 `main`에 병합했다(PLAN 1-1의 JWT·CRUD·여행 상태 체크). 1-1에 남은 것은 카카오·네이버 로그인이다. 서버 진행은 `../mapmarker-server/HANDOFF.md`를 본다.

## 다음에 할 첫 단계

다음 서버 단위는 소셜 로그인이고, 네이버·카카오 앱 등록(0단계)이 먼저다.

- 조직 소개(`profile/README.md`)의 진행 상황을 서버 API 완료에 맞게 고쳤다.

0단계에 남은 것은 소셜 로그인 앱 등록과 AWS 계정이다. 앱 쪽 진행은 `../mapmarker-app/HANDOFF.md`를 본다.

## 결론이 안 난 논의

- 다른 저장소의 CI
  - `.github`(문서뿐)와 `mapmarker-web`(정적 페이지)은 지금은 CI가 필요 없다고 봤다.
  - 앱 CI(`flutter analyze`, `flutter test`)는 사용자가 원한다. 서버가 좀 개발된 뒤에 하고, 시작할 때 PLAN에 항목을 넣는다.
  - 앱 CI에서 정할 것: Flutter 버전 고정 방법(고정 파일 없음, 로컬 3.47.7), Android 빌드 포함 여부(한 번에 5분 이상), 앱 `main` 브랜치 보호.
