# 環境設定手順書（Mac Book)

* PC買ったらまずはXcodeをインストールします。
* インストール後は一回起動してAgreeはしておくこと

* 2段階目は、HomeBrewをインストールすること
    * http://brew.sh/index_ja.html にアクセス
    * インストール方法に記載されているコマンドを叩く 
    * `brew doctor`を実行して使えることを確認する

* Ansibleをインストール
```
brew install ansible
```
* SSHのキーを生成します
    * [ ] `ssh-keygen -t rsa` の実施（Enterを3回）
    * [ ] `cat ~/.ssh/id_rsa.pub | pbcopy` でクリップボードに公開鍵をコピーする
        * [ ] コマンドを使うのはコピペミスを防ぐためです
* 出来上がったSSHキーをGitHubに登録する
* 実行する
```
ansible-playbook -i hosts -vv localhost.yml
```

sample.memo
