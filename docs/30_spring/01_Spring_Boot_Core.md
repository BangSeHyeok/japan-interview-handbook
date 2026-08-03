# Spring Boot Core Interview

## Overview

Spring Boot 면접에서는 DI, Layered Architecture, Transaction, Security, Test에 대한 실무 설계 감각을 확인한다.

---

## Important Concepts

| Concept | Why It Matters |
|---|---|
| DI / IoC | 결합도를 낮추고 테스트하기 쉽게 만든다 |
| Layered Architecture | Controller, Service, Repository 책임 분리 |
| Transaction | 데이터 정합성과 롤백 제어 |
| Security | 인증과 인가 분리 |
| Configuration | 운영 환경별 설정 관리 |

---

## Expected Questions

| Level | Question |
|---|---|
| Basic | Spring Bootとは何ですか。 |
| Basic | DIとは何ですか。 |
| Intermediate | Controller, Service, Repositoryの責務を説明してください。 |
| Intermediate | `@Transactional`の注意点は何ですか。 |
| Advanced | Spring Securityで認証と認可をどう設計しますか。 |
| Expert | Spring Bootアプリケーションの性能問題をどう調査しますか。 |

---

## Japanese Model Answers

### Q1. Spring Bootを使うメリットは何ですか。

```text
Spring Bootのメリットは、Spring Frameworkを利用したアプリケーション開発を効率化できる点です。
自動設定や組み込みサーバー、Starterによって、Web APIやバッチ処理を比較的短い時間で構築できます。

実務では、Controller、Service、Repositoryの責務を分けることで、
保守しやすくテストしやすい構成を意識しています。

ただし、自動設定に依存しすぎると内部で何が設定されているか分かりにくくなるため、
セキュリティ、トランザクション、DB接続設定などは明示的に理解しておく必要があると考えています。
```

### Q2. `@Transactional`の注意点は何ですか。

```text
`@Transactional`では、まずトランザクション境界をどこに置くかを意識しています。
基本的には業務処理の単位であるService層に付与し、
複数のDB操作を一つの整合性単位として扱います。

注意点としては、同じクラス内のメソッド呼び出しではProxyが効かないケースがあること、
例外の種類によってロールバック条件が変わること、
トランザクションを長く保持するとロックや性能問題につながることがあります。

そのため、業務単位、例外設計、DBロック、処理時間を合わせて考えるようにしています。
```

---

## Korean Explanation

- Spring Boot의 장점은 빠른 개발이지만, 답변은 반드시 설계와 운영 관점으로 확장해야 한다.
- `@Transactional`은 Proxy, rollback, lock, boundary가 핵심 꼬리질문이다.
- Controller/Service/Repository 책임 분리는 거의 반드시 나온다.

---

## Follow-up Questions

- DI를 사용하면 테스트가 쉬워지는 이유는 무엇인가요?
- `@Component`, `@Service`, `@Repository` 차이는 무엇인가요?
- Spring Bean의 Scope를 설명해주세요.
- Transaction propagation에는 어떤 종류가 있나요?
- 인증과 인가의 차이는 무엇인가요?
- JWT를 사용할 때 주의할 점은 무엇인가요?
- N+1 문제가 발생하면 어떻게 해결하나요?

---

## Technical Deep Dive

### Layer Responsibilities

| Layer | Responsibility |
|---|---|
| Controller | 요청/응답, validation, HTTP status |
| Service | 업무 로직, transaction boundary |
| Repository | DB 접근, query |
| DTO | 계층 간 데이터 전달 |
| Entity | 도메인 데이터 표현 |

### Transaction Mistakes

- Controller에 transaction을 두는 설계
- 너무 넓은 transaction 범위
- 예외를 catch하고 rollback되지 않는 구조
- 외부 API 호출을 transaction 안에서 수행
- self-invocation으로 transaction이 적용되지 않는 구조

---

## Checklist

- [ ] DI를 본인 말로 설명할 수 있다.
- [ ] Layer 책임을 명확히 설명할 수 있다.
- [ ] `@Transactional` 꼬리질문을 대비한다.
- [ ] Spring Security 경험을 인증/인가로 나눠 설명한다.

