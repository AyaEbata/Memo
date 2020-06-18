# Linuxコマンドメモ
ほんとマジでいつも忘れるんだわw  
ぐぐるワードは頭で浮かぶからググれば済むけど、まとめておいたらちょっとは楽になるかなって思って、まとめてみたメモ。

## ec2にssh
ユーザ名は`ec2-user`  
（と言うかconfigに書け）

```shell
$ chmod 400 hoge.pem
$ ssh -i hoge.pem ec2-user@<IPアドレス>
```

## sshでポートフォワード
`8001:localhost:8001`は`<自分のパソコンのポート>:<リモートサーバのIPアドレスとポート>`

```shell
$ ssh -i hoge.pem -L 8080:localhost:8080 <ユーザ名>@<IPアドレス>
```
