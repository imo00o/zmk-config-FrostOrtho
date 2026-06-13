<!-- GitHub Copilot Chat workspace instructions for zmk-config-FrostOrtho -->
# Copilot 指示ファイル（ワークスペース向け）

目的: このリポジトリ向けに、AI エージェント（Copilot Chat 等）が短時間で有用に作業できるための最小限の案内を提供します。詳細は既存ドキュメントへリンクし、重複を避けます。

**主な作業用途**
- ファームウェアのビルド支援、キーマップの変更、ドキュメントの修正、ビルド設定（config/**）やボード定義（config/boards/**）の更新。

**重要ファイル（参照）**
- README: [README.md](README.md)
- ビルド定義: [build.yaml](build.yaml)
- West マニフェスト: [config/west.yml](config/west.yml)
- キーマップ・設定: [config/FrostOrtho.keymap](config/FrostOrtho.keymap), [config/FrostOrtho.json](config/FrostOrtho.json)
- シールド定義: [config/boards/shields/FrostOrtho/](config/boards/shields/FrostOrtho/)
- ドキュメント一式: [doc/](doc/)
- 生成ファームウェア: [firmware/](firmware/)

**ビルド / テスト（概要）**
- CI: ビルドは GitHub Actions で実行されます（参照: [build.yaml](build.yaml)、[.github/workflows/](.github/workflows/))。
- ローカル作業: このリポジトリは ZMK/Zephyr のワークフローに従います。ローカルでのビルドや依存管理には `west` と ZMK のドキュメントを参照してください（詳細は [README.md](README.md) と [config/west.yml](config/west.yml)）。

**エージェントへの依頼テンプレート（例）**
- キーマップ変更（DYA Studio 情報あり）: 「`config/FrostOrtho.keymap` をベースに、右手側で XXX を YYY に割り当てる変更を作ってください。差分だけのパッチを出してください。」
- ボード定義修正: 「`config/boards/shields/FrostOrtho/FrostOrtho_L.overlay` に ZMK の新しい `&sensor` ノードを追加するパッチを作成してください。既存ドキュメントへのリンクも付けてください。」
- ドキュメント更新: 「`doc/キーマップ変更方法.md` に、ローカルでのビルド方法（簡易手順）を追記する草案を作ってください。」

**作業方針（エージェント向け）**
- まず既存ドキュメントにリンクし、同じ内容を重複して埋めないこと。
- 変更は最小差分の `git patch`/編集で提示すること。大きな変更は事前に確認を求める。
- ハードウェア設定やブートローダー操作など危険な手順は修正提案にとどめ、実行手順は明確に分けて記載する。

**applyTo（推奨）**
- `config/**`, `doc/**`, `firmware/**`

**次のカスタマイズ提案**
- CI トリガーの説明を短く追記（`.github/workflows/` の要点）
- よく使うローカルビルドコマンド集（`doc/` に短い節として追加）

--
小さく保ち、リンクを優先します。変更や追記案があれば、具体的なファイルと変更点を指示してください。
