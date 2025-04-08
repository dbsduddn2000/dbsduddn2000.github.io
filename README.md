Visit **[dbsduddn2000.github.io](https://dbsduddn2000.github.io)** 🚀


  ![on-push](../../actions/workflows/on-push.yaml/badge.svg)
  ![on-pull-request](../../actions/workflows/on-pull-request.yaml/badge.svg)
  ![on-schedule](../../actions/workflows/on-schedule.yaml/badge.svg)

# 🌐 사이트 관리 안내

---

## 🚫 수정 주의사항
- **⚠️ `gh-pages` 브랜치는 직접 수정하지 마세요!**
  - 모든 수정은 반드시 `main` 브랜치에서 진행해야 합니다.
  - `main` 브랜치에 수정이 발생하면 자동으로 `gh-pages` 브랜치로 **pull & build**됩니다.  
  - 자동 빌드는 약 **20~30초** 정도 소요되며, **Pull Requests** 항목에서 진행 상황을 확인할 수 있습니다.

---

## 📁 사이트 데이터 저장 위치
| 항목 | 경로 | 설명서 |
|------|------|--------|
| 📰 Publication Page | `_data/citations_cvmi.yaml` | [논문 관련 정보](_document/citations_cvmi.md) |
| 📂 Project Page | `_data/projects.yaml` | [프로젝트 관련 정보](_document/projects.md) |
| 📝 Blog Page | `_posts/` | [블로그 관련 정보](_document/posts.md) |
| 🖼 이미지 | `images/` 폴더 내 관리 |  |
| 👥 Member Page | `_members/` | [멤버 관련 정보](_document/members.md) |
| 🧱 Entity HTML (템플릿) | `_includes/`, `_layouts/` | [N/A] |

> 🔍 **이미지를 삽입할 경우**, 반드시 `images` 폴더에 업로드한 뒤 해당 경로를 사용해주세요.

---

## 📄 사이트 페이지 마크다운 정보
| 항목 | 경로 |
|------|------|
| 🏠 Home | `index.md` |
| 🔬 Research | `research/index.md` |
| 📁 Projects | `projects/index.md` |
| 👨‍🏫 Professor | `professor/index.md` |
| 📝 Blog | `blog/index.md` |
| ✉️ Contact | `contact/contact.md` |

> 📌 **페이지를 수정하는 경우**, 해당 경로에 있는 `.md` 파일을 편집해주세요.
> 📌 **페이지를 추가하는 경우**, 경로를 생성하고 `.md` 파일의 형식에 맞게 작성 해주세요.

---

## 🌍 사이트 주소
**➡️ [dbsduddn2000.github.io](https://dbsduddn2000.github.io)**

---

## ✅ 빌드 확인 & 반영 팁
- `main` 브랜치 수정 시 자동으로 빌드되어 `gh-pages`에 반영됩니다.
- 빌드 완료 후에도 수정 사항이 **반영되지 않은 것처럼 보일 경우**:
  - 브라우저의 **캐시 또는 세션** 문제일 수 있습니다.
  - **시크릿 모드**에서 확인하거나, **크롬 인터넷 기록 삭제** 후 다시 확인해주세요.
  - 또한, header와 같이 여러 페이지에 보여지는 entity의 경우에는 각 페이지마다 **refresh**를 해야 반영된 정보가 보입니다.

---










