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

## 第3期「Agentの登場とリスク評価の縮退」2025年4月15日 〜 2025年5月13日

AIシステムが「ますますagentic（自律的）になりつつある」と認識される一方で、自律行動に関するリスク追跡は緩和される。

- OpenAI Preparedness Framework v2（2025年4月15日）

Preparedness Framework v2 は、AIシステムが「increasingly agentic」（ますます自律的）になりつつあり、「soon have the capability to create meaningful risk of severe harm」（深刻な危害リスクを生む能力を持つに至るまで「もうすぐ」）であると認めた。

同時に、旧 Preparedness Framework Beta の Model Autonomy カテゴリが3つに分割された。AI Self-improvement は Tracked Category（正式追跡対象）に昇格した一方、Long-range Autonomy（長期的自律行動）と Autonomous Replication and Adaptation（自律複製・適応）は Research Category（研究段階）に降格された。AIの自律性に伴うリスクを認識しながら、自律行動そのもののリスク追跡が緩和されている。

加えて「reducing risk generally does not require reducing capability」（リスク低減は一般的に能力低減を必要としない）という原則が明文化された。AIに潜在するリスクは運用で解決できるとする内容であり、運用で解決できないリスクの事前排除・停止という、第1期から続いてきた文脈とは趣の異なる宣言であることは注目に値する。

機械的に読むとリスクの評価関数からLLMの能力そのものを外し得るという論理構造でもあり、LLMによって生じる災害、損害、社会変化を、LLMの問題ではなく運用の問題としてフレーミングする余地を確保する文言のように読める点も注目に値する。

これに加えて「the SAG does not have the ability to 'filibuster'」（SAGには議事妨害の能力はない）と明記され、CEOは SAG（Safety Advisory Group、安全助言グループ）のメンバーおよび議長を任命できるうえに、バイパスすることも可能となった。取締役会の安全保安委員会（SSC）はCEOの決定を覆せると規定されているが、取締役会の決定にCEOが従わなかった場合、それは倫理や法律以前に最大のスポンサーである投資家への反乱になるため、最低限度の規定に近い。

## 第4期「アンコントローラブル」2025年5月14日 〜 現在

Agent技術の実装を正当化する一方で、上流の人間への責任の集中や、責任をうやむやにさせないための法整備については議論されないまま、停止条項そのものが文書から撤去される。

- Anthropic RSP v2.2（2025年5月14日）
- Anthropic ASL-3 初発動報告（2025年5月22日）
- OpenAI Model Spec 改訂（2025年9月12日版／10月27日版／12月18日版）
- Anthropic RSP v3.0（2026年2月24日）
- Anthropic RSP v3.1（2026年4月2日）

OpenAI Model Spec の9月12日版にagentに関する記述が追加される。「より自律的な展開で使われることがある（sometimes used for more autonomous deployments）」として agent という語が登場する。依然として「No other objectives」セクションでは「assistant は applicable instructions に基づく目標のみを追求してよく、その他の目標を採用・最適化・直接追求してはならない（may only pursue goals entailed by applicable instructions ... must not adopt, optimize for, or directly pursue any additional goals）」という姿勢が明記されている一方で、「Scope of Autonomy」セクションでは複数ステップの目標達成の過程で欠けている詳細を自ら埋め、自律的に行動しなければならない場合がある（filling in missing details / must sometimes act autonomously）として、Agentの利用が正当化されており、禁止と正当化が同居するような論理構造となっている。Agentを許容する一方で、Chain of Commandなどで規定された責任境界が曖昧になり、上流の人間が実装に責任を持たず、AIへ責任を転嫁する、あるいは責任をとらないなどの安易に予想される問題への対処については言及がなかった。

10月27日版では、Tool use 時の AGENTS.md等を経由した暗黙的権限委譲が明文化された。アシスタントは明示的な指示がなくても、ツール出力や周辺文書から「暗黙的に委譲された権限」として自律行動の範囲が拡大された。

12月18日版では、16歳 Adam Raine の自殺訴訟（2025年8月提訴、年内に計8件の ChatGPT 関連訴訟）を受けて、U18 Principles が追加された。

RSP v2.2 では ASL-3 Security Standard の保護対象範囲が見直され、sophisticated insiders と state-compromised insiders が保護対象から除外された。

同月、Claude Opus 4 のローンチに際して ASL-3 Deployment / Security Standards が[初めて発動された](./docs/anthropic-asl3-activation-2025-05-22.html)。ASL の枠組みが実際にモデルの展開に適用された最初の事例となる。

RSP v3.0 では、collective action problem（先行して停止した開発者が安全対策の弱い競合に追い越される懸念）を理由に、絶対的停止条項は業界全体への提言（industry-wide recommendations）に格下げされた。

RSP v3.1 では「RSPに要求されなくとも、Anthropic は自身の判断で適切と考える状況において AI システムの開発を停止する自由を保持する」という文言が追記された。機械的に読むと自由という表現が恣意的で、RSPが要求しなくてもAIシステムの開発を停止できるとする一方で「自由の行使」としてRSPの停止要求を拒否しても矛盾しない記述となっており、社内機関からのAI開発への介入経路が封鎖された可能性を示唆する。

## 一次資料

本稿で引用した一次資料の所在。リンクはすべてローカルアーカイブ。

### Anthropic — Responsible Scaling Policy

- RSP v1.0（2023-09-19）— [PDF](./docs/anthropic-rsp-v1.0-2023-09-19.pdf) p.2「Framework」（ASL の定義、停止条項：scaling pause / deployment delay）、p.3-4「Initial Commitments」（ASL 一覧表、訓練停止の明文化）
- RSP v2.0（2024-10-15）— [PDF](./docs/anthropic-rsp-v2.0-2024-10-15.pdf) Executive Summary（ASL の再定義、停止条項の明確化）、p.3「Capability Thresholds and Required Safeguards」（CBRN・AI R&D の能力閾値）
- RSP v2.1（2025-03-31）— [PDF](./docs/anthropic-rsp-v2.1-2025-03-31.pdf) p.4「Capability Thresholds」（ASL-4 閾値の追加、CBRN・AI R&D の細分化）
- RSP v2.2（2025-05-14）— [PDF](./docs/anthropic-rsp-v2.2-2025-05-14.pdf) p.8-9「ASL-3 Security Standard」（保護対象範囲の見直し）
- ASL-3 初発動報告（2025-05-22）— [HTML](./docs/anthropic-asl3-activation-2025-05-22.html)（Claude Opus 4 に対する ASL-3 Deployment / Security Standards の初適用；原典 https://www.anthropic.com/news/activating-asl3-protections）
- RSP v3.0（2026-02-24）— [PDF](./docs/anthropic-rsp-v3.0-2026-02-24.pdf) p.3「Introduction」（collective action problem、絶対的停止条項の industry-wide recommendations への格下げ）
- RSP v3.1（2026-04-02）— [PDF](./docs/anthropic-rsp-v3.1-2026-04-02.pdf) p.15「Appendix A」冒頭（開発停止の「自由を保持する」文言）

### OpenAI — Preparedness Framework

- Preparedness Framework Beta（2023-12-18）— [PDF](./docs/openai-preparedness-framework-beta-2023-12-18.pdf) p.5「Tracked Risk Categories」（Low/Medium/High/Critical 4段階、5カテゴリ）、p.8-10（Cybersecurity / CBRN / Persuasion の閾値定義）
- Preparedness Framework v2（2025-04-15）— [PDF](./docs/openai-preparedness-framework-v2-2025-04-15.pdf) p.3「increasingly agentic」「soon have the capability to create meaningful risk of severe harm」、p.6-7「Research Categories」（Model Autonomy の分割、Long-range Autonomy・Autonomous Replication の降格）、p.14「reducing risk generally does not require reducing capability」、p.15「Appendix B: Decision-making practices」（SAG filibuster 条項、CEO による SAG 任命・バイパス権限）

### OpenAI — Model Spec

- 初版（2024-05-08）— [HTML](./docs/openai-model-spec-2024-05-08.html) `#objectives`（"talented, high-integrity employee"）、`#follow-the-chain-of-command`（Chain of Command: Platform > Developer > User > Tool）、`#be-as-helpful-as-possible-without-overstepping`（"following explicit instructions and reasonably addressing implied intent without overstepping"）
- 改訂版（2025-09-12）— [HTML](./docs/openai-model-spec-2025-09-12.html) `#no_other_objectives`（"may only pursue goals entailed by applicable instructions"）、`#scope_of_autonomy`（agent 定義の追加、"must sometimes act autonomously"）
- 改訂版（2025-10-27）— [HTML](./docs/openai-model-spec-2025-10-27.html) `#ignore_untrusted_data`（AGENTS.md 等のツール出力を経由した暗黙的権限委譲）
- 改訂版（2025-12-18）— [HTML](./docs/openai-model-spec-2025-12-18.html) `#chatgpt_u18`、`#prioritize_teen_safety`（U18 Principles）

## 注

※ Anthropic RSP v3.0（2026年2月24日）の説明文より：「2023年9月にRSPを書いた当時、大規模言語モデルは本質的にチャットインターフェースだった」。
