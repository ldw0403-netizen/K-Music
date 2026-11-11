# K-Music

Bugs · Melon · Genie 국내 음원 확장 패키지 (Mornye / SpotiFLAC)

**Author: [ldw0403-netizen](https://github.com/ldw0403-netizen)**

Korean music providers (Bugs, Melon, Genie) — metadata, charts, and URL imports with multi-source track matching.

## 설치

앱의 확장 설정에 아래 레지스트리 URL을 등록하면 3개 확장이 함께 설치·업데이트됩니다. (최소 앱 버전 3.0.1)

```
https://raw.githubusercontent.com/ldw0403-netizen/K-Music/main/registry.json
```

저장소의 `.spotiflac-ext` 파일을 직접 가져와 설치할 수도 있습니다.

## 구성

| 확장 | 주요 내용 |
| --- | --- |
| bugs-music | TOP100, 전 장르 차트, Music PD 앨범, 트랙·앨범·아티스트 상세, URL 가져오기 |
| melon-music | TOP100/HOT100/연령별 차트, 최신 곡·앨범, 장르 목록, DJ 플레이리스트, URL 가져오기 |
| genie-music | 기간별 TOP200, 장르 차트, DJ 플레이리스트, 아티스트 카탈로그, URL 가져오기 |

세 확장 공통: 멀티소스 ISRC 매칭(Deezer·Spotify·MusicBrainz·iTunes·YouTube Music), 한글 로마자 폴백, 260+ 아티스트 별칭표, iTunes 한글-라틴 브릿징, 확인된 `deezer_id`/`spotify_id` 직접 전달, 레이트리밋 페이싱과 일시 실패 재시도(90초 백그라운드 재대기열), 합성/콜라보 긴 제목 등록 인식, 변주 제목(인스트루멘탈/케라오케) 후보 강등.

## 버전 히스토리

- **2.2.9** (2026-11-09) — iTunes KR 스토어프론트 폴백: KR storefront의 `entity=song` 검색이 0건이면 entity 파라미터 없이 재시도하고 뮤직비디오 레코드는 필터링. 제목 등록 추가: 노스텔지아 ↔ Nostalgia (BIG Naughty), 첫 만남은 계획대로 되지 않아 ↔ Plot Twist (TWS).
- **2.2.8** (2026-11-08) — 번역 등록곡 회수: 한글 원제가 아닌 영문 번역 제목으로 등록된 곡의 매칭 실패 뿌리 제거, 번역 제목 별칭 쿼리를 Spotify 쿼리 예산 앞으로 이동, 영원은 그럴듯 ↔ Forever Has Always Been (Redoor) 등록.
- **2.2.7** (2026-11-08) — 무변동 재검증 빌드: 코드 변경 없이 클린 리런으로 고정 실패 코어 확정.
- **2.2.6** (2026-11-08) — 실패곡 회수 패치: 원제가 후보 제목에 완전히 포함되는 합본·콜라보 표기(예: Narr. 포함 제목) 등록 인식 + 재생시간 매칭 창 완화.
- **2.2.4** (2026-11-08) — 애플뮤직 트랙 식별자(`apple_music_id`) 송달 준비 버전(기본 꺼짐 스위치, 앱 수용 전).
- **2.2.2** (2026-11-07) — 100곡 일괄 처리 구조 개선: 레이트리밋 페이싱, 일시 실패 재시도, 백그라운드 재대기열 도입.

## 공식 스토어 등록

본 확장은 Mornye 공식 확장 저장소([mornyeapp/Mornye-Extension](https://github.com/mornyeapp/Mornye-Extension))에 심사를 거쳐 등록되어 있습니다(등록본 2.0.x, 회귀테스트 114건 통과). 공식 등록본은 심사 정책에 따라 자동 크로스서비스 ISRC 검색이 제외된 재구성 버전이며, 이 저장소가 최신 빌드(2.2.x)를 배포합니다.

---

© 2026 ldw0403-netizen
