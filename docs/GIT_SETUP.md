# Git / GitHub 연동 안내

로컬에서 Git을 초기화하고 GitHub에 연결하는 기본 단계입니다. 저는 로컬에서 Git 초기화 및 첫 커밋을 생성했습니다. 다음 단계로 GitHub 원격 저장소를 만든 뒤 로컬 저장소를 연결하고 푸시하세요.

1) GitHub에 새 저장소 만들기
- GitHub 웹에서 새 저장소를 생성하세요(예: `MinJun-art`). Public 또는 Private 선택.

2) 로컬에서 원격 추가 및 푸시

```bash
# 예: origin을 생성하고 main 브랜치로 푸시
git remote add origin https://github.com/your-username/your-repo.git
git branch -M main
git push -u origin main
```

3) Netlify / Vercel과 연결
- Netlify: 사이트 생성 → Import from Git → GitHub 선택 → 저장소 연결 → Publish directory에 `site` 입력
- Vercel: New Project → Import Git Repository → Root/Output directory에 `site` 지정

권장: 이미지 파일은 Git에 커밋하면 저장소 용량이 커질 수 있습니다. 빈번한 이미지 업데이트가 예상되면 LFS(Git Large File Storage) 사용을 고려하세요:

```bash
git lfs install
git lfs track "site/images/*"
git add .gitattributes
git add site/images/*
git commit -m "Track images with LFS"
```

문제가 있거나 제가 GitHub 연결을 단계별로 도와드리길 원하면 알려주세요(원격 생성에 필요한 정보: GitHub 사용자명, 저장소 이름).  
