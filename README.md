# CastSurf Receiver

CastSurf iOS 앱의 커스텀 Google Cast 수신기.

## 역할
- 기본 미디어 재생 (웹 영상 추출·파일 캐스팅) — CAF 기본 플레이어 사용
- 사진 슬라이드쇼 — 두 장을 겹쳐 CSS 크로스페이드로 전환 (기본 리시버의 검은 화면 문제 해결)
- 커스텀 채널: `urn:x-cast:com.castwave`

## 배포
GitHub Pages(main 브랜치 루트)로 서빙된다:
`https://ybeeen.github.io/castwave-receiver/`

## Cast 개발자 콘솔 등록
1. https://cast.google.com/publish 에서 Custom Receiver 추가
2. Receiver URL에 위 Pages 주소 입력 → 발급되는 **Application ID**를 앱에 설정
3. **Publish** — 공개 전에는 콘솔에 일련번호를 등록한 기기에서만 실행된다.
   미등록 기기는 앱의 검색 목록에조차 뜨지 않는다(디스커버리가 App ID로 걸러지기 때문).
   Publish하면 시리얼 등록 없이 모든 기기에서 동작하며, Pages URL은 그대로라 내용은 계속 고칠 수 있다.

## 참고
- 이 동글은 WebRTC 수신을 지원하지 않아, 저지연 미러링은 WebSocket 프레임 방식으로 별도 검토한다.
- 비밀값(쿠폰 시크릿 등)은 이 공개 저장소에 두지 않는다.
