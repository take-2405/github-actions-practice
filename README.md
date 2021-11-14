[![Go](https://github.com/take-2405/github-actions-practice/actions/workflows/go-test.yml/badge.svg)](https://github.com/take-2405/github-actions-practice/actions/workflows/go-test.yml)

# github-actions-practice

## リポジトリ概要
CICD(今回はGithub actionsを利用)について学ぶためのリポジトリ  
今回は過去に作ったRESTAPIのコードを持ってきて簡単なCICDを構築した  
(RESTAPIの使用はdocs/api.mdに記載)

### 実行方法
※実行にはdockerとgoの環境が必要(そのうちdocker images化するかも)  

1. リポジトリをクローン  
2. make compose-build  
3. make run  
4. make compose-cleean  
4はDBを削除するコマンドのため作業終了時に使用してください。


## 知識   
詳しくは今後Qiitaでまとめる予定 
 
##### 用語  
- CI；継続的インテグレーション、開発者向けの自動化プロセス。新しいコード変更を定期的にビルド、テストする。
- CD：CIが完了した後の継続的デリバリー（継続的デプロイメント）のことを指す
- CI/CDパイプライン：モニタリングと自動化を導入し、特に統合とテストのフェーズ、および配信とデプロイの段階で、アプリケーション開発のプロセスを向上させる。

##### パイプラインステージ  
- ビルド:アプリケーションがコンパイルされるステージ
- テスト:コードがテストされるステージ
- リリース:アプリケーションがリポジトリに配信されるステージ
- デプロイ:コードがプロダクションにデプロイされるステージ
- 検証とコンプライアンス:ビルドを検証するためのステップは、組織のニーズによって決まります。Clair などのイメージセキュリティスキャンツールは、既知の脆弱性 (CVE) と比較することでイメージの品質を確保します

#### 代表的なCICDツール
- Jenkins
- CircleCI

### 参考サイト  
https://www.redhat.com/ja/topics/devops/what-cicd-pipeline