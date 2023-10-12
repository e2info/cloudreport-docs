---
layout: default
title: クラウドドキュメント リリースノート

---
<br>
<div align="center">
<img src="images/logo-type.png" alt="クラウドドキュメント" title="クラウドドキュメント">
</div>
<br><br>

# クラウドドキュメント 商談管理階層対応マニュアル（管理者用）

<h2 id="TOP">目次</h2>

- [1.PORTERSとの同期](#porters)
  - [1-1.PORTERSフィールドの取得](#porters_1)
  - [1-2.PORTERS選択肢の取得](#porters_2)
  - [1-3.PORTERSユーザーの取得](#porters_3)
- [2.PORTERS側にアクションボタンを設定](#porters_action)
- [3.帳票の新規登録](#document)
- [4.マッピングの設定](#mapping)
- [5.PORTERSからクラウドドキュメントをダウンロードする](#porters_dl)
- [6.クラウドドキュメントからIDを入力して ダウンロードする](#dl)
  - [6-1.「帳票一覧」からクラウドドキュメントを出力する](#dl_1)
  - [6-2.「ダウンロード」からクラウドドキュメントを出力する](#dl_2)
- [7.台帳(一覧表)をダウンロードする](#dl_ledger)
  - [7-1.PORTERSの設定](#dl_ledger_1)
  - [7-2.テンプレートの作成](#dl_ledger_2)
  - [7-3.テンプレートの登録](#dl_ledger_3)
  - [7-4.一覧表の出力](#dl_ledger_4)
- [8.PORTERSに設定するURLの種類について](#dl_sp)
 

<h2 id="porters">1.PORTERSとの同期</h2>

#### 商談管理階層利用開始に伴い、PORTERSとクラウドドキュメントを手動で同期する必要があります。

<h3 id="porters_1">1-1.PORTERSフィールドの同期</h3>
(1) 左側メニューから「PORTERSフィールド同期」を選択します。<br>

<img src="images/hrbc_sync/hrbc_1.png" width="300">

(2)「PORTERSフィールド情報の同期」を押下します。

<img src="images/hrbc_sync/hrbc_2.png" width="800">


PORTERSフィールドの取得が完了すると管理画面に遷移し、<br>
「PORTERSフィールド情報を同期しました。」という緑色の帯が表示されます。

<img src="images/hrbc_sync/hrbc_3.png" width="800">

<br><br>

<h3 id="porters_2">1-2.PORTERS選択肢の取得</h3>
(1) 左側の「PORTERS選択肢取得」を選択します。

<img src="images/hrbc_sync/hrbc_4.png" width="300">

(2)「PORTERS選択肢情報の同期」を押下します。

<img src="images/hrbc_sync/hrbc_5.png" width="800">


PORTERSフィールドの取得が完了すると管理画面に遷移し、「PORTERS選択肢情報を同期しています。<br>
処理完了までおよそ10分程度かかります。」という緑色の帯が表示されます。<br>
10分程度置いていただければ完了となります。<br>

※現状、「PORTERS選択肢情報を同期しました。」と表示されませんが処理は完了しております。(現在改修中です)
<img src="images/hrbc_sync/hrbc_6.png" width="800">

<br><br>

<h3 id="porters_1">1-3.PORTERSユーザーの同期</h3>
(1) 左側メニューから「PORTERSユーザーの同期」を選択します。<br>

<img src="images/hrbc_sync/hrbc_7.png" width="300">

(2)「PORTERSユーザーの同期」を押下します。

<img src="images/hrbc_sync/hrbc_8.png" width="800">


PORTERSフィールドの取得が完了すると管理画面に遷移し、<br>
「PORTERSユーザーを同期しました。」という緑色の帯が表示されます。

<img src="images/hrbc_sync/hrbc_9.png" width="800">

<br><br>


[▲TOPに戻る](#TOP)
<br><br><br>

<h2 id="porters_action">2.PORTERS側にアクションボタンを設定</h2>
PORTERS側から、商談管理IDを押下した際にクラウドドキュメントに遷移するアクションボタンを設定します。

(1) PORTERSの「設定」→「カスタマイズ/デスクトップ」に入ります<br>

<img src="images/opportunity/opportunity_1.png" width="500">

(2) 「アクションメニュー」の編集を押下します<br>

<img src="images/opportunity/opportunity_2.png" width="500">

(3) 左上のプルダウンから「商談管理」を選択、その隣のプルダウンから「アクションメニュー」を選択し、右側の「新規」を押下します<br>

<img src="images/opportunity/opportunity_3.png" width="800">

(4) アクションボタンの名称とURLを設定します。<br>

<img src="images/opportunity/opportunity_4.png" width="500">

URLはクラウドドキュメントから取得可能です。<br>
クラウドドキュメント「PORTERS設定」から「PORTERS側の設定」に入ります。<br>
<img src="images/opportunity/opportunity_5.png" width="300">

一番上に表示されている「アクションメニュー設定用URL(帳票の種類:通常)」の欄から下にスクロールし<br>
<img src="images/opportunity/opportunity_7.png" width="800">
<br>
リソース　商談管理からURLをコピーします。<br>
<img src="images/opportunity/opportunity_6.png" width="800">

コピーしたものをPORTERSの下記画面のURL欄にペーストし、「保存」します。
<img src="images/opportunity/opportunity_4.png" width="500">

追加したアクションボタンを左の枠内にドラッグし、最後に必ず「レイアウトを確定」を押下してください。
<img src="images/opportunity/opportunity_11.png" width="800">

(5)以上の作業でアクションボタンの設定が完了です<br>

<img src="images/opportunity/opportunity_8.png" width="800">

※設定するURLの違いについては [8.PORTERSに設定するURLの種類について](#dl_sp)をご参照ください。


[▲TOPに戻る](#TOP)

<br><br><br>

<h2 id="document">3.帳票の新規登録</h2>
商談管理用の帳票を新規登録します。
※登録の仕方は他の階層と同様です

(1) 「帳票一覧」を選択し、「＋新規登録」を押下します。

<img src="images/document_temp/document_temp_1.png" width="800">

(2) 「タイトル」欄に帳票名を入力、「リソース」欄に「商談管理」を選択し、「保存する」を押下します。
<img src="images/opportunity/opportunity_9.png" width="800">

(3) 「テンプレート」欄の「ファイルをアップロードしてください」または「Browse」を押下し、ファイルをアップロードします。<br>
<img src="images/document_temp/document_temp_4.png" width="800">

(4) その他帳票の設定について<br>
・作成した帳票に許可する操作<br>
・帳票制作時の空白の値の処理<br>
の設定を選択してください。<br>
※作成した帳票に許可する操作は管理者はすべて許可、<br>
 ユーザーはPORTERSに保存することのみ許可がデフォルトで設定されています。<br>
※帳票制作時の空白の値の処理についてはデフォルトでは「値を出力せず、セルを空白にする」となっています。<br>
<img src="images/document_temp/document_temp_5.png" width="500">

(7)最後に「保存する」を押下すると帳票一覧に追加されます。

テンプレートが作成されると帳票一覧に遷移し、「更新しました」という緑色の帯が表示され、帳票一覧に作成したテンプレートが表示されます。

![テンプレートが表示される](images/document_temp/document_temp_8.png)

[▲TOPに戻る](#TOP)
<br><br><br>


<h2 id="mapping">4．マッピングの設定</h2>
登録した帳票にマッピングを行います。

(1) 「帳票一覧」を選択し、右側の「アクション」にある「マッピング」を押下します。
<img src="images/document_temp/document_temp_9.png" width="800">

(2) 「マッピング設定」に遷移するので、右側の「アクション」にある「更新」アイコンを押下します。<br>
<img src="images/mapping/mp_1.png" width="800">

(3) 「PORTERSフィールド」欄からPORTERSに紐づける項目を選択します。<br>
プルダウンから選択したり、キーワードを入力し検索することも可能です。<br>
<img src="images/mapping/mp_2.png" width="800">
<br><br><br>
なお、各リソース(階層)によってマッピングできるエイリアスの種類が異なります。
詳細は下記の通りです。<br>

|リソース(階層)|マッピングできるエイリアスの種類|
|-----|-----|
|商談管理|SystemField、Opportunity、Client、Recruiter|
|企業|SystemField、Client|
|企業担当者|SystemField、Recruiter、Client|
|JOB|SystemField、Job、Client、Recruiter|
|個人連絡先|SystemField、Person|
|レジュメ|SystemField、Resume、Person|
|売上|SystemField、Sales、Person、Job、Client、Recruiter、Contract、Resume|
|アクティビティ|SystemField、Activity、Job、Resume|
|選考プロセス|SystemField、Process、Person、Job、Client、Recruiter、Resume|

<br><br>
(4)設定が完了したら最後に 「保存する」を押下します。
<img src="images/mapping/mp_3.png" width="800">

更新が完了すると「マッピング設定」に遷移し、「マッピング情報を更新しました。」という緑色の帯が表示され、<br>
「PORTERS名称」と「PORTERSエイリアス」が反映されます。
<img src="images/mapping/mp_4.png" width="800">

<br><br>
[▲TOPに戻る](#TOP)
<br><br><br>

<h2 id="porters_dl">5.PORTERSから帳票をダウンロードする</h2>

#### 【ご注意ください】本番環境にて出力した帳票すべてが課金対象になります(トライアル期間内、テスト環境での利用を除く)<br>詳細は[帳票のご利用料金について](#price)をご確認ください。　<br>
#### ※マクロを使用したテンプレート(xlms形式)は出力について注意点がございます。　<br>詳細は[よくある質問 Q.テンプレートにマクロは使用できますか？ ](https://e2info.github.io/cloudreport-docs/faq/faq.html#template3)でご確認ください。


(1) PORTERSでクラウドドキュメントを作成したい商談管理IDをクリックし、アクションボタン「クラウドドキュメント」を押下します。<br>
<img src="images/opportunity/opportunity_8.png" width="600">

(3) クラウドドキュメントに遷移します。先ほど選択した商談管理IDが挿入された状態になっています。<br>
出力したいテンプレートをプルダウンから指定し「ダウンロード」をします。もしくは「プレビュー」も可能です。<br>
「ダウンロードする」ボタンを押下すると、帳票ダウンロード画面に切り替わります。<br>
<img src="images/opportunity/opportunity_10.png" width="600">


<br><br>

①アクション＝「ダウンロードする」の場合

(1)「ダウンロードする」の右側にあるEXCEL/PDFのボタンを押下します。
<img src="images/hrbc_dl/hrbc_dl_6.png" width="600">

(2) 画面左下に表示されるブラウザのダウンロードバーをクリックするとダウンロードしたEXCEL/PDFファイルが確認できます。
![EXCEL/PDFファイルを確認](images/hrbc_dl/hrbc_dl_7.png)

もしくはPCのダウンロードフォルダにEXCEL/PDFファイルが保存され確認できます。
![EXCEL/PDFファイルを保存](images/hrbc_dl/hrbc_dl_8.png)

<br><br>

②アクション＝ 「PORTERSに保存する」の場合
#### ※マクロを使用したテンプレート(xlms形式)はPORTERSに保存できません。

(1)「PORTERSに保存する」の右側にあるEXCEL/PDFのボタンを押下します。
<img src="images/hrbc_dl/hrbc_dl_9.png" width="800">

(2)上部に「PORTERSにファイルを添付しました。」という緑色の帯が表示されたら「PORTERSを開く」をクリックします。
<img src="images/hrbc_dl/hrbc_dl_10.png" width="800">

(3)PORTERS画面に切り替わり、出力したい各階層のウィンドウが表示されます。<br>
「サブリスト｜ 添付ファイル」でダウンロードしたEXCEL/PDFファイルが確認、ファイル名押下でダウンロードできます。<br>
  
<img src="images/opportunity/opportunity_20.png" width="800">

#### PORTERS上にサブリストが表示されない場合は
(1) PORTERの「設定」→「カスタマイズ/デスクトップ」に入ります<br>
<img src="images/opportunity/opportunity_1.png" width="500">

(2) 「サブリスト」の編集を押下し、左上のプルダウンから「商談管理」を選びます<br>
<img src="images/sublist/sublist_2.png" width="800">

(3)「添付ファイル」のサブリスト項目を中央の枠内にドラッグし、最後に必ず「レイアウトを確定」を押下します<br>
<img src="images/sublist/sublist_1.png" width="800">

上記の設定で表示されます。

<br><br>
[▲TOPに戻る](#TOP)
<br><br><br>

<h2 id="dl">6.クラウドドキュメントからIDを入力してダウンロードする</h2>

[5.PORTERSからクラウドドキュメントをダウンロードする](#porters_dl)でご紹介した方法以外の出力方法を紹介します。

<h3 id="dl_1">6-1.「帳票一覧」から帳票を出力する</h3>

#### 【ご注意ください】本番環境にて出力した帳票すべてが課金対象になります(トライアル期間内、テスト環境での利用を除く)　<br>詳細は[帳票のご利用料金について](#price)をご確認ください。
#### ※マクロを使用したテンプレート(xlms形式)は出力について注意点がございます。　<br>詳細は[よくある質問 Q.テンプレートにマクロは使用できますか？ ](https://e2info.github.io/cloudreport-docs/faq/faq.html#template3)でご確認ください。

(1) 「帳票一覧」を選択し、「個別出力」欄に出力したい各階層のIDを入力します。<br>

(2) 「出力」を押下すると、帳票ダウンロード画面に切り替わります。<br>

以降の操作は [5.クラウド帳票をダウンロードする](#porters_dl)をご参照ください。

<br><br>

<h3 id="dl_2">6-2.「帳票の作成」から帳票を出力する</h3>

#### 【ご注意ください】本番環境にて出力した帳票すべてが課金対象になります(トライアル期間内、テスト環境での利用を除く)<br>詳細は[帳票のご利用料金について](#price)をご確認ください。　<br>
#### ※マクロを使用したテンプレート(xlms形式)は出力について注意点がございます。　<br>詳細は[よくある質問 Q.テンプレートにマクロは使用できますか？ ](https://e2info.github.io/cloudreport-docs/faq/faq.html#template3)でご確認ください。

(1)「帳票の作成」から出力したいメニューを選択し、ID欄に出力したい各階層のIDを入力します。

![ID欄に出力したい各階層のIDを入力](images/hrbc_dl/hrbc_dl_25.png)

(2) 以降の操作は [5.クラウドドキュメントをダウンロードする](#porters_dl)をご参照ください。

<br><br>
[▲TOPに戻る](#TOP)
<br><br><br>

<h2 id="dl_ledger">7.一覧表をダウンロードする</h2>

#### 【ご注意ください】本番環境にて出力した帳票すべてが課金対象になります(トライアル期間内、テスト環境での利用を除く)　<br>詳細は[帳票のご利用料金について](#price)をご確認ください。<br>

同じリソースに対して、PORTERSで複数選択したデータの一覧表を出力します。

<h3 id="dl_ledger_1">7-1.PORTERSの設定</h3>
(1) PORTERの「設定」→「カスタマイズ/デスクトップ」に入ります<br>

<img src="images/opportunity/opportunity_1.png" width="500">

(2) 「アクションメニュー」の編集を押下します<br>

<img src="images/opportunity/opportunity_2.png" width="500">

(3) 左上のプルダウンから「商談管理」を選択、その隣のプルダウンから「一括アクション」を選択し、右側の「新規」を押下します<br>

<img src="images/opportunity/opportunity_12.png" width="600">

(4) アクションボタンの名称とURLを設定します。<br>

<img src="images/opportunity/opportunity_16.png" width="600">

URLはクラウドドキュメントから取得可能です。<br>
クラウドドキュメント「PORTERS設定」から「PORTERS側の設定」に入ります。<br>
<img src="images/opportunity/opportunity_5.png" width="300">

赤枠の「一覧表出力」を押下すると<br>
<img src="images/opportunity/opportunity_13.png" width="600">

「アクションメニュー設定用URL(帳票の種類:一覧表出力)」にページ内遷移しますのでそのまま下にスクロールし
<img src="images/opportunity/opportunity_14.png" width="600">

リソース　商談管理からURLをコピーします。<br>
<img src="images/opportunity/opportunity_15.png" width="600">

コピーしたものをPORTERSの下記画面のURL欄にペーストし、「保存」します。
<img src="images/opportunity/opportunity_16.png" width="600">

追加したアクションボタンを左の枠内にドラッグし、最後に必ず「レイアウトを確定」を押下してください。
<img src="images/opportunity/opportunity_17.png" width="600">

(5)以上の作業で一括アクションボタンの設定が完了です<br>

<img src="images/opportunity/opportunity_18.png" width="600">

※設定するURLの違いについては [8.PORTERSに設定するURLの種類について](#dl_sp)をご参照ください。


<br><br>

<h3 id="dl_ledger_2">7-2.テンプレートの作成</h3>

繰り返し行の前後を　\{\{LOOP_START\}\}　　～　　　\{\{LOOP_END\}\}で囲みます。(この行は削除されます) <br>
![囲む](images/dl_ledger/dl_ledger_2.png) <br><br>

<h3 id="dl_ledger_3">7-3.テンプレートの登録</h3> 

帳票一覧→新規登録を行い帳票の種類に「一覧表」を選んで保存し、テンプレートを設定し、マッピングを行います。

<img src="images/opportunity/opportunity_19.png" width="600">

<br><br>

<h3 id="dl_ledger_4">7-4.一覧表の出力</h3>

(1)一覧表として出力したいIDにチェックを入れて、「一括アクションボタン」に設定したボタンを押下します。

<img src="images/opportunity/opportunity_18.png" width="600">
<br><br>

(2)表示されているデータ全てorチェックを入れたデータかを選びます。<br>
※いずれの場合も選択できるデータの上限は1000件です。<br>
![表示されているデータ全てorチェックを入れたデータかを選ぶ](images/dl_ledger/dl_ledger_5.png)
<br><br>

(3)[7-2.テンプレートの作成](#dl_ledger_2)で登録したテンプレートを選択しダウンロードします。
<br>

(4) 以降の操作は [5.クラウドドキュメントをダウンロードする](#porters_dl)をご参照ください。
<br><br>


[▲TOPに戻る](#TOP)
<br><br>


<h3 id="dl_sp">8.PORTERSに設定するURLの種類について</h3>

### どのURLを入れるかによりアクションボタン押下で帳票出力画面に遷移後の表示が異なります。<br>
※ここではJOB階層での設定を例に説明します。<br><br>

#### ID変更:可　　テンプレート変更:可　　　テンプレート初期値：なし<br>
IDを変更可能、テンプレートも変更可能<br>

![ID可 テ可 初なし](images/dl_sp/IDOK_temOK_IVNO.png)<br><br>

#### ID変更:不可　　テンプレート変更:可　　　テンプレート初期値：なし<br>
IDは固定、テンプレートは変更可能<br>

![ID可 テ不可 初なし](images/dl_sp/IDNO_temOK_ivNO.png)<br><br>

#### ID変更:可　　テンプレート変更:可　　　テンプレート初期値：あり<br>
IDは変更可能、テンプレートは指定されたものが自動的に設定されるが変更可能<br>

![ID可 テ可 初あり](images/dl_sp/IDOK_temOK_ivOK.png)<br><br>

#### ID変更:可　　テンプレート変更:不可　　　テンプレート初期値：あり<br>
IDは変更可能、テンプレートは指定されたものが自動的に設定される(変更不可)<br>

![ID可 テ不可 初あり](images/dl_sp/IDOK_temNO_ivOK.png)<br><br>

#### ID変更:不可　　テンプレート変更:可　　　テンプレート初期値：あり

IDは変更不可、テンプレートは指定されたものが自動的に設定されるが変更可能<br>

![ID不可 テ可 初あり](images/dl_sp/IDNO_temOK_ivOK.png)

#### ID変更:不可　　テンプレート変更:不可　　　テンプレート初期値：あり

IDは変更不可、テンプレートは指定されたものが自動的に設定される(変更不可)<br>

![ID不可 テ不可 初あり](images/dl_sp/IDNO_temNO_ivOK.png)

上記を必要に応じて設定することで、帳票出力毎の設定の工程を短縮できます。


[▲TOPに戻る](#TOP)
<br><br><br><br>

-----

* 2023年9月29日新規作成


{% include footer.md %}
