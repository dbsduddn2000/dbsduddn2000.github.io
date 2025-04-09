## 👤 팀 멤버 정보 구성 가이드

팀 멤버 정보를 작성할 때는 아래의 항목들을 활용하여 `YAML` 블록과 소개 글을 구성합니다.

| 파라미터       | 설명                                                                                       | 예시 값                                         | 필수 여부 |
|----------------|--------------------------------------------------------------------------------------------|--------------------------------------------------|-----------|
| `name`         | 팀 멤버의 표시 이름입니다. 개인 페이지 상단에 표시됩니다.                                   | `홍길동`                                         | ✅ 필수    |
| `image`        | 팀 멤버의 사진 경로입니다. `/images/team/` 폴더에 저장한 파일명을 연결하면 됩니다.          | `images/team/hong.jpg`                          | ❌ 선택    |
| `role`         | 팀 멤버의 역할 (예: 교수, 대학원생, 연구원 등). 역할에 따라 아이콘 및 기본 설명이 다릅니다. | `professor`, `student`, `programmer` 등         | ✅ 필수    |
| `description`  | 해당 멤버의 구체적인 역할이나 연구 분야를 설명합니다.                                       | `인공지능 기반 예측 시스템 연구 담당 교수`      | ❌ 선택    |
| `aliases`      | 이름의 다양한 표기 방식(논문용, 영문 표기 등)을 리스트로 작성합니다.                       | `["Hong Gil-Dong", "H. Gil-Dong"]`              | ❌ 선택    |
| `links`        | 홈페이지, 이메일, GitHub, 트위터 등 외부 링크를 지정합니다.                                 | `home-page: https://honglab.example.com/` 등    | ❌ 선택    |

---

## ✨ 예시 구성

```yaml
---
name: 홍길동
image: images/team/hong.jpg
role: professor
description: 인공지능 기반 예측 시스템 연구 담당 교수
aliases:
  - Hong Gil-Dong
  - H. Gil-Dong
links:
  home-page: https://honglab.example.com/
  email: hong@example.com
  github: honglab
  linkedin: hong-gil-dong
---
