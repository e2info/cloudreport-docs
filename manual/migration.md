---
layout: default
title: クラウドドキュメント リリースノート

---

<br>
<div align="center">
<img src="images/logo-type.png" alt="クラウドドキュメント" title="クラウドドキュメント">
</div>
<br><br>

# クラウドドキュメント 新環境への移行手順


### 移行期間

#### 2022年1月4日(水)〜2023年6月30日(金)まで
<span style="color: red; ">※2023年7月1日(土)より旧環境はご利用いただけなくなります。</span>


上記期間中に新環境への移行を開始〜完了させてください。<br>
利用開始日〜翌月末までが1環境毎の個別の移行期間となり、利用開始日〜翌月末までの新環境での出力分については<br>
新環境での出力テストを想定しご請求対象外となります。<br>
詳しくは[移行期間の出力分について](#1)をご確認ください。<br>

本番環境の他にテスト環境のご利用がある場合にはそれぞれで移行作業が必要となります。<br>
<span style="color: red; ">※その際お申し込みのメールアドレスを本番と検証で別のアドレスにてお申し込みをお願いします。</span><br>
<span style="color: red; ">このメールアドレスは重要なご案内等をお送りする予定ですので、必ずご確認可能なアドレスの設定をお願いいたします。</span><br><br>


### 1.新環境での利用開始

PORTERSに管理者としてログイン後、下記の開始用URLにアクセスいただき、新環境の利用を開始してください。<br><br>
__利用開始URLはこちら__<br>
<span style="color: red; ">※お手数ですが誤操作防止のため下記をコピーして別ウィンドウでアクセスしてください。</span><br>
https://cloud-document.net/hrbc/callback?subscribe

<br>
<img src="images/migration/migration1.png" width="600" alt="利用規約" title="利用規約"><br>

クラウドドキュメント 利用規約をご確認後<br>
問題なければ<br>
・法人名<br>
・法人名フリガナ<br>
・ご担当者名<br>
・メールアドレス<br>
上記をご記入いただき、「利用規約に同意して利用開始する」ボタンを押下してください。<br><br>


その後、__「PORTERS HR-Business Cloud-リソースへのアクセス権の承認」__ という画面が表示されます。<br>
<img src="images/migration/migration2.png" width="400" alt="リソースへのアクセス権の承認" title="リソースへのアクセス権の承認"><br>

御社PORTERSのデータへのアクセス権をクラウドドキュメントに承諾いただくことでPORTERSと連携可能になります。<br>
ご利用開始されますと、弊社に通知が来るためその通知を持って利用開始日といたします。<br>
__利用開始時点ではトライアル期間は２週間となりますが、確認取れ次第弊社側で翌月末までの期限延長いたします。__<br><br>


### 2.マニュアルに沿ってPORTERSの設定を行う

①下記のマニュアルを参考にPORTERS側の設定をお願いいたします。<br>
※旧環境利用開始時に設定いただいた内容とほぼ同じ内容での作業となります。<br>
* [PORTERS設定マニュアル](manual/hrbc.md)

<br>
②PORTERSとの同期を行う<br>
(PORTERSフィールドの同期、選択肢の取得、ユーザーの同期)<br>

* [管理者マニュアル](manual/admin.html#porters)

<br><br>


### 3.新環境へのテンプレート設定

①旧環境から各テンプレートをダウンロードします<br>
帳票一覧から該当の帳票の「更新」　を押下します<br>
<img src="images/migration/migration3.png" width="600" alt="帳票一覧" title="帳票一覧"><br>
<br>
②帳票更新画面のテンプレート「現在の帳票テンプレート」　を押下いただくとダウンロードできます
<br>

<img src="images/migration/migration4.png" width="600" alt="帳票ダウンロード" title="帳票ダウンロード"><br>
<br>

③旧環境から各テンプレートに設定されたマッピング情報をエクスポートします
帳票一覧から該当の帳票の「マッピング」を押下します

<br>
<img src="images/migration/migration5.png" width="600" alt="帳票一覧" title="帳票一覧"><br>
<br>

「インポート/エクスポート」を押下します
<br>
<img src="images/migration/migration6.png" width="600" alt="インポート/エクスポート" title="インポート/エクスポート"><br>
<br>

「エクスポート」を押下いただくと、マッピング情報がエクセルファイル形式でダウンロードされます。
<br>
<img src="images/migration/migration7.png" width="600" alt="エクスポート" title="エクスポート"><br>
<br>


④旧環境からダウンロードした帳票とマッピング情報を新環境に設定します<br>
旧環境と同様に、新環境に帳票を新規作成し、先ほどダウンロードしたテンプレートを設定します。<br>
「インポート/エクスポート」を押下します
<br>
<img src="images/migration/migration6.png" width="600" alt="インポート/エクスポート" title="インポート/エクスポート"><br>
<br>
「インポート」部分で先ほどエクスポートしたマッピング情報のエクセルをアップロードいただき確認画面へ・設定を完了してください.
<br>
<img src="images/migration/migration8.png" width="600" alt="インポート" title="インポート"><br>
<br>


<h2 id="1"></h2>

### 移行期間の出力分について

新環境利用開始月の翌月末までの新環境での出力分は新環境での出力テストを想定しご請求対象外とします。<br>
__※旧環境の出力分はご請求対象となります。__<br><br>

利用開始３ヶ月目以降は旧環境・新環境での出力分はすべてご請求対象となります。<br>

__※利用開始日が月の途中でも、１ヶ月としてカウントいたします。__<br>
　そのため月の初旬に新環境での利用開始対応されることをお勧めいたします。<br>
（例:2023年1月15日に新環境を利用開始でも、2023年1月31日開始でも、利用開始を1月とし、2023年2月末までの出力分が対象です)<br><br>

●例<br>
2023年1月4日から利用開始した場合<br>
2023年1月4日〜2月28日<br>
・新環境での出力は請求対象外<br>
・旧環境での出力は請求対象<br>
2023年3月1日〜<br>
・新環境と旧環境の出力すべてが請求対象<br><br><br>


### よくある質問
Q.旧環境と新環境でどちらが新環境かわからなくなってしまいました
A.見分け方は下記の通りです。

#### 新環境<br>
URLが<br>
https://【利用中のドメイン】.cloud-document.net/
<br>
左上のアイコンが新英語名称のCloud Document<br>
<img src="images/migration/migration10.png" width="400" alt="Cloud Document" title="Cloud Document"><br>


#### 旧環境<br>
URLが<br>
https://【利用中のドメイン】.report-cloud.com/
<br>
左上のアイコンが旧英語名称のReport cloud<br>
<img src="images/migration/migration9.png" width="400" alt="Report cloud" title="Report cloud"><br>

<br><br>
### 不明な点のお問い合わせ<br>
クラウドドキュメント上の左側のメニュー「お問い合わせ」よりお願いいたします。<br>
(平日9:00-17:00で順次対応いたします)<br><br>

-----<br>
* 2022年12月26日新規作成<br>

{% include footer.md %}
