# EC2 にSSH接続する

## 前提条件
- AWSアカウントを持っていること
- EC2インスタンスが起動していること
- セキュリティグループでSSHポート（22）が開放されていること

## 接続コマンド

* バージニア北部リージョン
    * ssh -i "c:/users/den2k/.ssh/?????????.pem" ubuntu@ec2-35-153-231-144.compute-1.amazonaws.com
* 東京リージョン
    * ssh -i "c:/users/den2k/.ssh/?????????.pem" ubuntu@ec2-43-207-229-2.ap-northeast-1.compute.amazonaws.com

## 接続手順
1. ターミナルまたはコマンドプロンプトを開く
2. 上記の接続コマンドを入力して実行
3. 初回接続時は、ホストキーの確認メッセージが表示されるので、「yes」と入力

## リージョン
バージニア北部　us-east-1

## 注意事項
- .pemファイルのパーミッションは400に設定してください（Linuxの場合）
- IPアドレスは変更される可能性があるため、EC2インスタンスの再起動後は確認が必要です
- セキュリティのため、不要な時はEC2インスタンスを停止することをおすすめします

## トラブルシューティング
接続できない場合は以下を確認してください：
- EC2インスタンスが起動しているか
- セキュリティグループの設定
- .pemファイルのパスと権限
- ネットワーク接続
