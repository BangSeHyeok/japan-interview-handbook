# Java Core Interview

## Overview

Java 면접에서는 문법 암기보다, 객체지향・컬렉션・예외・JVM・동시성에 대한 실무 이해를 확인한다.

---

## Important Concepts

| Concept | Interview Point |
|---|---|
| OOP | 책임 분리, 캡슐화, 다형성 |
| Collection | 자료구조 선택 이유 |
| Exception | 복구 가능성, 전파, 로그 |
| JVM | 메모리, GC, 성능 |
| Concurrency | Thread safety, race condition |

---

## Expected Questions

| Level | Question |
|---|---|
| Basic | Javaの特徴を説明してください。 |
| Basic | オブジェクト指向とは何ですか。 |
| Intermediate | `equals`と`hashCode`の関係を説明してください。 |
| Intermediate | `ArrayList`と`LinkedList`の違いは何ですか。 |
| Advanced | 例外処理で意識していることは何ですか。 |
| Advanced | Javaでメモリリークが起きるケースを説明してください。 |
| Expert | 本番環境でJavaアプリケーションが遅い場合、どう調査しますか。 |

---

## Japanese Model Answers

### Q1. Javaの特徴を説明してください。

```text
Javaは、オブジェクト指向をベースにした汎用的なプログラミング言語で、
JVM上で動作するため、環境に依存しにくい点が特徴だと理解しています。

業務システムでは、型安全性、豊富なライブラリ、Spring Bootなどの成熟したエコシステムにより、
保守性の高いアプリケーションを開発しやすいというメリットがあります。

一方で、設計を意識せずに実装するとクラスの責務が曖昧になり、
保守しにくいコードになりやすいため、責務分離やテストしやすさを意識しています。
```

### Q2. 例外処理で意識していることは何ですか。

```text
例外処理では、まずその例外が業務的に復旧可能かどうかを意識しています。

例えば入力値の不正や業務チェックエラーであれば、利用者に分かる形でエラーを返す必要があります。
一方で、DB接続エラーや予期しないシステムエラーの場合は、
適切にログを出力し、原因調査ができるようにすることが重要です。

また、例外を握りつぶすと障害調査が難しくなるため、
必要な情報をログに残しつつ、上位層で適切にハンドリングする設計を意識しています。
```

---

## Korean Explanation

- Java 특징 질문에서는 JVM, 객체지향, 생태계를 균형 있게 말한다.
- 예외 처리는 “복구 가능 여부”와 “로그・조사 가능성”이 핵심이다.
- 금융/업무 시스템 경험과 연결하면 신뢰도가 높다.

---

## Follow-up Questions

- Checked Exception과 Unchecked Exception의 차이는 무엇인가요?
- `HashMap`의 동작 원리를 설명할 수 있나요?
- `StringBuilder`와 `StringBuffer`의 차이는 무엇인가요?
- GC가 자주 발생하면 어떤 문제가 생기나요?
- Thread-safe한 코드를 만들기 위해 무엇을 고려하나요?
- Java 17에서 자주 사용하는 기능은 무엇인가요?
- 실무에서 Java 성능 문제를 조사한 경험이 있나요?

---

## Technical Deep Dive

### Collection 선택 기준

| Need | Candidate |
|---|---|
| 순서 유지, 조회 중심 | `ArrayList` |
| Key-Value 조회 | `HashMap` |
| 중복 제거 | `HashSet` |
| 정렬 유지 | `TreeMap`, `TreeSet` |
| 동시성 고려 | `ConcurrentHashMap` |

### Exception 설계 기준

- 업무 예외와 시스템 예외를 구분한다.
- 로그에는 원인 분석에 필요한 정보를 남긴다.
- 사용자에게 내부 구현 정보를 노출하지 않는다.
- 트랜잭션 롤백 조건을 함께 고려한다.

---

## Checklist

- [ ] Java의 장점과 한계를 함께 설명할 수 있다.
- [ ] Collection 선택 이유를 말할 수 있다.
- [ ] 예외 처리 원칙을 업무 시스템 관점으로 설명할 수 있다.
- [ ] JVM/GC 질문에 기본 답변을 준비한다.

