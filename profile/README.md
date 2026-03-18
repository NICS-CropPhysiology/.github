# Digital Lab, Crop Production & Physiology Division, RDA

식량과학원 재배생리과 디지털연구실 Git Organization입니다.

이 Organization은 **연구 코드 관리, 협업, 재현 가능한 연구 환경 구축**을 목적으로 운영됩니다.  
GitHub에는 **코드 및 연구 재현을 위한 스크립트만 관리**하며, 대용량 데이터는 별도의 저장소에서 관리합니다.

---

## Organization Rules

- Repository는 반드시 README 포함
- `.gitignore` 적용
- 데이터 업로드 금지
- PR 기반 협업

---

## Administrators

현재 Organization 관리자

- 민간전문가

### 관리자 권한

- Organization 설정 관리
- Repository 생성 및 관리
- 권한 관리

---

## Repository Policy

Repository 운영 기본 원칙

1. GitHub에는 **코드만 업로드**
2. 데이터셋 및 대용량 파일 업로드 금지
3. 모든 repository에는 `README.md` 작성
4. `.gitignore` 설정 필수
5. `main` 브랜치 직접 push 지양 (**Pull Request 권장**)

---

## Repository Structure

Repository는 다음 목적에 따라 생성됩니다.

| Type | Description |
| :--- | :--- |
| **project** | 연구 프로젝트 코드 |
| **tools** | 데이터 처리 및 실험 도구 |
| **web** | 결과 시각화 및 서비스 |
| **docs** | 문서 및 가이드 |

---

## Repository README Template

새로운 repository 생성 시 다음 구조를 따릅니다.

```markdown
# Project Name

## Overview
프로젝트 설명

## Installation
환경 설정 방법

## Usage
사용 방법

## Directory Structure
프로젝트 구조 설명

  예시)
  project-name
  ├─ src
  ├─ configs
  ├─ scripts
  ├─ notebooks
  ├─ experiments
  └─ docs

## Requirements
필요한 라이브러리 및 환경

예시)
Python >= 3.10
numpy
pandas
torch
```

---

## Basic `.gitignore` Policy

다음 항목은 반드시 `.gitignore`에 포함해야 합니다.

```gitignore
# OS
.DS_Store
Thumbs.db

# Python
__pycache__/
*.pyc

# Environment
.env
venv/
.env.local

# Logs
*.log

# Dataset
data/
dataset/
datasets/

# Model files
*.pt
*.pth
*.ckpt

# Build
dist/
build/

# IDE
.vscode/
.idea/
```

---

## Contribution Guide
1. Repository fork 또는 branch 생성
2. 기능 개발
3. Pull Request 생성
4. 코드 리뷰 후 병합

---

## Contact

문의 사항은 Organization 관리자에게 연락 바랍니다.
