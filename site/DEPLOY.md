# 배포 안내 — Netlify / Vercel

이 프로젝트는 정적 사이트입니다. 배포 대상 폴더는 `site/`입니다.

로컬 미리보기

```bash
python -m http.server 8000
# 브라우저에서 http://localhost:8000/site/ 확인
```

Netlify (웹에서 연결)

- GitHub에 저장소를 만들고 `site/` 폴더가 포함된 커밋을 푸시하세요.
- Netlify에 로그인 → New site → Import from Git → GitHub 선택 → 저장소 연결
- Build settings: Build command 비움, Publish directory: `site` → Deploy

Netlify (드래그 앤 드롭)

- `site/` 폴더를 ZIP으로 압축한 후 https://app.netlify.com/drop 에 드래그하면 즉시 배포됩니다.

Netlify CLI (직접 배포)

```bash
npm install -g netlify-cli
# 처음 연결 설정
netlify init
# 또는 바로 배포
netlify deploy --dir=site --prod
```

Vercel (웹에서 연결)

- GitHub에 푸시 후 Vercel에서 New Project → Import Git Repository
- Root 또는 Output Directory를 `site`로 지정(필요 시)

Vercel CLI

```bash
npm i -g vercel
vercel # 안내에 따라 프로젝트 연결, 또는
vercel --prod site
```

권장 설정 및 주의사항

- 이미지 용량이 큰 경우 썸네일을 생성해 사용하세요(성능 개선).
- 공개/비공개 설정: 이미지 공개 여부를 확인하세요.
- GitHub로 소스 관리를 권장합니다—배포 이력 및 롤백이 쉬워집니다.

문제가 있으면 제가 GitHub 레포 준비(원하시면 커밋 포함)와 Netlify 연결 가이드를 단계별로 도와드리겠습니다.
