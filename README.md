# CastWave Receiver

CastWave iOS 앱의 커스텀 Google Cast 수신기.

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
3. 테스트 기기(Chromecast) 시리얼 등록

## 참고
- 이 동글은 WebRTC 수신을 지원하지 않아, 저지연 미러링은 WebSocket 프레임 방식으로 별도 검토한다.
- 비밀값(쿠폰 시크릿 등)은 이 공개 저장소에 두지 않는다.
