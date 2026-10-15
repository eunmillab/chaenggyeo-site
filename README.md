# 챙겨 사이트 (chaenggyeo.ai.kr)

정적 사이트. 빌드 없음. 이 폴더를 그대로 올리면 돼요.

- `/` 소개 (index.html)
- `/login` 로그인 관문 → Claude 아티팩트 앱 (claude.ai 로그인 + 초대가 필요)
- `/app` · `/guide` 는 아티팩트로 302
- 자체 로그인(Supabase)은 1.0 호스팅 건에서. 명세: ~/먀/작업/261015_챙겨_웹사이트/명세.md

## 로컬에서 보기
```bash
cd ~/먀 && python3 -m http.server 8921 --directory chaenggyeo-site
```

## 올리기 (mya-site 와 같음: GitHub Pages)
저장소 https://github.com/eunmillab/chaenggyeo-site · main 브랜치 루트 · CNAME = chaenggyeo.ai.kr
`git push` 하면 1~2분 뒤 반영. `/app` · `/guide` 는 meta refresh 로 아티팩트로 보냄 (Pages 는 _redirects 를 안 읽음).

DNS(가비아 · chaenggyeo.ai.kr):
- A  @  185.199.108.153 / 185.199.109.153 / 185.199.110.153 / 185.199.111.153
- CNAME  www  eunmillab.github.io
