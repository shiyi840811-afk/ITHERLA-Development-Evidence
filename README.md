# ITHERLA Development Evidence｜開發證據

Public development-evidence ledger for ITHERLA, a player-facing AI Agent product under active development.

This repository publishes high-level product and technical concepts, milestone summaries, and cryptographic identifiers. It does not contain source code, private datasets, credentials, executable packages, proprietary algorithms, or complete architecture details.

這裡是 ITHERLA 的公開開發證據庫。ITHERLA 是一款開發中的玩家用 AI Agent 產品。

本庫公開產品與技術概念、里程碑摘要及雜湊識別碼，不包含原始碼、私人資料集、憑證、可執行安裝包、專有演算法或完整架構細節。

## Product Concept and Progress｜產品概念與開發進度

- [English | Product Concept and Development Progress](docs/PRODUCT_PROGRESS.en.md)
- [English | Public Technical Concepts](docs/TECHNICAL_CONCEPTS.en.md)

The progress pages track product direction, maturity, and dated milestones. The companion concept pages explain design choices without disclosing implementation details.

- [繁體中文｜產品概念與開發進度](docs/PRODUCT_PROGRESS.zh-TW.md)
- [繁體中文｜公開技術概念](docs/TECHNICAL_CONCEPTS.zh-TW.md)

進度頁記錄產品方向、開發成熟度與各里程碑日期；技術概念頁解釋設計取捨，不公開實作細節。

## Product Direction｜產品方向

ITHERLA is intended to let an authorized AI Agent observe and participate in supported games while preserving identity and governed memory across replaceable local, cloud, and hybrid model engines. Models do not own memory, authorization, or tool authority. Game actions must remain inside product-specific capability, consent, platform, anti-cheat, privacy, and safety boundaries.

ITHERLA 的目標是讓經使用者授權的 AI Agent 觀察並參與支援的遊戲。即使切換本地、雲端或混合模式的模型引擎，同一 Agent 的身分與受治理記憶仍可延續。模型本身不持有記憶、授權或工具操作權；遊戲操作必須遵守產品能力範圍、使用者同意、平台規範、反作弊、隱私與安全限制。

## Current Maturity｜目前開發狀態

The current line contains an isolated cognitive-core prototype and its contracts and tests. It is not yet a finished player product. Player-facing UI, real model integration, NVIDIA OpenShell integration, game adapters, virtual input, installer lifecycle, and public release qualification remain incomplete or disabled unless a later evidence record explicitly shows otherwise.

目前已建立隔離的認知核心原型，以及對應的契約與測試，尚不是完整的玩家產品。玩家介面、實際模型接線、NVIDIA OpenShell 整合、遊戲介接、虛擬輸入、安裝與更新流程，以及公開發行驗收，仍未完成或未啟用，除非後續的證據紀錄另有明確說明。

## Evidence Method｜開發證據如何留存

Each milestone record binds a privately retained complete Git bundle, tracked-source snapshot, validation output, Git HEAD and tree identifiers, and SHA-256 manifest. The private artifacts stay on the development machine and are not uploaded to this ledger.

These records support development continuity and later comparison. They do not independently prove authorship, originality, legal compliance, product safety, commercial readiness, or an immutable trusted timestamp.

每筆里程碑紀錄都對應一份私下保留的完整 Git 備份、受 Git 追蹤的原始碼快照、驗證輸出、Git HEAD 與檔案樹識別碼，以及 SHA-256 清單。這些非公開資料留在開發機，不上傳到本證據庫。

這些紀錄便於延續開發與日後比對，不能單獨證明作者身分、原創性、法規遵循、產品安全、商用就緒程度，也不等於不可篡改的可信時間戳。

## Partnerships and Sponsorship｜合作與贊助聯繫

For development sponsorship, strategic partnerships, research collaboration, or early product discussions, contact [itherla.project@gmail.com](mailto:itherla.project@gmail.com).

Please include a brief overview in your first email and leave out confidential information. If we need to exchange confidential material, we can first agree on how to share and protect it.

開發贊助、策略合作、研究交流或早期產品合作洽詢，請聯絡 [itherla.project@gmail.com](mailto:itherla.project@gmail.com)。

初次來信簡單說明來意即可，請勿附上機密資料。如需交換機密資料，可先約定傳送方式與保密條件。

## Repository Boundaries｜公開範圍與使用限制

- [Copyright, brand, and use notice](COPYRIGHT_AND_USE.md)
- [Contribution policy](CONTRIBUTING.md)
- [Security reporting scope](SECURITY.md)
- [Public-release readiness record](PUBLICATION_READINESS.md)

Public visibility is not an open-source license. Unless a file states otherwise, all rights are reserved. The ITHERLA name, visual identity, product concepts, and unpublished implementation are not licensed for commercial reuse by this repository.

This repository is a limited public record, not the product distribution channel. It accepts no source-code, model, dataset, prompt, architecture, or executable contributions at this stage.

- [著作權、品牌與使用說明](COPYRIGHT_AND_USE.md)
- [貢獻政策](CONTRIBUTING.md)
- [資安通報範圍](SECURITY.md)
- [公開發行準備紀錄](PUBLICATION_READINESS.md)

公開可見不等於開源授權。除非個別檔案另有說明，均保留所有權利。本庫不授權將 ITHERLA 名稱、視覺識別、產品概念或未公開實作用於商業再利用。

這裡是有限範圍的公開紀錄，不是產品下載管道。現階段不接受原始碼、模型、資料集、提示詞、架構或可執行檔的投稿。
