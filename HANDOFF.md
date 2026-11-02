# HANDOFF

> 최종 갱신: 2026-11-02 · 브랜치: main

## 지금 하는 일

1-1단계(서버 기본)를 진행한다. 서버 단위는 "자체 JWT 인증 + Trip/Stop/Segment CRUD"를 하고 있다(소셜 로그인은 그다음). 서버 진행은 `../mapmarker-server/HANDOFF.md`를 본다.

- PLAN 1-1: JWT 인증과 여행 상태(직접 바꾼 상태를 API로 받고 돌려줌)를 체크했다. CRUD는 여행까지 됐고 장소·구간 쓰기가 남았다.

## 다음에 할 첫 단계

서버의 장소·구간 쓰기(C)를 구현한다(`../mapmarker-server/HANDOFF.md`). 끝나면 PLAN 1-1의 CRUD 항목을 체크한다.

0단계에 남은 것은 소셜 로그인 앱 등록과 AWS 계정이다. 앱 쪽 진행은 `../mapmarker-app/HANDOFF.md`를 본다.

## 결론이 안 난 논의

- 다른 저장소의 CI
  - `.github`(문서뿐)와 `mapmarker-web`(정적 페이지)은 지금은 CI가 필요 없다고 봤다.
  - 앱 CI(`flutter analyze`, `flutter test`)는 사용자가 원한다. 서버가 좀 개발된 뒤에 하고, 시작할 때 PLAN에 항목을 넣는다.
  - 앱 CI에서 정할 것: Flutter 버전 고정 방법(고정 파일 없음, 로컬 3.47.7), Android 빌드 포함 여부(한 번에 5분 이상), 앱 `main` 브랜치 보호.
