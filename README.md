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

호스트 머신의 복잡한 Ruby 런타임 버전 관리나 네이티브 빌드 오버헤드 없이, 경량화 컨테이너 데몬(OrbStack / Docker)을 통해 즉시 로컬 프리뷰를 실행할 수 있습니다.

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

본 블로그는 **단일 마스터 지식 원장(`notes/guides/`)과 연동된 자동화 도구**를 통해 배포됩니다:

```bash
# notes/guides/ 에서 작성한 공개(public) 가이드 문서를 원클릭 배포:
blog-publish 2026-11-14-macos-dotfiles-and-zsh-internals.md

# ➡️ 1. 보안 검사 (식별자/시크릿 유출 및 visibility: internal 비공개 차단)
# ➡️ 2. _posts/ 로 자동 동기화
# ➡️ 3. Ed25519 SSH 디지털 서명이 적용된 Verified 커밋 생성
# ➡️ 4. GitHub Actions 자동 빌드 & 전 세계 라이브 서비스 완료!
```

* `main` 브랜치에 변경 사항이 푸시되면 GitHub Actions 워크플로(`.github/workflows/pages-deploy.yml`)가 자동으로 실행되어 정적 사이트를 빌드하고 GitHub Pages로 배포합니다.
