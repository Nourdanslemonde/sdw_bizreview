# sdw_bizreview

26년 상반기 비즈니스 리뷰 대시보드 (암호화 배포).

- `index.html` — 전체 내용이 AES-256-GCM으로 암호화된 단일 페이지. 비밀번호를 입력해야 대시보드가 열린다.
- 소스에는 암호문만 노출되므로 공개 호스팅(GitHub Pages)에 올려도 데이터가 드러나지 않는다.
- 복호화는 브라우저에서 WebCrypto(PBKDF2-SHA256 600k + AES-GCM)로 수행. 서버·외부요청 없음.

비밀번호를 잊으면 복구 불가. 재빌드·재암호화 도구는 워크스페이스
`10-projects/24-biz-review-마감틀/scripts/encrypt_dashboard.py`.
