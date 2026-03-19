# Digital Lab, Crop Production & Physiology Division, RDA
식량과학원 재배생리과 디지털연구실 Git Organization입니다.

이 Organization은 **연구 코드 관리, 협업, 재현 가능한 연구 환경 구축**을 목적으로 운영됩니다.  
GitHub에는 **코드 및 연구 재현을 위한 스크립트만 관리**하며, 대용량 데이터는 별도의 저장소에서 관리합니다.

---

## Organization Rules

- Repository는 반드시 `README.md` 포함
- `.gitignore` 적용 필수
- 데이터 및 대용량 파일 업로드 금지
- PR(Pull Request) 기반 협업 원칙

---

## Administrators

Organization 관리자에게 문의하세요.

| 역할 | 이름 | 연락처 |
| :--- | :--- | :--- |
| 민간전문가 (개발 담당) | 홍길동 | hong@rda.go.kr |

### 관리자 권한
- Organization 설정 관리
- Repository 생성 및 관리
- 멤버 권한 관리

---

## Repository Policy

Repository 운영 기본 원칙

1. GitHub에는 **코드만 업로드**
2. 데이터셋 및 대용량 파일 업로드 금지
3. 모든 Repository에는 `README.md` 작성
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

## Branch Naming Convention

| 브랜치 | 용도 |
| :--- | :--- |
| `main` | 안정된 최종 코드 |
| `dev` | 개발 통합 브랜치 |
| `feat/기능명` | 새 기능 개발 (예: feat/data-loader) |
| `fix/버그명` | 버그 수정 (예: fix/csv-parse-error) |

---

## Repository README Template

새로운 Repository 생성 시 다음 구조를 따릅니다.

```markdown
# Project Name

## Overview
프로젝트에 대한 간단한 설명 (2~3줄)

- **담당자**: 이름 (이메일)
- **기간**: 2024.03 ~ 2025.02
- **관련 데이터**: 로컬 DB 실험 ID 또는 경로

---

## Results
실험 결과 요약 및 주요 수치

| 모델 | 데이터셋 | 정확도 | 비고 |
|------|---------|--------|------|
| YOLOv8 | 토마토_2024 | 92.3% | 최종 모델 |

---

## Directory Structure

project-name
├─ src          # 핵심 코드
├─ configs      # 실험 설정 파일
├─ scripts      # 실행 스크립트
├─ notebooks    # 분석용 주피터 노트북
├─ experiments  # 실험 결과 로그
└─ docs         # 문서

---

## Installation
> 처음 설치하는 경우 담당자에게 문의하세요.

**1. 저장소 복사**
git clone https://github.com/lab-org/project-name
cd project-name

**2. 가상환경 생성**
python -m venv venv
source venv/bin/activate        # Mac / Linux
venv\Scripts\activate           # Windows

**3. 라이브러리 설치**
pip install -r requirements.txt

---

## Usage
코드 실행 방법

**학습**
python scripts/train.py --config configs/default.yaml

**추론**
python scripts/predict.py --input 이미지경로

---

## Requirements

Python >= 3.10
numpy
pandas
torch

---

## Related Data
이 프로젝트에서 사용한 데이터 위치

- **로컬 DB 실험 ID**: EXP-2024-001
- **데이터 경로**: /data/lab/crops/tomato/2024/
- **데이터 설명**: 토마토 생육 이미지 12,000장 (드론 촬영)

---

## Contact
문의사항이 있으면 아래로 연락주세요.

- **개발 담당**: 이름 / 이메일
- **데이터 담당**: 이름 / 이메일
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
.env.local
venv/

# Logs
*.log

# Dataset (대용량 데이터는 별도 저장소에서 관리)
data/
dataset/
datasets/

# Model weights (필요 시 관리자와 협의 후 예외 처리)
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

> **PR(Pull Request)** 이란 코드 변경사항을 팀원이 검토한 후 반영하는 협업 방식입니다.  
> 직접 `main` 브랜치에 올리지 않고, PR을 통해 코드 품질을 유지합니다.

1. Repository를 fork하거나 branch를 생성합니다
2. 기능을 개발합니다
3. Pull Request를 생성합니다
4. 관리자 코드 리뷰 후 `main`에 병합됩니다

---

## Contact

문의사항은 Organization 관리자에게 연락 바랍니다.

| 역할 | 이름 | 연락처 |
| :--- | :--- | :--- |
| 민간전문가 (개발 담당) | 홍길동 | hong@rda.go.kr |
