# Docker over virtual box at windows

## 参照資料

1. SCLリポジトリー

    > [リポジトリのリソース一覧](http://mirror.centos.org/centos/7/sclo/x86_64/)

    ```bash
    # リポジトリの追加
    yum -y install centos-release-scl-rh centos-release-scl

    # ソフトのインストール
    yum --enablerepo=centos-sclo-rh -y install rh-ruby25

    # Bashの有効化
    scl enable rh-ruby25 bash
    ```
