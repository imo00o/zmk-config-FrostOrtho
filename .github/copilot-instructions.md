<!-- GitHub Copilot / Agent instructions for the FrostOrtho ZMK workspace -->
# FrostOrtho — Agent Instructions

目的: このリポジトリで作業するAIエージェントが、素早く安全に支援できるよう最小限の指示と参照をまとめます。詳細はリポジトリ内の関連ドキュメントにリンクして参照してください（埋め込みは行いません）。

**重要ファイル（素早く参照）**
- **ビルド設定**: [build.yaml](build.yaml)
- **ボード/シールド定義**: [config/boards/shields/FrostOrtho/](config/boards/shields/FrostOrtho/)
- **キーマップ**: [config/FrostOrtho.keymap](config/FrostOrtho.keymap)
- **カスタムモジュール定義**: [zephyr/module.yml](zephyr/module.yml)
- **ドキュメント（日本語）**: [doc/](doc/)
- **配布済ファームウェア（UF2）**: [firmware/](firmware/)

**ZMK 参照**
- リポジトリで使用している ZMK v0.3 系の要点とリンクは [doc/ZMK_REFERENCE_v0.3.md](doc/ZMK_REFERENCE_v0.3.md) を参照してください。ファームウェアやキーマップを変更する際は、このファイルと v0.3 ドキュメントを必ず参照するようにしてください。

**リポジトリ上の慣習（要点）**
- 左右分割で FrostOrtho_L / FrostOrtho_R を用いる。
- カスタムZMKフォーク／モジュールが含まれるため、公式ドキュメントとの差分に注意する。
- キーマップはレイヤー/hold-tap/マクロを多用する（調整時は `config/FrostOrtho.keymap` を参照）。

**よくある環境注意点**
- フラッシュ失敗時は `settings_reset-seeeduino_xiao_ble-zmk.uf2` を使ったリセットが有効な場合がある（詳細は [doc/キーマップ変更方法.md](doc/%E3%82%AD%E3%83%BC%E3%83%9E%E3%83%83%E3%83%97%E5%A4%89%E6%9B%B4%E6%96%B9%E6%B3%95.md) を参照）。
- CIはGitHub Actionsと `build.yaml` を利用する。ローカルビルドは west/Zephyr 環境が前提。

**ローカルでの基本コマンド（例）**
```bash
# リポジトリルートでのビルド例（環境によって調整）
west build -b seeeduino_xiao_ble -s .

# ビルド済みUF2をデバイスに書き込む: ブートローダーに入れてUF2をコピー
# プラットフォームによって手順が異なるため、詳細は doc/ を参照
```

**エージェントへの指示テンプレ（例）**
- キーマップのレイヤー3にCapsLock相当の動作を追加したい。どのファイルを編集すれば良いかと修正例を示して。
- 左ボードが接続されない問題がある。まず確認すべきハード/ソフト項目を順に挙げて。
- 新しいトラックボールモジュールを追加したい。既存のモジュール依存と必要な変更箇所を教えて。

**applyTo（推奨）**
- config/**
- doc/**
- zephyr/**

変更や大きな修正は「候補の差分（patch）」で提案してください。自動でコミットする前にレビューを行います。

---
このファイルはブートストラップです。必要に応じて、テスト手順やCI運用ルールなどのセクションを追加します。
