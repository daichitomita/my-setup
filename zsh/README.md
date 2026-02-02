# Zsh セットアップ

ローカルマシンのzsh環境を構築するための手順書です。

## 前提条件

- zshがインストールされていること
- curlまたはgitが利用可能であること

## Zinit のインストール

Zinitは高速で柔軟なZshプラグインマネージャーです。

https://github.com/zdharma-continuum/zinit

## Homebrew のインストール

HomebrewはmacOSやLinuxでパッケージを管理するためのツールです。

https://brew.sh/ja/

## .zprofile、.zshrcの設定

このディレクトリ内にある'.zprofile'と'.zshrc'をコピーして使ってOKです。

既存の設定がある場合は適宜調整してください。

## 解説

### Zinit Annexes（拡張機能）

Zinitの機能を拡張するアネックスを読み込んでいます：

| Annex | 説明 |
|-------|------|
| zinit-annex-as-monitor | ファイルの変更を監視し、変更時にコマンドを実行 |
| zinit-annex-bin-gem-node | バイナリ、Ruby gems、Node.jsパッケージの管理 |
| zinit-annex-patch-dl | プラグインにパッチを適用可能にする |
| zinit-annex-rust | Rustパッケージ（cargo）のインストールサポート |

### プラグイン

| プラグイン | 説明 |
|-----------|------|
| history-search-multi-word | `Ctrl+R` で複数キーワードによる履歴検索が可能に |
| zsh-autosuggestions | 過去の履歴から入力候補をグレー表示で提案 |
| fast-syntax-highlighting | コマンドラインのシンタックスハイライト |

### テーマ

**Starship** を使用しています。Rust製の高速でカスタマイズ可能なプロンプトです。

https://starship.rs/

Zinitが自動でバイナリをダウンロードし、初期化スクリプトと補完を生成します。

### 補完

`compinit` を有効化し、Zshの強力な補完機能を利用できるようにしています。
