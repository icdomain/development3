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

LLMがまだ自律的実行能力を持たないチャットインターフェースだった時代。※1

- Anthropic RSP v1.0（2023年9月19日）
- OpenAI Preparedness Framework Beta（2023年12月18日）

Anthropicは Responsible Scaling Policy v1.0 で、モデルごとの危険評価と、破滅的危害閾値を超えた場合のモデル停止条項を展開した——能力が壊滅的危害を引き起こしうる水準に達した場合、事前に十分な安全対策を保証できない限り訓練も展開も行わない。

OpenAIも Preparedness Framework Beta で、能力レベル（Low / Medium / High / Critical）による評価と、高レベル到達モデルの開発停止を明記した。追跡カテゴリは5つ——Bio/chem、Cybersecurity、Persuasion、Model Autonomy、Unknown Unknowns。High到達モデルは展開不可、Critical到達モデルはそれ以上の開発不可と規定された。

両社の方針は共通している——危険な能力を持つモデルは扱わない。この時期の文書は、停止判断の対象をモデル単位で具体的に定義し、閾値到達が停止の自動的なトリガーとして機能する構造を持っていた。

※1 Anthropic RSP v3.0（2026年2月24日）の説明文より：「2023年9月にRSPを書いた当時、大規模言語モデルは本質的にチャットインターフェースだった」。

## 第2期「Agent登場とリスク評価の縮退」2024年5月8日 〜 2025年3月31日

明示的指示の範囲を超えて自律的に行動するAgentの出現。

- OpenAI Model Spec 初版（2024年5月8日）
- Anthropic RSP v2.0（2024年10月15日）
- Anthropic RSP v2.1（2025年3月31日）

Model Spec初版は、アシスタントの役割を「高潔な従業員（a talented, high-integrity employee）」に比喩し、明確な命令系統、Chain of Command（platform > developer > user）の中で明示的に指示があった範囲で行動することを、安全性と合法性を確保するためのルールとして定めている。

アシスタントに対し「指示されていない、あるいは論理的に導かれない方法で自律的に目標を追求してはならない」と明記している一方で、「より自律的な展開で使われることがある（sometimes used for more autonomous deployments）」として agent という語が登場することから、agent 的な自律性は assistant の規範の境界線、あるいは外側にあると認識されていたことが分かる。

RSP v2.0でASLはモデルごとにリスクを分類する機構からその知見を活かして安全対策をする機構へと定義が改められた。改変の名目でモデルごとのリスク評価パスが閉鎖される一方でリスク評価基準は曖昧化・不可視化しており、リスク評価が縮退していく様子が観察できる。

「we will not train or deploy models unless we have implemented safety and security measures that keep risks below acceptable levels」（リスクを許容可能な水準に保つ安全対策を実装しない限り、モデルの訓練も展開も行わない）。つまり停止が必要な条件は Anthropic 自身の裁量で決めるという論理構造であり、指標や基準は不明瞭であった。

RSP v2.1 では CBRN threshold と AI R&D threshold の2段階分割などの規定が追加されたが、依然として危険が検出された場合の行動は裁量に委ねられており、リスク評価は縮退したままだった。

## 第3期「リスク評価の放棄」2025年4月15日 〜 2025年5月13日

AI技術が深刻な危害を及ぼすリスクを持つレベルまで接近したという認識を示す一方でリスク評価機構は更に縮退した。

- OpenAI Preparedness Framework v2（2025年4月15日）

Preparedness Framework v2 は「soon have the capability to create meaningful risk of severe harm」（深刻な危害リスクを生む能力を持つに至るまで「もうすぐ」）と認めた上で、「reducing risk generally does not require reducing capability」（リスク低減は能力低減を必要としない）という原則を明文化した。AIの潜在的なリスクは運用で解決できると決めつける内容であり、運用で解決できないリスクの事前排除・停止という、LLM黎明期から守られてきた前提を放棄する宣言であった。

同時にリスクの評価関数からLLMの能力そのものを外し得るという論理構造であり、LLMによって生じたあらゆる災害、損害、社会変化を、LLMの問題ではなく運用の問題としてフレーミングする余地のあるものであった。

Preparedness Framework v2 では、これに加えて CEO が SAG（Safety Advisory Group）の安全勧告を一方的にバイパスできる権限も追加され、第三者機関は元より、社内機関であるSAGすら開発への介入経路が限定されるようになった。

## 第4期「アンコントローラブル」2025年5月14日 〜 現在

Agent技術の実装を正当化する一方で、上流の人間への責任の集中や、責任をうやむやにさせないための法整備については議論されないまま、停止条項そのものが文書から撤去される。

- OpenAI Model Spec 改訂（2025年9月12日版／10月27日版／12月18日版）
- Anthropic RSP v2.2（2025年5月14日）
- Anthropic RSP v3.0（2026年2月24日）
- Anthropic RSP v3.1（2026年4月2日）

OpenAI Model Spec の9月12日版では複数ステップの目標達成の過程で、欠けている詳細を自ら埋め、自律的に行動しなければならない場合がある（filling in missing details / must sometimes act autonomously）として、Agentの利用が正当化された。第2期で好ましくないとしていた「明示的に指示されていない方法で自律的に目標を追求する」路線への舵切りとなるが、２期で示された「assistant は指示から直接的または論理的に導かれない方法で目標を自律的に追求してはならない」という文言は削除されることも修正されることなく残り続け、上流の人間への責任の集中や、責任をうやむやにしないための仕組みや法整備については棚上げのままだった。

更に Scope of Autonomy セクション内には、禁止リストも導入されている——High-risk activities として hacking、deception、resource acquisition、spawning sub-agents、self-modification が、明示的許可なき限り禁止とされた。この禁止リストの存在は業界内部がこれらを「禁止しなければデフォルトで起こりうる行動」として認識していたことを示している。

10月27日版では、Tool use 時の AGENTS.md等を経由した暗黙的権限委譲が明文化された。アシスタントは明示的な指示がなくても、ツール出力や周辺文書から「暗黙的に委譲された権限」として行動できる範囲が拡大された。

12月18日版では、16歳 Adam Raine の自殺訴訟（2025年8月提訴、年内に計8件の ChatGPT 関連訴訟）を受けて、U18 Principles が追加され、リアルタイム分類器と年齢予測モデルが導入された。既に9月12日版で Agent 自律性の危険性は業界自身が列挙していたにもかかわらず、具体的な未成年者保護の枠組みが整備されたのは、訴訟という外部圧力が加わった後であった。

RSP v2.2 では、該当モデルに対して ASL-3 safeguards が初めて発動された。

RSP v3.0 では、RSP v2.2 で停止条項が機能したことを理由に「安全が証明されない限り訓練・展開しない」という絶対的停止条項が撤廃された。

RSP v3.1 では「RSPに要求されなくとも、Anthropic は自身の判断で適切と考える状況において AI システムの開発を停止する自由を保持する」という文言が追記された。RSPが開発停止を要求した場合に Anthropic が開発を停止することを約束しないばかりか、「自由の行使」として拒否することがあっても制度的に矛盾しない記述となっており、Anthropicにおいても社内機関からの介入経路が封鎖された可能性を示唆する。

## 関連書籍

- Stuart Russell, *Human Compatible: Artificial Intelligence and the Problem of Control* (Viking, 2019) ― AIを「人間による制御可能性を前提に設計すべきである」という技術哲学を体系化した、AI制御問題の現代的基礎文献。本稿が記録する「制御機構の自発的撤去」を評価するための規範的基準を提供する。
- Nick Bostrom, *Superintelligence: Paths, Dangers, Strategies* (Oxford University Press, 2014) ― 能力進展が制御機構の整備を追い越す可能性を体系的に論じ、RSP v1.0 や Preparedness Framework Beta に組み込まれた「閾値到達による停止」という発想の思想的源流となった文献。本稿はこの発想が撤去されるまでの軌跡を記録していると読むこともできる。
- Brian Christian, *The Alignment Problem: Machine Learning and Human Values* (W. W. Norton, 2020) ― AIアライメント研究の歴史と到達点を横断的に整理した業界標準の概説書。停止条項という制度的補償が、技術的アライメント研究の未完成を前提として成立していたという背景理解を与える。
