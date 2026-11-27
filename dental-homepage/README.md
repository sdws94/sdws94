# 서울튼튼플란트치과 홈페이지 (초안)

한 페이지짜리 정적 사이트입니다. `index.html`을 브라우저로 열면 됩니다.

- 이미지는 `img/`에 있습니다. 둘러보기 사진은 지금 인테리어 투시도입니다.
- 화면에 점선 테두리로 표시된 항목(전화번호, 주차 안내 등)은 확정 후 교체해야 합니다.

## 검색·AI 검색 설정

들어 있는 것:
- `index.html`의 제목, 설명, 대표 주소(canonical), 공유 미리보기(Open Graph), 지역 태그
- 구조화 데이터(JSON-LD): 치과(Dentist), 대표원장(Person), 사이트(WebSite), 자주 묻는 질문(FAQPage)
- `robots.txt`, `sitemap.xml`, `llms.txt`(AI 검색용 요약), `favicon.svg`, `img/og.jpg`(공유 이미지)

도메인을 정한 뒤 할 일:
1. `index.html`, `robots.txt`, `sitemap.xml`, `llms.txt`에서 `https://example.com`을 실제 주소로 모두 바꾸기
2. 대표 전화가 개통되면 화면의 `033-000-0000`을 바꾸고, JSON-LD의 치과 항목에 `"telephone"` 추가
3. 네이버 서치어드바이저와 구글 서치 콘솔에 사이트 등록 후, `index.html` 머리 부분의 소유 확인 태그 주석을 풀고 값 넣기. 두 곳 모두에 `sitemap.xml` 제출
4. 네이버 스마트플레이스와 구글 비즈니스 프로필에 치과 등록. 이름, 주소, 전화, 진료시간을 홈페이지와 똑같이 적기
