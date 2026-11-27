# 서울튼튼플란트치과 홈페이지 (초안)

한 페이지짜리 정적 사이트입니다. `index.html`을 브라우저로 열면 됩니다.

- 이미지는 `img/`에 있습니다. 둘러보기 사진은 지금 인테리어 투시도입니다.
- 진료과목 이미지는 `img/care/`(페이지용 1200x800)입니다. 원본은 두 세트가 있습니다: `img/care-src-white/`(흰 배경, 지금 쓰는 세트)와 `img/care-src/`(베이지 배경, 이전 세트).
- 진료과목은 11개입니다: 임플란트(implant), 보철 치료(prosthetic), 틀니(denture), 충치·신경치료(endo), 자연치아 살리기(save), 잇몸 치료(gum), 사랑니 발치(wisdom), 턱관절 질환(tmj), 치아미백(whitening), 라미네이트(laminate), 검진·예방(checkup). 괄호 안이 이미지 파일 이름이고, 과목마다 `img/care/<이름>.jpg` 한 장을 씁니다. 뒤에 추가한 네 과목(save, tmj, whitening, laminate)은 흰 배경 원본만 있습니다.
- 화면에 점선 테두리로 표시된 항목(대중교통 안내, 사업자등록번호)은 확정 후 교체해야 합니다. 전화번호는 대표번호 033-436-2875로 넣었습니다.

## 주소와 배포

- 공개 주소는 `https://seoultuntun.co.kr`입니다(가비아에서 2026-11-27 등록, 1년).
- Cloudflare Pages가 이 `dental-homepage/` 폴더를 그대로 내보냅니다(hoohoocc.com과 같은 방식). 빌드 과정은 없습니다.
- `_headers`는 Cloudflare Pages 설정 파일입니다. 임시 주소(`*.pages.dev`)가 검색에 잡히지 않게 막습니다.

## 오시는 길 지도

- `index.html` 맨 아래에 카카오맵 '지도 퍼가기' 코드가 들어 있습니다. 웹에 올린 페이지에서 지도가 뜨고, 불러오지 못하면 지도 자리에 안내 문구가 남습니다.
- 지도 표시 이름은 '서울튼튼플란트치과', 위치는 홍천로8길 4입니다. 카카오맵에 치과가 장소로 등록되면 그 장소 화면의 공유 > HTML 태그 복사로 코드를 다시 만들어 `timestamp`와 `key` 값을 바꾸면 됩니다.
- 주차 안내는 건물 바로 옆 홍천전통시장 공영주차장(홍천로 371)입니다. 공영주차장과 제휴가 정해지면 주차 문구(오시는 길, 자주 묻는 질문, `llms.txt`)에 내용을 더하세요.

## 검색·AI 검색 설정

들어 있는 것:
- `index.html`의 제목, 설명, 대표 주소(canonical), 공유 미리보기(Open Graph), 지역 태그
- 구조화 데이터(JSON-LD): 치과(Dentist), 대표원장(Person), 사이트(WebSite), 자주 묻는 질문(FAQPage)
- `robots.txt`, `sitemap.xml`, `llms.txt`(AI 검색용 요약), `favicon.svg`, `img/og.jpg`(공유 이미지)

끝난 일(2026-11-27):
- `index.html`, `robots.txt`, `sitemap.xml`, `llms.txt`의 주소를 `https://seoultuntun.co.kr`로 바꿨습니다.
- 화면 3곳과 `llms.txt`에 대표 전화 033-436-2875를 넣고, JSON-LD의 치과 항목에 `"telephone"`을 추가했습니다.

남은 일:
1. 네이버 서치어드바이저와 구글 서치 콘솔에 사이트 등록 후, `index.html` 머리 부분의 소유 확인 태그 주석을 풀고 값 넣기. 두 곳 모두에 `sitemap.xml` 제출
2. 네이버 스마트플레이스와 구글 비즈니스 프로필에 치과 등록. 이름, 주소, 전화, 진료시간을 홈페이지와 똑같이 적기
