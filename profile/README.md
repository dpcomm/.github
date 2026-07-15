<div align="center">
  <img src="./assets/cba-connect-icon.png" width="112" alt="CBA Connect app icon" />
  <h1>RE:CBA · 개기자팀</h1>
  <p><strong>공동체의 필요를 발견하고, 디지털 플랫폼으로 연결합니다.</strong></p>
  <p>Discover · Build · Operate · Improve</p>
  <p>
    <a href="https://play.google.com/store/apps/details?id=com.cba.cba_connect_application&amp;pcampaignid=web_share">
      <img alt="Google Play에서 다운로드" src="https://img.shields.io/badge/Google_Play에서_다운로드-414141?style=for-the-badge&logo=googleplay&logoColor=white" />
    </a>
    <a href="https://apps.apple.com/kr/app/cba-connect/id6747623245">
      <img alt="App Store에서 다운로드" src="https://img.shields.io/badge/App_Store에서_다운로드-0D96F6?style=for-the-badge&logo=apple&logoColor=white" />
    </a>
  </p>
</div>

## We are

**개기자팀**은 성락교회 CBA 대학청년부 공동체 안팎의 문제를 디지털 플랫폼으로 연결하는 스프린트 중심의 팀입니다.

수련회 운영의 작은 불편을 해결하는 모임에서 시작해, 지금은 **CBA Connect**를 직접 만들고 운영하고 있습니다. 개발자만의 팀이 아니라 공동체의 필요를 발견하고, 문제를 정의하고, 디지털로 해결하는 팀입니다.

| Discover | Build | Operate | Improve |
| --- | --- | --- | --- |
| 현장의 필요와 불편을 찾습니다. | 앱, 웹, 서버와 인프라를 만듭니다. | 실제 공동체 행사와 일상에서 운영합니다. | 사용자 피드백과 운영 경험을 다음 개선으로 연결합니다. |

## CBA Connect

<p align="center">
  <img src="./assets/cba-connect-platform-showcase.webp" width="100%" alt="CBA Connect 모바일 앱, 백오피스, 카풀 및 QR 체크인 통합 화면" />
</p>

**CBA Connect**는 공동체의 행사 준비부터 현장 운영까지 하나의 흐름으로 연결하는 플랫폼입니다. 참여자는 필요한 정보를 쉽게 확인하고 신청하며, 운영자는 반복 업무를 줄이고 더 정확하게 현장을 관리할 수 있습니다.

| 영역 | 주요 기능 |
| --- | --- |
| 신청과 결제 | 수련회 및 행사 신청, 식사·교통 옵션, 납부 상태 관리 |
| 안내와 소통 | 공지사항, 가이드북, 푸시 알림, 이메일 인증 |
| 이동과 현장 | 카풀 연결, QR 체크인, 출석 및 신청자 관리 |
| 운영 도구 | 웹 백오피스, 관리자 앱, 대시보드, 계정 및 시스템 설정 |

## Our journey

| 시기 | 변화 |
| --- | --- |
| **2024 Summer** | React 웹 MVP와 Express·Prisma 기반 서버를 구축하고 첫 수련회에서 실제 운영을 시작했습니다. |
| **2024 Winter – 2025 Spring** | 여러 수련회와 행사로 도메인을 확장하고, 신청 내역·가이드북·운영 안정성을 개선했습니다. |
| **2025 Summer** | 모바일 경험을 강화하며 카풀, 채팅, 실시간 기능과 푸시 알림을 도입했습니다. |
| **2025 Winter – 2026** | React Native 앱과 NestJS 서버로 전환하고 Kubernetes 기반 운영 환경과 QR 관리자 앱을 구축했습니다. |
| **Now** | 행사 운영 도구를 넘어 공동체의 일상과 사역을 연결하는 플랫폼으로 확장하고 있습니다. |

## Platform

```mermaid
flowchart LR
    Member[공동체 구성원] --> App[React Native App]
    Operator[운영자] --> Backoffice[Web Backoffice]
    Operator --> AdminApp[Admin App]
    App --> API[NestJS API]
    Backoffice --> API
    AdminApp --> API
    API --> Data[(MySQL · Redis)]
    API --> Queue[RabbitMQ]
    Queue --> Workers[Email · Push Workers]
    API --> Storage[Object Storage]
    Actions[GitHub Actions] --> Registry[OCI Registry]
    Registry --> GitOps[Argo CD]
    GitOps --> Cluster[Kubernetes]
```

<p>
  <img alt="React Native" src="https://img.shields.io/badge/React_Native-20232A?style=flat-square&logo=react&logoColor=61DAFB" />
  <img alt="NestJS" src="https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white" />
  <img alt="TypeScript" src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" />
  <img alt="Kubernetes" src="https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white" />
  <img alt="Argo CD" src="https://img.shields.io/badge/Argo_CD-EF7B4D?style=flat-square&logo=argo&logoColor=white" />
  <img alt="Oracle Cloud" src="https://img.shields.io/badge/Oracle_Cloud-F80000?style=flat-square&logo=oracle&logoColor=white" />
</p>

## Repositories

| Repository | 역할 |
| --- | --- |
| [`cba_connect`](https://github.com/dpcomm/cba_connect) | 구성원이 사용하는 React Native 모바일 앱 |
| [`cba_was_renewal`](https://github.com/dpcomm/cba_was_renewal) | NestJS 기반 API와 이메일·푸시 워커 |
| [`cba_app_management`](https://github.com/dpcomm/cba_app_management) | 행사와 계정을 운영하는 웹 백오피스 |
| [`cba_connect_admin`](https://github.com/dpcomm/cba_connect_admin) | QR 체크인과 현장 운영을 위한 관리자 앱 |
| `cba_infra` | Kubernetes, Argo CD, Terraform 기반 인프라와 GitOps 구성 |

## Members

<table>
  <tr>
    <td align="center" width="20%">
      <a href="https://github.com/Hoooooou-Jun">
        <img src="https://github.com/Hoooooou-Jun.png?size=120" width="96" alt="김호준 GitHub profile" /><br />
        <sub><b>김호준</b></sub><br />
        <sub>팀 리드 · 풀스택 · 인프라</sub><br />
        <sub>@Hoooooou-Jun</sub>
      </a>
    </td>
    <td align="center" width="20%">
      <a href="https://github.com/limcr-dev">
        <img src="https://github.com/limcr-dev.png?size=120" width="96" alt="임채린 GitHub profile" /><br />
        <sub><b>임채린</b></sub><br />
        <sub>모바일 앱 · 프론트엔드</sub><br />
        <sub>@limcr-dev</sub>
      </a>
    </td>
    <td align="center" width="20%">
      <a href="https://github.com/Gusq1s">
        <img src="https://github.com/Gusq1s.png?size=120" width="96" alt="박현빈 GitHub profile" /><br />
        <sub><b>박현빈</b></sub><br />
        <sub>백엔드</sub><br />
        <sub>@Gusq1s</sub>
      </a>
    </td>
    <td align="center" width="20%">
      <a href="https://github.com/qlqqqk">
        <img src="https://github.com/qlqqqk.png?size=120" width="96" alt="전형진 GitHub profile" /><br />
        <sub><b>전형진</b></sub><br />
        <sub>풀스택</sub><br />
        <sub>@qlqqqk</sub>
      </a>
    </td>
    <td align="center" width="20%">
      <a href="https://github.com/1214sujin">
        <img src="https://github.com/1214sujin.png?size=120" width="96" alt="강수진 GitHub profile" /><br />
        <sub><b>강수진</b></sub><br />
        <sub>웹 프론트엔드</sub><br />
        <sub>@1214sujin</sub>
      </a>
    </td>
  </tr>
  <tr>
    <td align="center" width="20%">
      <a href="https://github.com/jung-ing">
        <img src="https://github.com/jung-ing.png?size=120" width="96" alt="유정인 GitHub profile" /><br />
        <sub><b>유정인</b></sub><br />
        <sub>백엔드</sub><br />
        <sub>@jung-ing</sub>
      </a>
    </td>
    <td align="center" width="20%">
      <img src="./assets/member-minseo.svg" width="96" alt="이민서" /><br />
      <sub><b>이민서</b></sub><br />
      <sub>UI/UX 디자인</sub>
    </td>
    <td align="center" width="20%">
      <a href="https://github.com/anna-choisk">
        <img src="https://github.com/anna-choisk.png?size=120" width="96" alt="최슬기 GitHub profile" /><br />
        <sub><b>최슬기</b></sub><br />
        <sub>서비스 기획</sub><br />
        <sub>@anna-choisk</sub>
      </a>
    </td>
    <td align="center" width="20%">
      <a href="https://github.com/lyg010502">
        <img src="https://github.com/lyg010502.png?size=120" width="96" alt="이영광 GitHub profile" /><br />
        <sub><b>이영광</b></sub><br />
        <sub>백엔드</sub><br />
        <sub>@lyg010502</sub>
      </a>
    </td>
    <td align="center" width="20%">
      <a href="https://github.com/lawproclaim">
        <img src="https://github.com/lawproclaim.png?size=120" width="96" alt="국윤령 GitHub profile" /><br />
        <sub><b>국윤령</b></sub><br />
        <sub>자문 · 팀 지원</sub><br />
        <sub>@lawproclaim</sub>
      </a>
    </td>
  </tr>
</table>

## How we work

- 필요한 기능을 작은 스프린트 단위로 나누고, 목적에 맞는 TF를 유연하게 구성합니다.
- 무엇을 만드는지보다 **왜 필요한지**와 원인·결과의 흐름을 먼저 이해합니다.
- 문서와 대화를 통해 맥락을 공유하고, 맡은 결과에 끝까지 책임집니다.
- 실제 사용자의 목소리와 운영 데이터를 다음 제품 결정에 반영합니다.

## What we believe

우리가 만드는 결과물과 일하는 과정에 하나님의 마음이 드러나기를 바랍니다. 사랑과 신뢰로 연합하고, 공동체에 좋은 대안을 제시하며, 서로의 성장을 돕는 팀을 지향합니다.

---

<div align="center">
  <strong>Built and operated by RE:CBA · 개기자팀</strong><br />
  <sub>Connecting people, ministry and everyday community life.</sub>
</div>
