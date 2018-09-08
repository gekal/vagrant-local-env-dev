# Jekyll over virtual box at windows
(作成中)

## 前提条件

* Window/Macos
* Vagrant
* virtual box
    * [vagrant-vbguest](https://github.com/dotless-de/vagrant-vbguest)
    * [vagrant-proxyconf](https://github.com/tmatilai/vagrant-proxyconf)
    * [vagrant-teraterm](https://github.com/tiibun/vagrant-teraterm)
* Tera Term

## Jekyllって、何

プレーンテキストから静的な Web サイトやブログを生成する。

[日本語版のホームページ](https://jekyllrb-ja.github.io/)

## 環境構築

> 前提条件がクリスされること

```powershell
# 開始コマンド
vagrant up
```

## Jekyllコマンド

```bash
# 新なブログの作成
jekyll new myblog

# ビルド＋サーバー起動
jekyll serve
```

## 他の参照資料

1. SCLリポジトリー(不採用)

    > [リポジトリのリソース一覧](http://mirror.centos.org/centos/7/sclo/x86_64/)

    ```bash
    # リポジトリの追加
    yum -y install centos-release-scl-rh centos-release-scl

    # ソフトのインストール
    yum --enablerepo=centos-sclo-rh -y install rh-ruby25

    # Bashの有効化
    scl enable rh-ruby25 bash
    ```
