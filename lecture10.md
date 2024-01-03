# 課題10について
## CloudFormation を利用して、現在までに作った環境をコード化する。  
## コード化ができたら実行してみて、環境が自動で作られることを確認する。

### スタック作成
- VPC、セキュリティグループ、EC2、ALB、RDS、IAM、S3毎にテンプレートを作成した。  
- 上記記述の順で実行した。  
![stack](img10/stack.png)  

### 実行結果
- VPC  
![vpc](img10/vpc.png)  
- EC2用のセキュリティーグループ  
![EC2-SG-in](img10/EC2-SG-in.png)  
![EC2-SG-out](img10/EC2-SG-out.png)  
- ALB用のセキュリティーグループ  
![ALB-SG-in](img10/ALB-SG-in.png)  
![ALB-SG-out](img10/ALB-SG-out.png)  
- RDS用のセキュリティーグループ  
![RDS-SG-in](img10/RDS-SG-in.png)  
![RDS-SG-out](img10/RDS-SG-out.png)  
- EC2  
![EC2-1](img10/EC2-1.png)  
![EC2-2](img10/EC2-2.png)  
- ALB  
![ALB](img10/ALB.png)
- RDS  
![RDS](img10/RDS.png)  
- IAM  
![IAM](img10/IAM.png)  
- S3  
![S3](img10/S3.png)  

### 感想
- テンプレートを作成する際はコンソールの設定画面を見ながらすることによって理解が深まった。
- IAMのテンプレートを実行後、EC2にどのようにIAMロールを付与すればいいか時間がかかった。  
  EC2のテンプレートにIAMロールの設定を追記して更新したら出来た。本来は最初にEC2のテンプレートを実行する前にIAMのテンプレートを実行するのが望ましいと感じた。
  しかし、更新の方法が勉強になったのでよかった。
- インデントが正しくないとエラーになってしまうので、VScodeにindent-rainbowをインストールして対応した。