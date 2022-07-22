---
layout: default
title: クラウドドキュメント リリースノート

---
<br>
<div align="center">
<img src="images/logo-type.png" alt="クラウドドキュメント" title="クラウドドキュメント">
</div>
<br><br>

# クラウドドキュメント 作成マニュアル（標準ユーザー用）

<h2 id="TOP">目次</h2>

- [はじめに](#introduction)
  - [クラウドドキュメントの動作保証環境について](#os) 
  - [主なフローについて](#flow)
  - [クラウドドキュメントのログインについて](#login)
  - [帳票のご利用料金について](#price)
- [1.PORTERSからクラウドドキュメントをダウンロードする](#porters_dl)
  - [1-1.クラウドドキュメントを1件ダウンロードする](#porters_dl_1)
  - [1-2.クラウドドキュメントを一括ダウンロードする](#porters_dl_2)
- [2.クラウドドキュメントから成約IDを入力して ダウンロードする](#dl)
  - [2-1.「ダウンロード」からクラウドドキュメントを出力する](#dl_1)
  - [2-2.「一括ダウンロード」からクラウドドキュメントを出力する](#dl_2)
  - [2-3.「出力履歴」からクラウドドキュメントを出力する](#dl_3)
- [3.台帳(一覧表)をダウンロードする](#dl_ledger)
  - [3-1.出力](#dl_ledger_1)
- [4.特定の帳票を設定したアクションボタンについて](#dl_sp)

 
<h2 id="introduction">はじめに</h2>

<h3 id="os">クラウドドキュメントの動作環境について</h3>
PORTERSに準じ、動作環境を設定しています。

[クラウドドキュメント よくある質問 「クラウドドキュメントの動作環境はどちらになりますか？」](https://e2info.github.io/cloudreport-docs/faq/faq.html#about1)でご確認ください。
<br><br>

<h3 id="flow">フローについて</h3>

<br>
<div align="center">
<img src="images/hrbc_sync/flow_user.png" width="600" alt="フロー" title="フロー">
</div>
<br><br>

#### ダウンロード（管理者/標準ユーザー共通で利用可能）

帳票テンプレートを使用しPORTERSにダウンロードします。<br>
※管理者のみ直接PCへのダウンロードが可能です。<br>
※PORTERSへダウンロードするには事前にPORTERSの同期や帳票テンプレートの作成、設定が必要となり、<br>この作業は管理者のみ対応可能です。<br>
管理者の方の手順については管理者用マニュアルにてご確認ください。<br>
 
[クラウドドキュメント 作成マニュアル（管理者用）はこちら](https://e2info.github.io/cloudreport-docs/manual/admin.html)
<br><br>

<h3 id="login">クラウドドキュメントのログインについて</h3>
クラウドドキュメントのご利用には一度PORTERSを経由してログインする必要があります。<br>
お知らせしたクラウドドキュメントURLにアクセスいただき、PORTERSのログインを経てご使用いただけます。

<br><br>

<h3 id="price">帳票のご利用料金について</h3>

#### 本番環境にて出力した帳票全てが課金対象となります。(トライアル期間・テスト環境での利用を除く)

(1) 課金のタイミングについて<br>
「ダウンロード」ボタンを押すと１帳票分課金となります。<br>
その後遷移する画面にて「PORTERSに保存する」のPDFやExcelのダウンロードボタンを押しても課金されません。

![課金のタイミングについて](images/price3.png)

(2) 出力枚数の確認について<br>
クラウドドキュメントのメニュー 利用状況 統計に各月における各帳票の出力枚数の確認ができます。

![出力枚数の確認について](images/price2.png)


<br><br>

[▲TOPに戻る](#TOP)
<br><br><br>


<h2 id="porters_dl">1.PORTERSからクラウドドキュメントをダウンロードする</h2>

#### 【ご注意ください】本番環境にて出力した帳票すべてが課金対象になります(トライアル期間内、テスト環境での利用を除く)<br>詳細は[帳票のご利用料金について](#price)をご確認ください。　<br>
#### ※マクロを使用したテンプレート(xlms形式)は出力について注意点がございます。　<br>詳細は[よくある質問 Q.テンプレートにマクロは使用できますか？ ](https://e2info.github.io/cloudreport-docs/faq/faq.html#template3)でご確認ください。

<h3 id="porters_dl_1">1-1.クラウドドキュメントを1件ダウンロードする</h3>
(1) PORTERS画面左上のタブで「成約」または「売上」を選択し、ドロップダウンから「すべての成約」または「すべての売上」を選択すると一覧が表示されます。

![成約一覧](images/hrbc_dl/hrbc_dl_1.png)

(2) クラウドドキュメントを作成したいPORTERSデータのIDをクリックします
![PORTERSデータのIDをクリック](images/hrbc_dl/hrbc_dl_2.png)

(3) 左上のタブで「クラウド帳票(本番)」を選択し、ダウンロード画面に切り替えます。

※検証環境がある場合、検証環境でダウンロードしたい場合は「クラウド帳票(検証)」を選択します。
![ダウンロード画面](images/hrbc_dl/hrbc_dl_3.png)

<h3 id="porters_dl_1_4"></h3>
(4) ダウンロード画面のSales ID欄に表示されているIDが正しいことを確認し、
テンプレートのドロップダウンから利用したいテンプレート名称を選択します。

![テンプレート名称を選択](images/hrbc_dl/hrbc_dl_user1.png)

(5)「ダウンロードする」ボタンを押下すると、帳票ダウンロード画面に切り替わります。
![帳票ダウンロード画面](images/hrbc_dl/hrbc_dl_user2.png)

<br><br>

アクション＝ 「PORTERSに保存する」
#### ※マクロを使用したテンプレート(xlms形式)はPORTERSに保存できません。

(1)「PORTERSに保存する」の右側にあるEXCEL/PDFのボタンを押下します。
![EXCEL/PDFのボタン](images/hrbc_dl/hrbc_dl_user3.png)

(2)上部に「PORTERSにファイルを添付しました。」という緑色の帯が表示されたら「PORTERSを開く」をクリックします。
![「PORTERSを開く」](images/hrbc_dl/hrbc_dl_user4.png)

(3)PORTERS画面に切り替わり、「成約」ウィンドウが表示されます。「サブリスト｜ 添付ファイル」でダウンロードしたEXCEL/PDFファイルが確認できます。
  
![EXCEL/PDFファイルを確認](images/hrbc_dl/hrbc_dl_11.png)

<br><br>

<h3 id="porters_dl_2">1-2.クラウドドキュメントを一括ダウンロードする</h3>

まずPORTERSの設定から行います。<br>
※PORTERSの設定は管理者の方のみ設定可能です。<br>
(1)PORTERSの「カスタマイズ」ページに入り<br>
<br>
<img src="images/hrbc_dl/hrbc_dl_33.png" width="300"><br><br>
アクションメニュー→レジュメ or 売上　or JOBを選択→一括アクションを選択します。<br>
新規の項目を作成します。<br>
<img src="images/hrbc_dl/hrbc_dl_34.png" width="500">

(2)項目名は任意で設定してください。<br>
　URLは下記の通り、【ご利用中のドメイン】にはご利用中のドメインを置き換えて設定してください。<br>
 (例)https://e2info.cloud-document.net →利用中のドメインは　e2info の部分です。<br>
 <img src="images/hrbc_dl/hrbc_dl_35.png" width="500"><br>
<br>
売上<br>
https://【ご利用中のドメイン】.cloud-document.net/report/multiple/sales/\{\{Sales.P_Id\}\}?user=\{\{Session.P_UserId\}\}
<br>
レジュメ<br>
https://【ご利用中のドメイン】.cloud-document.net/report/multiple/resume/\{\{Resume.P_Id\}\}?user=\{\{Session.P_UserId\}\}
<br>
JOB<br>
https://【ご利用中のドメイン】.cloud-document.net/report/multiple/job/\{\{ob.P_Id\}\}?user=\{\{Session.P_UserId\}\}
<br>

(3)PORTERSの各階層で、出力したいIDにチェックを入れて、先ほど設定したアクションメニューを選択します。<br>
もしくはページに表示されている全件のIDの出力を希望の場合はチェックを入れる必要はありません。<br>
<img src="images/hrbc_dl/hrbc_dl_39.png" width="800"><br><br>

(4)「チェックされているデータ」を選択し「OK」を押下します。<br>
ページに表示されている全件のIDの出力を希望の場合は「表示されているデータ」を選択し「OK」を押下します。<br>
<img src="images/hrbc_dl/hrbc_dl_36.png" width="300"><br><br>

(5)クラウドドキュメントに遷移し、先ほどチェックを入れた複数のIDが自動的に入力されます。<br>
テンプレートを選択して「ダウンロードする」ボタンを押下します。<br>
![ダウンロードする](images/hrbc_dl/hrbc_dl_32.png)<br><br>

(6)左側のメニュー「帳票の一括作成」の中の「処理結果DL」ページに入り、<br>
<img src="images/hrbc_dl/hrbc_dl_31.png" width="300"><br><br>

(7)処理結果からExcelまたはPDFを選択します。<br>
※処理結果にExcelまたはPDFのボタンが表示されるまで少々お待ちください。<br>
※ダウンロードできるのは5の「ダウンロードする」ボタンを押してから30分以内となりますのでお気をつけください。
![形式を選択](images/hrbc_dl/hrbc_dl_37.png)<br><br>

(8)zipファイルにてダウンロードされますので解凍してご確認ください。<br>
![ダウンロード](images/hrbc_dl/hrbc_dl_38.png)<br><br>

<br><br>

<h2 id="dl">2.クラウドドキュメントから成約IDを入力してダウンロードする</h2>

#### 【ご注意ください】本番環境にて出力した帳票すべてが課金対象になります(トライアル期間内、テスト環境での利用を除く)<br>詳細は[帳票のご利用料金について](#price)をご確認ください。　<br>

<h3 id="dl_1">2-1.「帳票の作成」からクラウドドキュメントを出力する</h3>
(1)「帳票の作成」から出力したいメニューを選択し、Sales ID欄に成約IDを入力します。

![Sales ID欄に成約IDを入力](images/hrbc_dl/hrbc_dl_user5.png)

(2) 以降の操作は [1-1.クラウドドキュメントを1件ダウンロードする(4)](#hrbc_dl_1_4)をご参照ください。

<br><br>

<h3 id="dl_2">2-2.「帳票の一括作成」からクラウドドキュメントを出力する</h3>

(1) クラウドドキュメントの左側のメニュー「帳票の一括作成」から、該当する階層を選びます。<br>
<br>
<img src="images/hrbc_dl/hrbc_dl_30.png" width="300"><br><br>

(2) 出力したいIDをコンマで区切り入力し、テンプレートを選択して「ダウンロードする」ボタンを押下します。<br>
![出力したいIDをコンマで区切り入力](images/hrbc_dl/hrbc_dl_32.png)<br><br>

(3) 左側のメニュー「帳票の一括作成」の中の「処理結果DL」ページに入り、<br>
<img src="images/hrbc_dl/hrbc_dl_31.png" width="300"><br><br>

(4) 処理結果からExcelまたはPDFを選択します。<br>
※処理結果にExcelまたはPDFのボタンが表示されるまで少々お待ちください。<br>
※ダウンロードできるのは2の「ダウンロードする」ボタンを押してから30分以内となりますのでお気をつけください。<br>
![形式を選択](images/hrbc_dl/hrbc_dl_37.png)<br><br>

(5) zipファイルにてダウンロードされますので解凍してご確認ください。<br>
![ダウンロード](images/hrbc_dl/hrbc_dl_38.png)<br><br>

<br><br>

<h3 id="dl_3">2-3.「出力履歴」からクラウドドキュメントを出力する</h3>
「出力履歴」では、過去に出力したクラウドドキュメントの履歴を確認し、再出力できます。

(1)「出力履歴」を選択し、右側の「対象データ」にあるIDを押下します。

![左のメニューから出力履歴を選択](images/hrbc_dl/hrbc_dl_27.png)

![「対象データ」にあるIDを押下](images/hrbc_dl/hrbc_dl_user7.png)

(2) 別ウィンドウでPORTERSの「売上一覧」が表示されます。左上のタブで「クラウド帳票(本番)」を選択し、ダウンロード画面に切り替えます。

※検証環境がある場合、検証環境でダウンロードしたい場合は「クラウド帳票(検証)」を選択します。
![PORTERSの「売上一覧」が表示されます](images/hrbc_dl/hrbc_dl_29.png)

(3) 以降の操作は [1-1.クラウドドキュメントを1件ダウンロードする(4)](#hrbc_dl_1_4)をご参照ください。

[▲TOPに戻る](#TOP)
<br><br><br>


<h2 id="dl_ledger">3.台帳(一覧表)をダウンロードする</h2>

#### 【ご注意ください】本番環境にて出力した帳票すべてが課金対象になります(トライアル期間内、テスト環境での利用を除く)<br>詳細は[帳票のご利用料金について](#price)をご確認ください。　<br>
#### ※マクロを使用したテンプレート(xlms形式)は出力について注意点がございます。　<br>詳細は[よくある質問 Q.テンプレートにマクロは使用できますか？ ](https://e2info.github.io/cloudreport-docs/faq/faq.html#template3)でご確認ください。

同じリソースに対して、PORTERSで複数選択したデータの台帳が出力します。

<h3 id="dl_ledger_1">3-1.出力</h3>

(1)一括アクションボタンのプルダウンから、 一覧表メニューを選びます。

![一覧表メニューを選ぶ](images/dl_ledger/dl_ledger_4.png)
<br><br>

(2)表示されているデータ全てorチェックを入れたデータかを選びます。<br>
![表示されているデータ全てorチェックを入れたデータかを選ぶ](images/dl_ledger/dl_ledger_5.png)
<br><br>

(3)テンプレートを選択しダウンロードします。
<br>

(4) 以降の操作は [1-1.クラウドドキュメントを1件ダウンロードする(4)](#hrbc_dl_1_4)をご参照ください。
<br><br>

[▲TOPに戻る](#TOP)
<br><br><br>


<h2 id="dl_sp">4.特定の帳票を設定したアクションボタンについて</h2>

よく使う帳票はアクションボタンに設定することが可能です。<br>

![アクションボタン](images/dl_sp/dl_sp_5.png)<br>

※設定は管理者の方のみ可能です。変更したい場合は管理者の方に依頼をお願いいたします。

<br><br>
-----
* 2021年8月25日新規作成
* 2022年7月22日更新


{% include footer.md %}
