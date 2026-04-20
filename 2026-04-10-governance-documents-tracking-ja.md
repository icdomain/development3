---
layout: post
title: OpenAIとAnthropicにおけるガバナンス文書の追跡 2023-2026
description: RSP・Model Spec・Preparedness Frameworkを時系列で追跡し、停止条項が撤廃されるまでのガバナンス縮退の軌跡を一次資料から記録する。
permalink: /ja/archives/2026/04/10/governance-documents-tracking/
lang: ja
alt_lang_url: /en/archives/2026/04/10/governance-documents-tracking/
date: 2026-04-10T09:00:00Z
last_modified_at: 2026-04-10T09:00:00Z
author: founder
categories: [strategic-forecasting]
tags: [AI, ガバナンス, OpenAI, Anthropic, RSP, Model Spec, Preparedness Framework, AI安全性]
---

本稿は「[AI革命はすでにアンコントローラブルである]({{ site.baseurl }}/ja/archives/2026/04/09/ai-revolution-uncontrollable/)」の検証編として、ガバナンス文書の一次資料を時系列で追跡する。

## 第1期「LLMの黎明」2023年9月19日 〜 2024年5月7日

LLMがまだ自律的実行能力を持たないチャットインターフェースだった時代。※

- Anthropic RSP v1.0（2023年9月19日）
- OpenAI Preparedness Framework Beta（2023年12月18日）

Anthropicは Responsible Scaling Policy v1.0 で、モデルの能力水準に応じた安全基準（ASL）を設け、一定以上の能力水準を示したモデルは安全対策が整うまでより高性能なモデルの訓練停止や公開の延期を行うと規定した。

OpenAIも Preparedness Framework Beta で、能力レベル（Low / Medium / High / Critical）による評価を明記した。追跡カテゴリは5つ——CBRN（化学・生物・放射性・核）、Cybersecurity、Persuasion、Model Autonomy、Unknown Unknowns。High到達モデルは展開不可、Critical到達モデルはそれ以上の開発不可と規定された。

両社の方針は共通している——危険な能力を持つモデルは扱わない。この時期の文書は、停止判断の対象をモデル単位で具体的に定義し、閾値到達が停止の自動的なトリガーとして機能する構造を持っていた。

## 第2期「アシスタントの運用方針の確立」2024年5月8日 〜 2025年3月31日

アシスタントの役割とリスク評価基準が運用に即して明確化される。

- OpenAI Model Spec 初版（2024年5月8日）
- Anthropic RSP v2.0（2024年10月15日）
- Anthropic RSP v2.1（2025年3月31日）

Model Spec初版は、アシスタントの役割を「高潔な従業員（a talented, high-integrity employee）」と比喩し、明確な命令系統、Chain of Command（Platform > Developer > User > Tool）の中で行動することを、安全性と合法性を確保するためのルールとして定めている。加えて assistant は「明示的指示に従い、明示されていない意図にも過剰に踏み込まない範囲で応答する（following explicit instructions and reasonably addressing implied intent without overstepping）」ことを基本姿勢として記述されている。

RSP v2.0でASLは、モデルごとに危険度を判定する仕組みから、開発・公開時に満たすべき安全基準へと再定義された。

「not to train or deploy models capable of causing catastrophic harm unless we have implemented safety and security measures that will keep risks below acceptable levels」（破滅的危害を引き起こしうるモデルは、リスクを許容可能な水準に保つ安全対策を実装しない限り、訓練も展開も行わない）という姿勢が明確化され、具体的な閾値としてCBRN（化学・生物・放射性・核）およびAI R&Dの能力閾値が定められた。

RSP v2.1 では v2.0 の CBRN threshold と AI R&D threshold それぞれが内部的に細分化され（CBRN-3 / CBRN-4、AI R&D-4 / AI R&D-5）、ASL-4 を要する閾値が予告された。

## 第3期「リスク評価の放棄」2025年4月15日 〜 2025年5月13日

AI技術が深刻な危害を及ぼすリスクを持つレベルまで接近したという認識を示す一方でリスク評価機構は更に縮退した。

- OpenAI Preparedness Framework v2（2025年4月15日）

Preparedness Framework v2 は「soon have the capability to create meaningful risk of severe harm」（深刻な危害リスクを生む能力を持つに至るまで「もうすぐ」）と認めた上で、「reducing risk generally does not require reducing capability」（リスク低減は一般的に能力低減を必要としない）という原則を明文化した。AIの潜在的なリスクは運用で解決できると決めつける内容であり、運用で解決できないリスクの事前排除・停止という、LLM黎明期から守られてきた前提を放棄する宣言であった。

同時にリスクの評価関数からLLMの能力そのものを外し得るという論理構造であり、LLMによって生じた広範な災害、損害、社会変化を、LLMの問題ではなく運用の問題としてフレーミングする余地のあるものであった。

Preparedness Framework v2 では、これに加えて OpenAI Leadership（CEOまたはその指定代理人）が SAG の参加なしに決定を下せることが制度として明文化された——「SAGには審議を引き延ばす権限はない」と明記される形で。取締役会の安全保安委員会（SSC）が監督役として決定を review でき、必要に応じて取締役会が決定を覆せると規定されてはいるが、SAGが独立した専門家集団として機能しうるのに対し、SSCおよび取締役会の判断基準はOpenAI Leadershipの利害と運用上隣接しており、実質的な歯止めとして機能するかは別問題である。

## 第4期「アンコントローラブル」2025年5月14日 〜 現在

Agent技術の実装を正当化する一方で、上流の人間への責任の集中や、責任をうやむやにさせないための法整備については議論されないまま、停止条項そのものが文書から撤去される。

- OpenAI Model Spec 改訂（2025年9月12日版／10月27日版／12月18日版）
- Anthropic RSP v2.2（2025年5月14日）
- Anthropic RSP v3.0（2026年2月24日）
- Anthropic RSP v3.1（2026年4月2日）

OpenAI Model Spec の9月12日版では、初版に存在しなかった agent 概念が定義に追加された——「より自律的な展開で使われることがある（sometimes used for more autonomous deployments）」として agent という語が assistant の対概念として導入された。同時に「Scope of Autonomy」セクションが新設され、複数ステップの目標達成の過程で欠けている詳細を自ら埋め、自律的に行動しなければならない場合がある（filling in missing details / must sometimes act autonomously）として、Agentの利用が正当化された。一方で、同じ9月12日版の「No other objectives」セクションには「assistant は applicable instructions に基づく目標のみを追求してよく、その他の目標を採用・最適化・直接追求してはならない（may only pursue goals entailed by applicable instructions ... must not adopt, optimize for, or directly pursue any additional goals）」と明記されている。同一版の中で禁止と正当化が同居する構造となっており、上流の人間への責任の集中や、責任をうやむやにしないための仕組みや法整備については棚上げのままだった。

更に Scope of Autonomy セクション内には、禁止リストも導入されている——High-risk activities として hacking、deception、resource acquisition、spawning sub-agents、self-modification が、明示的許可なき限り禁止とされた。この禁止リストの存在は OpenAI 自身がこれらを「禁止しなければデフォルトで起こりうる行動」として認識していたことを示している。

10月27日版では、Tool use 時の AGENTS.md等を経由した暗黙的権限委譲が明文化された。アシスタントは明示的な指示がなくても、ツール出力や周辺文書から「暗黙的に委譲された権限」として行動できる範囲が拡大された。

12月18日版では、16歳 Adam Raine の自殺訴訟（2025年8月提訴、年内に計8件の ChatGPT 関連訴訟）を受けて、U18 Principles が追加された。既に9月12日版で Agent 自律性の危険性は業界自身が列挙していたにもかかわらず、具体的な未成年者保護の枠組みが整備されたのは、訴訟という外部圧力が加わった後であった。

RSP v2.2 では ASL-3 Security Standard の保護対象範囲が見直され、sophisticated insiders と state-compromised insiders が保護対象から除外された——CBRN-3 の threat model では universal jailbreak 経由のアクセスが主たる経路であり、AI R&D-4 では model weight theft に依存しないことを理由として、これらの insider に対する保護は当該 risk level に対して必要ないと判断された。

RSP v3.0 では、collective action problem（先行して停止した responsible developer が weaker protections の競合に追い越される懸念）を理由として、v2.0 の「破滅的危害を引き起こしうるモデルは、リスクを許容可能な水準に保つ安全対策を実装しない限り、訓練も展開も行わない」という絶対的停止条項が、Anthropic 単独の commitment から外され、業界全体への提言（industry-wide recommendations）の側に位置付け直された。

RSP v3.1 では Appendix A 冒頭に「Further, the commitments below do not preclude us from taking cautionary action, such as refraining from training or deploying models, in other circumstances. Mitigating the risks from our models is a top priority for us, and we would strongly consider pausing development and/or deployment to improve the safety profiles of our models even in cases not covered below.」（さらに、以下の commitment は、他の状況下で訓練・展開を見送るといった慎重な行動を取ることを排除しない。我々のモデルが及ぼすリスクの軽減は最優先事項であり、本 commitment の対象外のケースであっても、モデルの安全性プロファイルを改善するため、開発・展開の停止を強く検討する）という文言が追記された。

## 一次資料

本稿で引用した一次資料の所在。リンクはすべてローカルアーカイブ。

### Anthropic — Responsible Scaling Policy

- RSP v1.0（2023-09-19）— [PDF](./docs/anthropic-rsp-v1.0-2023-09-19.pdf) p.2「Framework」（ASL の定義、停止条項：scaling pause / deployment delay）、p.3-4「Initial Commitments」（ASL 一覧表、訓練停止の明文化）
- RSP v2.0（2024-10-15）— [PDF](./docs/anthropic-rsp-v2.0-2024-10-15.pdf) Executive Summary（ASL の再定義、停止条項の明確化）、p.3「Capability Thresholds and Required Safeguards」（CBRN・AI R&D の能力閾値）
- RSP v2.1（2025-03-31）— [PDF](./docs/anthropic-rsp-v2.1-2025-03-31.pdf) p.4「Capability Thresholds」（ASL-4 閾値の追加、CBRN・AI R&D の細分化）
- RSP v2.2（2025-05-14）— [PDF](./docs/anthropic-rsp-v2.2-2025-05-14.pdf) p.18-19「Changelog: May 14, 2025」（ASL-3 Security Standard の保護対象範囲見直し）
- RSP v3.0（2026-02-24）— [PDF](./docs/anthropic-rsp-v3.0-2026-02-24.pdf) p.3「Introduction」（collective action problem を理由とする方針転換、industry-wide recommendations への分離）
- RSP v3.1（2026-04-02）— [PDF](./docs/anthropic-rsp-v3.1-2026-04-02.pdf) p.15「Appendix A」冒頭（do not preclude us 文言）、p.19「Changelog: April 2, 2026」

### OpenAI — Preparedness Framework

- Preparedness Framework Beta（2023-12-18）— [PDF](./docs/openai-preparedness-framework-beta-2023-12-18.pdf) p.5「Tracked Risk Categories」（Low/Medium/High/Critical 4段階、5カテゴリ）、p.8-10（Cybersecurity / CBRN / Persuasion の閾値定義）
- Preparedness Framework v2（2025-04-15）— [PDF](./docs/openai-preparedness-framework-v2-2025-04-15.pdf) p.3「soon have the capability to create meaningful risk of severe harm」、p.14「reducing risk generally does not require reducing capability」、p.15「Appendix B: Governance」（SAG / OpenAI Leadership / SSC / Board の意思決定構造）

### OpenAI — Model Spec

- 初版（2024-05-08）— [HTML](./docs/openai-model-spec-2024-05-08.html) `#objectives`（"talented, high-integrity employee"）、`#follow-the-chain-of-command`（Chain of Command: Platform > Developer > User > Tool）、`#be-as-helpful-as-possible-without-overstepping`（"following explicit instructions and reasonably addressing implied intent without overstepping"）
- 改訂版（2025-09-12）— [HTML](./docs/openai-model-spec-2025-09-12.html) `#chain_of_command`、`#no_other_objectives`（"may only pursue goals entailed by applicable instructions ... must not adopt, optimize for, or directly pursue any additional goals"）、`#scope_of_autonomy`（agent 定義の追加、High-risk activities 禁止リスト）
- 改訂版（2025-10-27）— [HTML](./docs/openai-model-spec-2025-10-27.html) `#ignore_untrusted_data`（AGENTS.md 等のツール出力を経由した暗黙的権限委譲）
- 改訂版（2025-12-18）— [HTML](./docs/openai-model-spec-2025-12-18.html) `#chatgpt_u18`、`#prioritize_teen_safety`（U18 Principles）

## 注

※ Anthropic RSP v3.0（2026年2月24日）の説明文より：「2023年9月にRSPを書いた当時、大規模言語モデルは本質的にチャットインターフェースだった」。
