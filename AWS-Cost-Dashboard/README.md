# AWS (A原始) - 费用趋势看板

与 `API-Cost-Dashboard` 同结构，数据来自飞书 **AI-平台消耗 → A原始**（单位：美元，截至 **10/17**）。

**分享/对比区块**（日走势、瀑布、占比）只展示 **10 月累计 TOP8** 服务；其余服务在瀑布/占比/明细里合并为「其他 (N 项)」。顶部 KPI 与表尾合计仍为全量。

## 打开方式

双击根目录 `AWS-看板.html`，或本目录 `AWS-Cost-Dashboard.html`。保存后 **Ctrl+F5** 强刷。

## 口径

- 含税累计、同期、整月、截止日合计都以飞书 **A 列显示值**为准：10 月合计 **$10,967.71**，9/1–9/17 **$10,495.10**，9 月合计 **$18,787.21**，10/17 **$683.18**，10/16 **$661.25**。分服务四舍五入后再相加为 **$10,967.75**，顶部和表尾合计不用这个数
- `week`：10/11–10/17 原币种日耗
- `d27` / `d26`：各服务 10/17、10/16 日耗；**表尾日合计**强制为飞书 **A155 / A154**（**$683.18 / $661.25**）
- `mtd`：10/1–10/17
- `augSame`：9/1–9/17（飞书 A 列同期合计 **$10,495.10**）
- `augFull`：9 月整月（飞书「9月合计」**$18,787.21**）
- `est`：`mtd ÷ 17 × 31`
- 10/18 及之后日单元格为空，不计入累计
- **Tax** 用「Tax($)」日列。**总税费**是累计数，不重复计入
- 顶部 **不含税** 累计/日均 = 全量合计减去 Tax 行
- 表内没有账户余额，看板不展示余额和可撑天数
- 美元卡片附约合人民币，汇率与其余 API 看板相同（×6.7108）

## 费用项与飞书列

| 看板项 | 飞书列 |
|--------|--------|
| S3 | S3($) |
| RDS | Relational Database Service($) |
| ECS | Elastic Container Service($) |
| ELB | Elastic Load Balancing($) |
| CloudFront | CloudFront($) |
| Amplify | Amplify($) |
| EC2 实例 | EC2 实例($) |
| ElastiCache | ElastiCache($) |
| VPC | VPC($) |
| CloudWatch | CloudWatch($) |
| EC2-其他 | EC2-其他($) |
| DMS | DMS($) |
| Rekognition | Rekognition($) |
| WAF | WAF($) |
| ECR | EC2 Container Registry (ECR)($) |
| Comprehend | Comprehend($) |
| ACM | Certificate Manager($) |
| Route 53 | Route 53($) |
| KMS | Key Management Service($) |
| Secrets Manager | Secrets Manager($) |
| GuardDuty | GuardDuty($) |
| Lambda | Lambda($) |
| Cost Explorer | Cost Explorer($) |
| Tax | Tax($) |

SNS、CloudShell、CloudTrail、Glue、CloudFront Flat-Rate Plans 等列在 9–10 月均为 0，未放入看板。
