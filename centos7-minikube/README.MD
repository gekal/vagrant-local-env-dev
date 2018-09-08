# minikube over virtual box at windows

## 前提条件

* Window/Macos
* Vagrant
* virtual box
    * [vagrant-vbguest](https://github.com/dotless-de/vagrant-vbguest)
    * [vagrant-proxyconf](https://github.com/tmatilai/vagrant-proxyconf)
    * [vagrant-teraterm](https://github.com/tiibun/vagrant-teraterm)
* Tera Term

## 環境構築

> 前提条件がクリスされること

```powershell
# 開始コマンド
vagrant up
```

## その他
社内で利用する場合、プロキシを通すのは一般です。下記の環境変数を設定すれば、ネット周りを意識せず使えます。

```conf
http_proxy="http://username:passwd@proxyserver:8080"
```
