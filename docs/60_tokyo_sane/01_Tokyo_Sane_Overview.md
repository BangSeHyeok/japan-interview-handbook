# Tokyo-Sane Overview

## Overview

Tokyo-Sane은 한국 사용자를 대상으로 한 일본 상품 판매 EC 서비스다.

면접에서는 단순한 개인 프로젝트가 아니라, AI 주도 개발 프로세스와 백엔드 설계 역량을 보여주는 대표 프로젝트로 활용한다.

---

## Project Summary

| Item | Description |
|---|---|
| Project | Tokyo-Sane |
| Domain | EC / Cross-border Shopping |
| Period | 2025-04 ~ 2026-04 |
| Role | Main Developer / Leader |
| Backend | Java 18, Spring Boot 3.4.5, MyBatis |
| Frontend | React 18 |
| Database | PostgreSQL 16.10, Redis 7.1.0 |
| Infrastructure | AWS, CI/CD |
| AI Tool | Claude Code, Claude 3.7 Sonnet |

---

## Expected Questions

- Tokyo-Saneの概要を説明してください。
- なぜこのプロジェクトを作りましたか。
- 技術スタックを選んだ理由は何ですか。
- AI主導開発をどのように適用しましたか。
- 一番難しかった技術課題は何ですか。
- 今後改善したい点は何ですか。

---

## Japanese Model Answer

```text
Tokyo-Saneは、韓国向けに日本の商品を販売するECサービスとして開発した自主プロジェクトです。

私は主要開発担当として、要件整理、基本設計、詳細設計、インフラ設計、実装、テスト、
リリース、保守対応まで一貫して担当しました。

技術スタックとしては、バックエンドにSpring Boot、DBにPostgreSQL、
キャッシュや一部の高速アクセス用途にRedis、フロントエンドにReactを利用しました。

このプロジェクトで特に力を入れたのは、Claude Codeを中心としたAI主導開発環境の構築です。
Rules、Agents、Skillsを設計し、要件定義、設計、実装、レビュー、テストをAIが支援できる流れを作りました。

その結果、当初約18か月を想定していた開発を約12か月で完了し、
開発効率だけでなく、設計やレビューの再現性向上にもつながりました。
```

---

## Korean Explanation

- Tokyo-Sane은 “개인 프로젝트”보다 “자율 개발 + AI 프로세스 검증 프로젝트”로 말한다.
- 기간 단축은 수치가 있으므로 강점이다.
- 단, 품질을 희생했다는 인상을 주지 않도록 “재현성”과 “리뷰”를 함께 말한다.

---

## Follow-up Questions

- ECサービスで一番重要な設計観点は何ですか。
- PostgreSQLとRedisをどう使い分けましたか。
- MyBatisを選んだ理由は何ですか。
- 認証・認可はどのように設計しましたか。
- 注文処理の整合性はどう担保しますか。
- AIエージェントはどのように分けましたか。
- 18か月から12か月に短縮できた具体的な理由は何ですか。
- 本番運用するとしたら何を改善しますか。

---

## Technical Deep Dive

### Architecture Topics to Prepare

- 회원가입 / 로그인
- 상품 관리
- 주문 처리
- 결제 연동 가정
- 재고 관리
- 관리자 기능
- 캐시 전략
- CI/CD
- AWS 배포
- 로그와 모니터링

### AI Development Topics

- 요구사항 템플릿
- 설계 리뷰 Agent
- 구현 Agent
- 테스트 Agent
- 코드 리뷰 기준
- Markdown 기반 지식 축적

---

## Checklist

- [ ] 프로젝트 개요를 90초 안에 설명할 수 있다.
- [ ] 기술 선택 이유를 말할 수 있다.
- [ ] AI 주도 개발 성과를 수치로 말할 수 있다.
- [ ] EC 도메인의 정합성 질문을 대비한다.

