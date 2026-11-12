# The Arc Archive

> **Enterprise Backend Architect | Ledger Integrity, Distributed Pipelines & Resilient Systems**  
> GitHub Pages: [boris-arc-dev.github.io](https://boris-arc-dev.github.io)

Jekyll [Chirpy](https://github.com/cotes2020/jekyll-theme-chirpy) 테마 기반으로 구축된 Boris의 기술 블로그 저장소입니다.

---

## 🛠️ Tech Stack & Topology

- **Engine**: Jekyll & `jekyll-theme-chirpy`
- **CI/CD**: GitHub Actions (`.github/workflows/pages-deploy.yml`)
- **Container / Local Runtime**: OrbStack (Docker Compose)
- **Author Identity**: Boris (`boris.arcdev@gmail.com`)

---

## 🚀 로컬 프리뷰 실행 (OrbStack / Docker)

로컬 머신(Intel i9 macOS)의 서멀 스로틀링 및 Ruby 버전 의존성 컴파일 부담 없이, 경량화 컨테이너 데몬(OrbStack)을 통해 즉시 프리뷰할 수 있습니다.

```bash
# 로컬 개발 서버 시작 (http://localhost:4000)
docker compose up

# 백그라운드 구동 시
docker compose up -d

# 컨테이너 종료
docker compose down
```

---

## 📝 포스트 작성 규칙

포스트는 `_posts/` 디렉터리에 `YYYY-MM-DD-title.md` 형식으로 작성합니다.

```markdown
---
title: 포스트 제목
date: YYYY-MM-DD HH:MM:SS +0900
categories: [대분류, 소분류]
tags: [태그1, 태그2]
---

본문 내용 작성...
```

---

## 🚀 배포 (Deployment)

`main` 브랜치에 변경 사항을 `git push`하면 GitHub Actions 워크플로(`.github/workflows/pages-deploy.yml`)가 자동으로 실행되어 정적 사이트를 빌드하고 GitHub Pages로 배포합니다.
