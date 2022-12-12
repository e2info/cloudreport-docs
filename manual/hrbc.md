---
layout: default
title: クラウドドキュメント リリースノート

---

<br>
<div align="center">
<img src="images/logo-type.png" alt="クラウドドキュメント" title="クラウドドキュメント">
</div>
<br><br>

# クラウドドキュメント PORTERS設定マニュアル

## PORTERSからクラウドドキュメントへの画面遷移

PORTERSからクラウドドキュメントを利用する場合、下記URLより遷移します。

https://cloud-document.net/hrbc/callback


### 設定手順

※PORTERSにシステム管理者権限でのログインが必要です。

1. 設定→カスタマイズの順に選択します
2. アクションメニュー編集を選択
3. アクションメニューを設定するリソースを選択します
   ![アクションメニュー／リソースの選択](images/hrbc/hrbc_actionmenu_2.png)
   
4. 隣に表示されたリストからアクションメニューを選択します<br>
5. アクションメニューを追加します<br>
   ![アクションメニュー／追加](images/hrbc/hrbc_actionmenu_3.png)<br>
   
    * 英語：任意の文字列　例：report-output
    * 日本語：任意の文字列　例：帳票出力
    * URL：URL一覧を参照
<br>

### URL一覧

旧環境と同様に、詳細設定せずアクションメニューを追加したい場合は、下記URLの【利用中のドメイン】をお使いのドメインに置き換えて設定してください。<br>

※【利用中のドメイン】について
　(例)https://e2info.cloud-document.net →利用中のドメインは　e2info の部分です。

|リソース|URL|
|-----|-----|
|企業|https://【利用中のドメイン】.cloud-document.net/report/client/\{\{Client.P_Id\}\}?user=\{\{Session.P_UserId\}\}|
|企業担当者|https://【利用中のドメイン】.cloud-document.net/report/recruiter/\{\{Recruiter.P_Id\}\}?user=\{\{Session.P_UserId\}\}|
|JOB|https://【利用中のドメイン】.cloud-document.net/report/job/\{\{Job.P_Id\}\}?user=\{\{Session.P_UserId\}\}|
|個人連絡先|https://【利用中のドメイン】.cloud-document.net/report/candidate/\{\{Person.P_Id\}\}?user=\{\{Session.P_UserId\}\}|
|レジュメ|https://【利用中のドメイン】.cloud-document.net/report/resume/\{\{Resume.P_Id\}\}?user=\{\{Session.P_UserId\}\}|
|売上|https://【利用中のドメイン】.cloud-document.net/report/sales/\{\{Sales.P_Id\}\}?user=\{\{Session.P_UserId\}\}|
|アクティビティ|https://【利用中のドメイン】.cloud-document.net/report/activity/\{\{Activity.P_Id\}\}?user=\{\{Session.P_UserId\}\}|
|選考プロセス|https://【利用中のドメイン】.cloud-document.net/report/process/\{\{Process.P_Id\}\}?user=\{\{Session.P_UserId\}\}|


### 新機能
クラウドドキュメント上の左側のメニュー「PORTERS設定」の「PORTERS側の設定」
<img src="images/hrbc/hrbc_actionmenu_4.png" width="400px">

「アクションメニュー設定用URL（帳票の種類：通常）」の
URLをコピーして設定いただくと、より詳細な設定が可能になります。
![PORTERS側の設定](images/hrbc/hrbc_actionmenu_5.png)<br><br>

ID・テンプレートが可または不可、初期値が指定有りまたは無し　でURLが異なります。<br>
どのURLを入れるかによりアクションボタン押下で帳票出力画面に遷移後の表示が異なります。<br>
くわしくは[こちら](https://e2info.github.io/cloudreport-docs/manual/admin.html#dl_sp_2)をご確認ください。<br>

<br><br>

上記設定を終えますと
PORTERSに設定いただいたアクションメニューからクラウドドキュメントに遷移し、出力が可能となります。

![アクションメニュー例](images/hrbc/hrbc_actionmenu_1.png)
-----
* 2020年12月25日新規作成
* 2022年12月12日更新

{% include footer.md %}
