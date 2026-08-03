# HRMS Project

## Overview

HRMS는 社内勤怠管理システム 리뉴얼 프로젝트다.

이 문서는 HRMS 경험을 리더십, Spring Boot, React, AWS, AI 활용 프로세스 관점으로 정리한다.

---

## Project Summary

| Item | Description |
|---|---|
| Period | 2024-02 ~ 2025-04 |
| Domain | HRMS / 勤怠管理 |
| Role | Sub Leader / Leader |
| Phase | 要件整理, 基本設計, 詳細設計, 実装, テスト, 環境構築, 運用改善 |
| Backend | Java 18, Spring Boot 3.4.5, Spring Security 6.3.0 |
| Frontend | React 18 |
| Database | PostgreSQL 16.10, Redis 7.1.0 |
| AI Tool | Claude 3 Opus |
| Team | 全6名 |

---

## Important Concepts

| Concept | Interview Point |
|---|---|
| Leadership | 개발方針, 進捗管理, review |
| Spring Boot | API, batch, security |
| HRMS | 근태, 관리자 기능, 인증 |
| AI Process | prompt, template, review |
| Standardization | 재현 가능한 개발 프로세스 |

---

## Expected Questions

- HRMSではどのような役割を担当しましたか。
- リーダーとして意識したことは何ですか。
- Spring Securityをどのように利用しましたか。
- AIを活用して何を改善しましたか。
- メンバー支援では何をしましたか。
- 開発プロセス標準化とは具体的に何ですか。

---

## Japanese Model Answers

### Q1. HRMSではどのような役割を担当しましたか。

```text
HRMSプロジェクトでは、社内勤怠管理システムのリニューアル開発に、
サブリーダー・リーダーとして参画しました。

Spring BootとReactを用いたWebアプリケーション開発に加えて、
認証機能、管理者機能、Web API、Javaバッチ機能の設計・開発を担当しました。

また、開発方針の整理、進捗管理、コードレビュー、メンバー支援、
AWS環境構築、CI/CDパイプライン整備にも取り組みました。
```

### Q2. AIを活用して何を改善しましたか。

```text
HRMSでは、AIを使って設計・実装・テスト工程のレビュー品質を安定させる取り組みを行いました。

具体的には、AIレビュー用のプロンプトやMarkdownテンプレートを整備し、
要件定義、基本設計、詳細設計、実装、テストの各工程で、
確認すべき観点を明確にしました。

これにより、属人的になりやすいレビュー観点を標準化し、
開発効率だけでなく、レビュー品質の向上にもつなげることを意識しました。
```

---

## Korean Explanation

- HRMS는 “리더십 + Spring + AI 표준화”를 보여주는 프로젝트다.
- Tokyo-Sane보다 회사 내부 프로젝트 성격이 있으므로 팀 개발・レビュー를 강조한다.
- AI 경험은 “프롬프트 정리”보다 “工程별 확인 관점 표준화”라고 말하면 강하다.

---

## Follow-up Questions

- 進捗管理ではどのような情報を見ていましたか。
- コードレビューでは何を重視しましたか。
- メンバー支援で難しかったことは何ですか。
- 認証機能で注意した点は何ですか。
- 勤怠管理システムで重要な業務ルールは何ですか。
- AIレビューのテンプレートには何を書きましたか。
- 標準化によってどのような効果がありましたか。

---

## Technical Deep Dive

### HRMS Domain Points

- 출퇴근 기록
- 근무 시간 계산
- 휴가/결근 관리
- 관리자 승인
- 권한 분리
- 배치 처리
- 감사 로그

### Leadership Actions

- 작업 우선순위 정리
- 개발方針 공유
- 코드 리뷰
- 진행 상황 확인
- 막힌 부분 지원
- AI 활용 가이드 정리

---

## Checklist

- [ ] HRMS에서 맡은 역할을 리더 관점으로 말할 수 있다.
- [ ] Spring Security 관련 질문을 대비한다.
- [ ] AI 리뷰 템플릿의 목적을 설명할 수 있다.
- [ ] 팀 개발 기여를 구체적으로 설명한다.

