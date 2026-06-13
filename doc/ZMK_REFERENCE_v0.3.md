# ZMK Reference (v0.3 branch)

このリポジトリで使用されている ZMK の参照集（v0.3 系）です。

## リポジトリ内のバージョン情報
- `config/west.yml` で `zmk` は `remote: cormoran`、`revision: v0.3-branch+dya` を参照しています。

## 公式ドキュメント（v0.3 ブランチ）
- v0.3 ドキュメント（推奨参照先）: https://v0-3-branch.zmk.dev/docs/
- 一般ドキュメント: https://zmk.dev/docs/

## フォーク / ソースコード
- このリポジトリは `cormoran/zmk` フォークを利用しています: https://github.com/cormoran/zmk
- フォークは公式 `zmkfirmware/zmk` の v0.3 系をベースにカスタム変更を含みます。

## 重要トピック（作業時に必ず参照）
- ビルド手順（Zephyr/west のセットアップと `west build` の使い方） — v0.3 ドキュメントの "Getting Started" と "Building" セクションを参照。
- キーマップ構成と `behavior` — `config/FrostOrtho.keymap` とドキュメントの "Keymap", "Behaviors" を照合。
- ボード/シールド定義 — `config/boards/shields/FrostOrtho/` 内の overlay と DTSI の差分に注意。
- カスタムモジュール/依存 — `config/west.yml` に列挙されたモジュール（`zmk-module-*` 等）の README を確認。

## よくある手順（短縮メモ）
```bash
# リポジトリルートでビルド（例）
west build -b seeeduino_xiao_ble -s .

# フラッシュ済みUF2でリセットが必要な場合
# settings_reset-seeeduino_xiao_ble-zmk.uf2 をデバイスに適用
```

## エージェント向け指示（要約）
- ファームウェアやキーマップを変更する前に、本ファイルと v0.3 ドキュメントを参照すること。
- `config/west.yml` に記載された各モジュールのリビジョン差分を確認し、互換性が必要な場合は該当モジュールの README / CHANGELOG を参照。
- 主要な参照先は上の公式ドキュメント URL と `cormoran/zmk` リポジトリ。

---
このファイルは参照用の要約です。必要であれば、特定トピック（keymap, behaviors, build）の抜粋を追加してローカルに保存します。
