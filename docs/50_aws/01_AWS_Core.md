# AWS Core Interview

## Overview

AWS 면접에서는 서비스 이름을 아는지보다, 실제 애플리케이션을 어떻게 안정적으로 배포하고 운영하는지 확인한다.

---

## Important Concepts

| Area | Concepts |
|---|---|
| Compute | EC2, ECS, Lambda |
| Database | RDS, backup, parameter |
| Network | VPC, subnet, security group |
| Storage | S3 |
| Security | IAM, least privilege |
| Delivery | CI/CD, environment separation |

---

## Expected Questions

| Level | Question |
|---|---|
| Basic | AWSで利用したサービスを教えてください。 |
| Intermediate | VPCとSecurity Groupを説明してください。 |
| Intermediate | RDSを利用するメリットは何ですか。 |
| Advanced | AWS環境でセキュリティ上注意する点は何ですか。 |
| Expert | 障害時にどのように原因調査しますか。 |

---

## Japanese Model Answers

### Q1. AWSでどのような経験がありますか。

```text
HRMSやTokyo-Saneのプロジェクトで、AWS環境構築とCI/CDパイプラインの整備を担当しました。

具体的には、アプリケーションを動作させる環境、DB接続、環境変数、デプロイフローなどを整理し、
開発からリリースまでの流れを標準化しました。

AWSでは便利なマネージドサービスを利用できる一方で、
IAM権限、ネットワーク設定、ログ、バックアップ、コスト管理を意識しないと、
運用上のリスクが高くなると考えています。
```

---

## Korean Explanation

- 현재 이력서에는 AWS 서비스 상세가 많지 않으므로, 과장하지 않는다.
- “환경 구축과 CI/CD 경험” 중심으로 말한다.
- IAM, 네트워크, 로그, 백업, 비용을 운영 관점으로 언급한다.

---

## Follow-up Questions

- 어떤 AWS 서비스를 사용했나요?
- IAM 권한은 어떻게 관리해야 하나요?
- Security Group과 NACL의 차이는 무엇인가요?
- RDS 백업 전략은 어떻게 설계하나요?
- CloudWatch 로그를 어떻게 활용하나요?
- CI/CD에서 환경 변수를 어떻게 관리하나요?
- 비용 최적화를 위해 무엇을 확인하나요?

---

## Technical Deep Dive

### AWS Operation Checklist

- IAM 최소 권한
- 네트워크 접근 제한
- DB 백업과 복구 절차
- 로그 수집과 알림
- 환경별 설정 분리
- 배포 실패 시 롤백 전략
- 비용 모니터링

---

## Checklist

- [ ] 실제 경험 범위를 과장하지 않는다.
- [ ] AWS를 운영 관점으로 설명한다.
- [ ] IAM, VPC, RDS, CI/CD 질문을 대비한다.
- [ ] Tokyo-Sane 경험과 연결한다.

