# MinJun 작가 홈페이지 (로컬)

이 폴더는 MinJun 작가의 정적 홈페이지 골격입니다.

- 이미지 추가: `site/images/` 폴더에 JPG/PNG 파일을 넣으세요.
- 소개(bio) 편집: `index.html`의 `#bio` 부분을 편집하세요.
- 로컬 미리보기(간단):

```bash
python -m http.server 8000
# 그런 다음 브라우저에서 http://localhost:8000/site/ 를 엽니다.
```

권장 이미지 크기: 가로 1200px 내외, 파일당 최대 2-3MB 권장.

원하시면 제가 `민준작품` 폴더의 이미지를 `site/images/`로 복사하고 갤러리를 자동 생성해드릴 수 있습니다.
