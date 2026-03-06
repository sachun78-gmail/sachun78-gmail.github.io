# sachun78.github.io

GitHub Pages(Jekyll) 기반 포트폴리오 템플릿입니다.

## 구조

- `_config.yml`: Jekyll 설정
- `_layouts/default.html`: 공통 레이아웃
- `_data/profile.yml`: 기본 프로필/역량 데이터
- `_data/projects.yml`: 프로젝트 이력 데이터
- `index.md`: 메인 페이지(데이터 렌더링)
- `assets/css/style.css`: 스타일

## GitHub Pages 배포

1. 이 저장소를 `username.github.io` 형태로 유지
2. `main` 브랜치에 push
3. GitHub `Settings > Pages`에서 배포 브랜치가 `main / root`인지 확인

## 로컬 실행 (선택)

Ruby/Jekyll 환경이 있다면:

```bash
bundle install
bundle exec jekyll serve
```

브라우저에서 `http://127.0.0.1:4000` 확인

## 내용 수정

- 소개/스킬 변경: `_data/profile.yml`
- 프로젝트 추가/수정: `_data/projects.yml`
