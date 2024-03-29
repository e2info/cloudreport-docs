---
layout: default
title: クラウドドキュメント リリースノート

---
<br>
<div align="center">
<img src="images/logo-type.png" alt="クラウドドキュメント" title="クラウドドキュメント">
</div>
<br><br>

# クラウドドキュメント 作成マニュアル（管理者用）

<h2 id="TOP">目次</h2>

- [はじめに](#introduction)
  - [クラウドドキュメントの動作保証環境について](#os) 
  - [主なフローについて](#flow)
  - [クラウドドキュメントのログインについて](#login)
  - [帳票のご利用料金について](#price)
  - [処理時間の上限について](#processing_time)
- [1.PORTERSとの同期](#porters)
  - [1-1.PORTERSフィールドの取得](#porters_1)
  - [1-2.PORTERS選択肢の取得](#porters_2)
  - [1-3.PORTERSユーザーの取得](#porters_3)
- [2.テンプレート用ファイルの作成](#document_temp_file)
  - [2-1.テンプレート用ファイルの作成](#document_temp_file_1)
- [3.テンプレートの作成](#document_temp)
  - [3-1.テンプレートの新規作成](#document_temp_1)
  - [3-2.テンプレートの更新](#document_temp_2)
  - [3-3.テンプレートの削除](#document_temp_3) 
  - [3-4.テンプレートのステータス(有効/無効)について](#document_temp_4) 
- [4.マッピングの設定](#mapping)
  - [4-1.マッピングの更新](#mapping_1)
  - [4-2.マッピングのエクスポート/インポート](#mapping_2)
  - [4-3.マッピングの削除](#mapping_3)
- [5.PORTERSからクラウドドキュメントをダウンロードする](#porters_dl)
  - [5-1.クラウドドキュメントを1件ダウンロードする](#porters_dl_1)
  - [5-2.クラウドドキュメントを一括ダウンロードする](#porters_dl_2)
- [6.クラウドドキュメントからIDを入力して ダウンロードする](#dl)
  - [6-1.「帳票一覧」からクラウドドキュメントを出力する](#dl_1)
  - [6-2.「ダウンロード」からクラウドドキュメントを出力する](#dl_2)
  - [6-3.「一括ダウンロード」からクラウドドキュメントを出力する](#dl_3)
  - [6-4.「出力履歴」からクラウドドキュメントを出力する](#dl_4)
- [7.台帳(一覧表)をダウンロードする](#dl_ledger)
  - [7-1.PORTERSの設定](#dl_ledger_1)
  - [7-2.テンプレートの作成](#dl_ledger_2)
  - [7-3.テンプレートの登録](#dl_ledger_3)
  - [7-4.出力](#dl_ledger_4)
- [8.特定の帳票をアクションボタンに設定する](#dl_sp)
  - [8-1.PORTERSの設定](#dl_sp_1)
  - [8-2.出力](#dl_sp_2)
 
<h2 id="introduction">はじめに</h2>

<h3 id="os">クラウドドキュメントの動作保証環境について</h3>
PORTERSに準じ、動作保証環境を設定しています。

[クラウドドキュメント よくある質問 「クラウドドキュメントの動作保証環境はどちらになりますか？」](https://e2info.github.io/cloudreport-docs/faq/faq.html#about1)でご確認ください。
<br><br>


<h3 id="flow">主なフローについて</h3>

<br>
<div align="center">
<img src="images/hrbc_sync/flow.png" width="600" alt="主なフロー" title="主なフロー">
</div>
<br><br>

#### 1.PORTERSの同期（管理者のみ利用可能）

初回はクラウドドキュメントの「PORTERSフィールド取得」「PORTERS選択肢の取得」画面にて、PORTERSのデータと紐づける項目を同期します。
なお、PORTERSで項目の追加・削除などの変更があった場合、クラウドドキュメント側も都度同期する必要があります。

詳細は[1.PORTERSとの同期](#porters)をご確認ください。

<br>

#### 2.帳票テンプレートの作成（管理者のみ利用可能）

「帳票一覧」画面より、クラウドドキュメントに出力する帳票のテンプレートを新規作成します。<br>
テンプレートを新規作成あるいは更新する場合、Excelファイルで作成したテンプレートを取り込みます。<br>
その後、「マッピング設定」画面にて、出力項目とPORTERSのデータを紐づけします。

詳細は[2.帳票テンプレート用ファイルの作成](#document_temp_file)　[3.帳票テンプレートの作成](#document_temp)　[4.マッピングの設定](#mapping)をご確認ください。

<br>

#### 3.ダウンロード（管理者/標準ユーザー共通で利用可能）

作成した帳票テンプレートをユーザーPCかPORTERSにダウンロードします。<br>
ダウンロードは、「PORTERSから出力したい各階層のIDの画面から出力する方法」と「クラウドドキュメントから出力したい各階層のIDを入力する方法」があります。<br>

詳細は[5.PORTERSからクラウドドキュメントをダウンロードする](#porters_dl)　　[6.クラウドドキュメントから出力したい各階層のIDを入力してダウンロードする](#dl)をご確認ください。
<br><br>

<h3 id="login">クラウドドキュメントのログインについて</h3>
初回の設定を行う上で、クラウドドキュメントの画面は一度PORTERSを経由してログインする必要があります。
お知らせしたクラウドドキュメントURLにアクセスいただき、PORTERSのログインを経てご使用いただけます。

<h3 id="price">帳票のご利用料金について</h3>

#### 本番環境にて出力した帳票全てが課金対象となります。(トライアル期間・テスト環境での利用を除く)

(1) 課金のタイミングについて<br>
「ダウンロード」ボタンを押すと１帳票分課金となります。<br>
その後遷移する画面にてPDFやExcelのダウンロードボタン、もしくは「PORTERSに保存する」のPDFやExcelのダウンロードボタンを押しても課金されません。

![課金のタイミングについて](images/price1.png)

(2) 出力枚数の確認について<br>
クラウドドキュメントのメニュー 利用状況 統計に各月における各帳票の出力枚数の確認ができます。

![出力枚数の確認について](images/price2.png)

[▲TOPに戻る](#TOP)
<br><br><br>

<h3 id="processing_time">処理時間の上限について</h3>

各処理にはタイムアウト時間が設けられています。<br>
処理が完了せずタイムアウト時間に到達すると、エラーとなり帳票出力が失敗します。<br>
その場合は、処理件数を減らす・マッピング数を減らすなどの調整をお願いします。<br><br>

|処理分類|分類|項目|処理時間|
|-----|-----|-----|-----|
|同期処理|共通|同期処理タイムアウト|30秒|
|非処理|共通|非処理タイムアウト|60秒|
|非処理|帳票の一括作成|帳票の一括作成|30分|
|非処理|PORTERS設定|選択肢の同期|30分|
|非処理|一覧表|一覧表|30分|

[▲TOPに戻る](#TOP)
<br><br><br>

<h2 id="porters">1.PORTERSとの同期</h2>

#### PORTERSのフィールドや選択肢、ユーザーを追加・変更した場合、クラウドドキュメントを手動で同期する必要があります。

<h3 id="porters_1">1-1.PORTERSフィールドの同期</h3>
(1) 左側の「PORTERS設定」から「フィールドの同期」を選択します。<br>

![PORTERSフィールドの同期](images/hrbc_sync/hrbc_1.png)

(2)「PORTERSフィールドの同期」を押下します。
![PORTERSフィールドの同期](images/hrbc_sync/hrbc_2.png)

PORTERSフィールドの取得が完了すると管理画面に遷移し、「PORTERSフィールドを同期しました。」という緑色の帯が表示されます。

![PORTERSフィールドを同期しました](images/hrbc_sync/hrbc_3.png)

<br><br>

<h3 id="porters_2">1-2.PORTERS選択肢の同期</h3>
(1) 左側の左側の「PORTERS設定」から「選択肢の同期」を選択します。

![選択肢取得](images/hrbc_sync/hrbc_4.png)

(2)「PORTERS選択肢の同期」を押下します。
![PORTERS選択肢の同期](images/hrbc_sync/hrbc_5.png)

PORTERSフィールドの取得が完了すると管理画面に遷移し、「PORTERS選択肢情報を同期しています。処理完了までおよそ10分程度かかります。」という緑色の帯が表示されます。
10分程度置いていただければ完了となります。

※現状、「PORTERS選択肢を同期しました。」と表示されませんが処理は完了しております。(現在改修中です)
![PORTERS選択肢を同期しました](images/hrbc_sync/hrbc_6.png)


<br><br>

<h3 id="porters_3">1-3.PORTERSユーザーの同期</h3>
(1) 左側の左側の「PORTERS設定」から「ユーザーの同期」を選択します。

![ユーザーの同期](images/hrbc_sync/hrbc_10.png)

(2)「PORTERSユーザーの同期」を押下します。
![PORTERSユーザーの同期を押下](images/hrbc_sync/hrbc_12.png)

PORTERSユーザーの同期が完了すると管理画面に遷移し、「PORTERSユーザーを同期しました。」という緑色の帯が表示されます。

![PORTERSユーザーを同期しました](images/hrbc_sync/hrbc_11.png)

<br><br>


[▲TOPに戻る](#TOP)
<br><br><br>

<h2 id="document_temp_file">2.帳票テンプレート用ファイルの作成</h2>
クラウドドキュメントのテンプレートはExcelファイルで作成したものを取り込む必要があります。
ここでは、テンプレート用ファイルの作成について説明いたします。


#### <注意事項>
#### ・原則としてテンプレートの作成や修正はお客様にてお願いしており、弊社での対応はオプションにて承ります。<br>
#### (テンプレート作成:出力項目数、分岐数等により100,000円～)<br>
#### ・PDFでの出力はエクセルでの出力結果と全く同じにならない場合がございます。
#### ・マクロを使用したテンプレート(xlms形式)は出力について注意点がございます。　<br>詳細は[よくある質問 Q.テンプレートにマクロは使用できますか？ ](https://e2info.github.io/cloudreport-docs/faq/faq.html#template3)でご確認ください。
<br>

<h3 id="document_temp_file_1">2-1.テンプレート用ファイルの作成</h3>
(1) Excelファイルでテンプレートファイルを作成します。このときクラウドドキュメントに出力したい　箇所は
\{\{\}\}で囲みます。<br>

![テンプレートファイル](images/document_temp/document_temp_file_1.png)

(2) 保存する際は、下記の拡張子でファイルを保存してください。

![保存する際の拡張子](images/document_temp/document_temp_file_2.png)


[▲TOPに戻る](#TOP)

<br><br><br>

<h2 id="document_temp">3.帳票テンプレートの作成</h2>

[2．帳票テンプレート用ファイルの作成](#document_temp_file)で作成したファイルを取り込みます。
ファイルを取り込むことで、クラウドドキュメントに出力したい項目を抽出することができます。

<h3 id="document_temp_1">3-1.テンプレートの新規作成</h3>
(1) 「帳票一覧」を選択し、「＋新規登録」を押下します。

![＋新規登録](images/document_temp/document_temp_1.png)

(2) 「タイトル」欄に帳票名を入力、「リソース」欄にPORTERSリソースを選択し、「保存する」を押下します。
![「リソース」欄にPORTERSリソースを選択し、「保存する」](images/document_temp/document_temp_2.png)

(3) 「テンプレート」欄の「ファイルをアップロードしてください」または「Browse」を押下します。
![「ファイルをアップロードしてください」または「Browse」](images/document_temp/document_temp_3.png)

(4) 表示されるエクスプローラーの中からファイルを選択し、アップロードします。
![ファイルを選択し、アップロード](images/document_temp/document_temp_4.png)

(5) 作成する帳票の操作について許可、不許可を選択してください。
※デフォルトではすべて「許可」となっています。
![作成する帳票の操作について許可、不許可を選択](images/document_temp/document_temp_5.png)

(6) 帳票制作時の空白の値の処理について選択してください。
※デフォルトでは「値を出力せず、セルを空白にする」となっています。
![帳票制作時の空白の値の処理について選択](images/document_temp/document_temp_6.png)

(7)「保存する」を押下すると帳票一覧に追加されます。
![「保存する」](images/document_temp/document_temp_7.png)

テンプレートが作成されると帳票一覧に遷移し、「更新しました」という緑色の帯が表示され、帳票一覧に作成したテンプレートが表示されます。

![テンプレートが表示される](images/document_temp/document_temp_8.png)

出力したい項目が正しく抽出されたかを確認する場合、「帳票一覧」を選択し、右側の「アクション」にある「マッピング」を押下してご確認ください。

![「マッピング」](images/document_temp/document_temp_9.png)

注意事項 ：「帳票更新」画面の「ステータス」欄の「有効」をOFFにした場合
![「ステータス」欄の「有効」をOFF](images/document_temp/document_temp_10.png)

「帳票更新」画面の「ステータス」欄の「有効」をOFFにした場合、「帳票一覧」に表示されなくなります。

「無効の帳票も表示する」を選択することで表示されます。

![無効の帳票も表示する](images/document_temp/document_temp_11.png)

またマッピングが必要な場合、「無効の帳票も表示する」を選択し[3-2.テンプレートの更新](#document_temp_2)にて「ステータス」の「有効」をONに変更する必要があります。

<br><br>

<h3 id="document_temp_2">3-2.テンプレートの更新</h3>
(1) 「帳票一覧」を選択し、右側の「アクション」にある「更新」を押下します。

![更新を押下](images/document_temp/document_temp_12.png)

(2) 「テンプレート」欄の「ファイルをアップロードしてください」または「Browse」を押下します。
![「ファイルをアップロードしてください」または「Browse」](images/document_temp/document_temp_13.png)

(3) 表示されるエクスプローラーの中からファイルを選択し、アップロードします。
![アップロード](images/document_temp/document_temp_4.png)

(4)「保存する」を押下すると「帳票一覧」に追加されます
![「帳票一覧」に追加](images/document_temp/document_temp_7.png)

テンプレートが作成されると「帳票一覧」に遷移し、「更新しました」という緑色の帯が表示され、作成したテンプレートが表示されます。

![更新しました](images/document_temp/document_temp_14.png)

<br><br>

<h3 id="document_temp_3">3-3.テンプレートの削除</h3><br>
(1) 「帳票一覧」を選択し、右側の「アクション」にある「更新」を押下します。<br>

![更新を押下](images/document_temp/document_temp_12.png)<br><br>

(2) 「帳票更新」画面下の「この帳票を削除する」ボタンを押下します。<br>
![「「この帳票を削除する」ボタンを押下](images/document_temp/document_temp_15.png)<br><br>

(3)帳票削除について確認画面が表示されます。<br>
#### 【ご注意ください】　削除するともとに戻すことはできません。<br>よくご確認の上「削除する」を押下します。<br>
<img src="images/document_temp/document_temp_16.png" width="500"><br><br>

(4)削除が完了すると「帳票を削除しました」と確認の案内がでます。<br>
![「削除確認](images/document_temp/document_temp_17.png)<br><br>

<br><br>

<h3 id="document_temp_3">3-4.テンプレートのステータス(有効/無効)について</h3><br>
テンプレートのステータスを無効にすることで一時的にテンプレートを利用できないようにします。<br>
標準ユーザーの方には無効のテンプレートは表示されないため選択できません。<br>
(1) 「帳票一覧」を選択し、右側の「アクション」にある「更新」を押下します。<br>

![更新を押下](images/document_temp/document_temp_12.png)<br><br>

(2) 「帳票更新」画面下の「この帳票を無効する」ボタンを押下します。<br>
![「「この帳票を無効にする」ボタンを押下](images/document_temp/document_temp_18.png)<br><br>

(3)デフォルトの状態では無効の帳票は一覧に表示されません。<br>
無効とした帳票を表示したい場合は赤枠の「無効の帳票も表示する」を押下してください。<br>
![「デフォルトの状態](images/document_temp/document_temp_19.png)<br><br>

(4)ステータスを有効に変更したい場合は「帳票更新」の項目から「ステータス」を有効にしてください。<br>
![有効](images/document_temp/document_temp_21.png)<br><br>



[▲TOPに戻る](#TOP)
<br><br><br>

<h2 id="mapping">4．マッピングの設定</h2>

ここでは[3.帳票テンプレートの作成](#document_temp) で取り込んだ出力用の項目を、PORTERSデータに紐づけを行います。

<h3 id="mapping_1">4-1.マッピングの更新</h3>
(1) 「帳票一覧」を選択し、右側の「アクション」にある「マッピング」を押下します。

![「アクション」にある「マッピング」](images/document_temp/document_temp_9.png)

(2) 「マッピング設定」に遷移するので、右側の「アクション」にある「更新」アイコンを押下します。
![「アクション」にある「更新」](images/mapping/mp_1.png)

(3) 「PORTERSフィールド」欄からPORTERSに紐づける項目を選択します。
![PORTERSに紐づける項目](images/mapping/mp_2.png)
<br><br><br>
なお、各リソース(階層)によってマッピングできるエイリアスの種類が異なります。
詳細は下記の通りです。<br>

<h3 id="mapping_alias"></h3>

|リソース(階層)|マッピングできるエイリアスの種類|
|-----|-----|
|コンタクト|SystemField、Client、Contact|
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
(4) 「保存する」を押下します。
![保存する](images/mapping/mp_3.png)

更新が完了すると「マッピング設定」に遷移し、「マッピング情報を更新しました。」という緑色の帯が表示され、「PORTERS名称」と「PORTERSエイリアス」が反映されます。
![「PORTERS名称」と「PORTERSエイリアス」が反映される](images/mapping/mp_4.png)

<br><br>

<h3 id="mapping_2">4-2.マッピングのエクスポート/インポート</h3>

(1)「エクスポート」では設定済みの「項目」と「エイリアス」の一覧表をExcelにてダウンロードが可能です。

![エクスポート](images/mapping/mp_11.png)

(2)「インポート」よりマッピングを一括で行うことが可能です。

![「エクスポート」](images/mapping/mp_6.png)


(3)エクスポートしたマッピングファイルをアップロードし、インポートしてください。

![ファイルをアップロード](images/mapping/mp_10.png)

(4)インポートした内容が表示されますので、内容を確認し、問題なければ「登録する」ボタンを押してください。

![「登録するボタン」を押下](images/mapping/mp_12.png)

(5)「マッピング情報を更新しました」と表示されましたらインポート完了です。

![マッピング情報を更新しました](images/mapping/mp_13.png)


※インポート用に「項目」と「エイリアス」の一覧表をExcelで作成してインポートして一括でマッピングすることも可能です。
インポート可能なファイルは、xls,xlsx,xlsmの拡張子のファイルのみ、最大サイズは5MBです

![「一覧表作成」](images/mapping/mp_8.png)




<h3 id="mapping_3">4-3.マッピングの削除</h3>
(1) 「帳票一覧」を選択し、右側の「アクション」にある「マッピング」を押下します。

![「アクション」にある「マッピング」](images/document_temp/document_temp_9.png)

(2) 「マッピング設定」に遷移するので、右側の「アクション」にある「更新」アイコンを押下します。
![「アクション」にある「更新」](images/mapping/mp_1.png)

(3) 「PORTERSフィールド」欄から「選択してください」を選択し、マッピングを外します。
![「選択してください」を選択](images/mapping/mp_5.png)

(4)マッピングが解除されると「マッピング設定」に遷移し、指定した行が削除されております。


[▲TOPに戻る](#TOP)
<br><br><br>


<h2 id="porters_dl">5.PORTERSから帳票をダウンロードする</h2>

ここでは[3.帳票テンプレートの作成](#document_temp) で取り込んだ出力用の項目を、PORTERSデータに紐づけを行います。<br>

#### 【ご注意ください】本番環境にて出力した帳票すべてが課金対象になります(トライアル期間内、テスト環境での利用を除く)<br>詳細は[帳票のご利用料金について](#price)をご確認ください。　<br>
#### ※マクロを使用したテンプレート(xlms形式)は出力について注意点がございます。　<br>詳細は[よくある質問 Q.テンプレートにマクロは使用できますか？ ](https://e2info.github.io/cloudreport-docs/faq/faq.html#template3)でご確認ください。

<h3 id="porters_dl_1">5-1.クラウドドキュメントを1件ダウンロードする</h3>
(1) PORTERS画面左上のタブで出力したい各階層を選択し、ドロップダウンからすべてのID分を表示するように選択すると一覧が表示されます。

![一覧](images/hrbc_dl/hrbc_dl_1.png)

(2) クラウドドキュメントを作成したいPORTERSデータのIDをクリックします
![PORTERSデータのIDをクリック](images/hrbc_dl/hrbc_dl_2.png)

(3) 左上のタブで「クラウド帳票(本番)」を選択し、ダウンロード画面に切り替えます。

※検証環境がある場合、検証環境でダウンロードしたい場合は「クラウド帳票(検証)」を選択します。
![ダウンロード画面](images/hrbc_dl/hrbc_dl_3.png)

<h3 id="porters_dl_1_4"></h3>
(4) ダウンロード画面の各ID欄に表示されているIDが正しいことを確認し、
テンプレートのドロップダウンから利用したいテンプレート名称を選択します。

![テンプレート名称を選択](images/hrbc_dl/hrbc_dl_4.png)

(5)「ダウンロードする」ボタンを押下すると、帳票ダウンロード画面に切り替わります。
![帳票ダウンロード画面](images/hrbc_dl/hrbc_dl_5.png)

<br><br>

①アクション＝「ダウンロードする」の場合

(1)「ダウンロードする」の右側にあるEXCEL/PDFのボタンを押下します。
![EXCEL/PDFのボタンを押下](images/hrbc_dl/hrbc_dl_6.png)

(2) 画面左下に表示されるブラウザのダウンロードバーをクリックするとダウンロードしたEXCEL/PDFファイルが確認できます。
![たEXCEL/PDFファイルを確認](images/hrbc_dl/hrbc_dl_7.png)

(3) PCのダウンロードフォルダにEXCEL/PDFファイルが保存されます。
![EXCEL/PDFファイルを保存](images/hrbc_dl/hrbc_dl_8.png)

▼EXCELの場合

![EXCELファイル保存](images/hrbc_dl/hrbc_dl_8_1.png)

▼PDFの場合

![PDFファイル保存](images/hrbc_dl/hrbc_dl_8_2.png)

##### ※マッピング項目先（PORTERS側の値）に半角「¥」が入っていると帳票出力時に半角「\」に変換されてしまいます。<br>
##### 「¥」を帳票に表示したい場合は全角の￥をご使用ください。

![全角の￥をご使用ください](images/hrbc_dl/hrbc_dl_8_3.png)

<br><br>

②アクション＝ 「PORTERSに保存する」の場合
#### ※マクロを使用したテンプレート(xlms形式)はPORTERSに保存できません。

(1)「PORTERSに保存する」の右側にあるEXCEL/PDFのボタンを押下します。
![EXCEL/PDFのボタン](images/hrbc_dl/hrbc_dl_9.png)

(2)上部に「PORTERSにファイルを添付しました。」という緑色の帯が表示されたら「PORTERSを開く」をクリックします。
![「PORTERSを開く」](images/hrbc_dl/hrbc_dl_10.png)

(3)PORTERS画面に切り替わり、出力したい各階層のウィンドウが表示されます。「サブリスト｜ 添付ファイル」でダウンロードしたEXCEL/PDFファイルが確認できます。
  
![EXCEL/PDFファイルを確認](images/hrbc_dl/hrbc_dl_11.png)

<br><br>

<h3 id="porters_dl_2">5-2.クラウドドキュメントを一括ダウンロードする</h3>

#### ※マクロを使用したテンプレート(xlms形式)は出力について注意点がございます。　<br>詳細は[よくある質問 Q.テンプレートにマクロは使用できますか？ ](https://e2info.github.io/cloudreport-docs/faq/faq.html#template3)でご確認ください。

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
<br><br>

(3)PORTERSの各階層で、出力したいIDにチェックを入れて、先ほど設定したアクションメニューを選択します。<br>
もしくはページに表示されている全件のIDの出力を希望の場合はチェックを入れる必要はありません。<br>
※一度に一括出力できるIDは100件までです<br>
<img src="images/hrbc_dl/hrbc_dl_39.png" width="800"><br><br>

(4)「チェックされているデータ」を選択し「OK」を押下します。<br>
ページに表示されている全件のIDの出力を希望の場合は「表示されているデータ」を選択し「OK」を押下します。<br>
※この場合でも上限は100件です<br>
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

<h2 id="dl">6.クラウドドキュメントからIDを入力してダウンロードする</h2>

ここでは[3.帳票テンプレートの作成](#document_temp) で取り込んだ出力用の項目を、PORTERSデータに紐づけを行います。

<h3 id="dl_1">6-1.「帳票一覧」から帳票を出力する</h3>

#### 【ご注意ください】本番環境にて出力した帳票すべてが課金対象になります(トライアル期間内、テスト環境での利用を除く)　<br>詳細は[帳票のご利用料金について](#price)をご確認ください。
#### ※マクロを使用したテンプレート(xlms形式)は出力について注意点がございます。　<br>詳細は[よくある質問 Q.テンプレートにマクロは使用できますか？ ](https://e2info.github.io/cloudreport-docs/faq/faq.html#template3)でご確認ください。

(1) 「帳票一覧」を選択し、「個別出力」欄に出力したい各階層のIDを入力します。<br>

(2) 「出力」を押下すると、帳票ダウンロード画面に切り替わります。<br>

![「帳票一覧」を選択](images/hrbc_dl/hrbc_dl_24.png)

(3) 以降の操作は [5-1.クラウド帳票を1件ダウンロードする(4)](#porters_dl_1_4)をご参照ください。

#### 【ご注意ください】個別出力にIDを入力し出力された場合も課金対象になります(トライアル期間内、テスト環境での利用を除く)<br>詳細は[帳票のご利用料金について](#price)をご確認ください。

<br><br>

<h3 id="dl_2">6-2.「帳票の作成」からクラウドドキュメントを出力する</h3>

#### 【ご注意ください】本番環境にて出力した帳票すべてが課金対象になります(トライアル期間内、テスト環境での利用を除く)<br>詳細は[帳票のご利用料金について](#price)をご確認ください。　<br>
#### ※マクロを使用したテンプレート(xlms形式)は出力について注意点がございます。　<br>詳細は[よくある質問 Q.テンプレートにマクロは使用できますか？ ](https://e2info.github.io/cloudreport-docs/faq/faq.html#template3)でご確認ください。

(1)「帳票の作成」から出力したいメニューを選択し、ID欄に出力したい各階層のIDを入力します。

![ID欄に出力したい各階層のIDを入力](images/hrbc_dl/hrbc_dl_25.png)

(2) 以降の操作は [5-1.クラウドドキュメントを1件ダウンロードする(4)](#porters_dl_1_4)をご参照ください。

<br><br>

<h3 id="dl_3">6-3.「帳票の一括作成」からクラウドドキュメントを出力する</h3>

(1) クラウドドキュメントの左側のメニュー「帳票の一括作成」から、該当する階層を選びます。<br>
<br>
<img src="images/hrbc_dl/hrbc_dl_30.png" width="300"><br><br>

(2) 出力したいIDをコンマで区切り入力し、テンプレートを選択して「ダウンロードする」ボタンを押下します。<br>
※一度に一括出力できるIDは100件までです<br>
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

<h3 id="dl_4">6-4.「出力履歴」からクラウドドキュメントを出力する</h3>

#### 【ご注意ください】本番環境にて出力した帳票すべてが課金対象になります(トライアル期間内、テスト環境での利用を除く)<br>詳細は[帳票のご利用料金について](#price)をご確認ください。　<br>
#### ※マクロを使用したテンプレート(xlms形式)は出力について注意点がございます。　<br>詳細は[よくある質問 Q.テンプレートにマクロは使用できますか？ ](https://e2info.github.io/cloudreport-docs/faq/faq.html#template3)でご確認ください。

「出力履歴」では、過去に出力したクラウド帳票の履歴を確認し、再出力できます。

(1)「出力履歴」を選択し、右側の「対象データ」にあるIDを押下します。

![左のメニューから出力履歴を選択](images/hrbc_dl/hrbc_dl_27.png)

![「対象データ」にあるIDを押下](images/hrbc_dl/hrbc_dl_28.png)

(2) 別ウィンドウでPORTERSの「売上一覧」が表示されます。左上のタブで「クラウド帳票(本番)」を選択し、ダウンロード画面に切り替えます。

※検証環境がある場合、検証環境でダウンロードしたい場合は「クラウド帳票(検証)」を選択します。
![PORTERSの「売上一覧」が表示されます](images/hrbc_dl/hrbc_dl_29.png)

(3) 以降の操作は [5-1.クラウドドキュメントを1件ダウンロードする(4)](#porters_dl_1_4)をご参照ください。

[▲TOPに戻る](#TOP)
<br><br><br>


<h2 id="dl_ledger">7.台帳(一覧表)をダウンロードする</h2>

#### 【ご注意ください】本番環境にて出力した帳票すべてが課金対象になります(トライアル期間内、テスト環境での利用を除く)　<br>詳細は[帳票のご利用料金について](#price)をご確認ください。<br>

同じリソースに対して、PORTERSで複数選択したデータの台帳が出力します。

<h3 id="dl_ledger_1">7-1.PORTERSの設定</h3>
※PORTERSにシステム管理者権限でのログインが必要です。 <br>
(1)設定→カスタマイズの順に選択します <br>
(2)アクションメニュー編集を選択 <br>
(3)アクションメニューを設定するリソースを選択します <br>
(4)一括アクションを選択します

![一括アクションを選択](images/dl_ledger/dl_ledger_1.png)<br>


(5)新規でアクションメニューを作成し、URLを設定します

クラウドドキュメント上の左側のメニュー「PORTERS側の設定」に入ります<br>
<img src="images/dl_ledger/dl_ledger_8.png" width="300"><br>

該当するリソースのURLをコピーしてください <br>
※IDやテンプレートの変更可否やテンプレート初期値の指定あり・なしでURLが変わります。 <br>
　詳しくは [8.特定の帳票をアクションボタンに設定する](#dl_sp)をご参照ください。 <br>
![アクションメニュー設定用URL（帳票の種類：一覧表）_3rd](images/dl_ledger/dl_ledger_7.png)<br>


<br><br>

<h3 id="dl_ledger_2">7-2.テンプレートの作成</h3>

繰り返し行の前後を　\{\{LOOP_START\}\}　　～　　　\{\{LOOP_END\}\}で囲みます。(この行は削除されます) <br>
![囲む](images/dl_ledger/dl_ledger_2.png) <br><br>

<h3 id="dl_ledger_3">7-3.テンプレートの登録</h3> 

帳票一覧→新規登録から一覧表を選んで保存し、テンプレートを設定し、マッピングを行います。

![一覧表を選ぶ](images/dl_ledger/dl_ledger_3.png)

<br><br>

<h3 id="dl_ledger_4">7-4.出力</h3>

(1)一括アクションボタンのプルダウンから、 [7-1.PORTERSの設定](#dl_ledger_1)でPORTERSに設定した一覧表メニューを選びます。

![一覧表メニューを選ぶ](images/dl_ledger/dl_ledger_4.png)
<br><br>

(2)表示されているデータ全てorチェックを入れたデータかを選びます。<br>
※いずれの場合も選択できるデータの上限は1000件です。<br>
![表示されているデータ全てorチェックを入れたデータかを選ぶ](images/dl_ledger/dl_ledger_5.png)
<br><br>

(3)[7-2.テンプレートの作成](#dl_ledger_2)で登録したテンプレートを選択しダウンロードします。
<br>

(4) 以降の操作は [5-1.クラウドドキュメントを1件ダウンロードする(4)](#porters_dl_1_4)をご参照ください。
<br><br>

[▲TOPに戻る](#TOP)
<br><br>

<h2 id="dl_sp">8.特定の帳票をアクションボタンに設定する</h2><br>

よく使う帳票はアクションボタンに設定することが可能です。<br>
この設定により、帳票の種類を選ぶ工程等を省くことができます。<br>

<h3 id="dl_sp_1">8-1.PORTERSの設定</h3>
※PORTERSにシステム管理者権限でのログインが必要です。 <br>
(1)設定→カスタマイズの順に選択します <br>
(2)アクションメニュー編集を選択 <br>
(3)アクションメニューを設定するリソースを選択します <br>
(4)新規アクションメニューを追加します<br>
(5)URLを設定します<br>

![URL設定](images/dl_sp/dl_sp_1.png)<br><br>

#### URLの設定方法
クラウドドキュメントの左側のメニューの「PORTERS側の設定」から値をコピーします<br>

![PORTERS側の設定](images/dl_sp/dl_sp_2.png)<br><br>

#### URLは下記の変更可否によって分かれています。<br>

|項目|内容|
|-----|-----|
|ID変更|JOBID等の各IDを変更できるかどうか|
|テンプレート変更|テンプレートを変更できるかどうか|
|テンプレート初期値|URLの【ここに帳票識別IDを指定してください】の部分を指定するかどうか=帳票を指定するかどうか|

<br>
※帳票識別IDは「帳票更新」画面から確認できます。<br>

![帳票識別ID](images/dl_sp/dl_sp_3.png)<br>

指定したい帳票の帳票識別IDを【ここに帳票識別IDを指定してください】の部分に挿入してください。<br>
(例)<br>
https://XXXXX.cloud-document.net/report/job/{{Job.P_Id}}/template/【ここに帳票識別IDを指定してください】/?user={{Session.P_UserId}}　<br>
帳票識別IDが00035の場合下記のように挿入してください<br>

![挿入](images/dl_sp/dl_sp_4.png)<br><br>

<br>
(6)レイアウトを確定し、設定が完了するとアクションボタンが追加されます。<br>

![アクションボタン追加後](images/dl_sp/dl_sp_5.png)<br><br>

<h3 id="dl_sp_2">8-2.出力</h3>

### どのURLを入れるかによりアクションボタン押下で帳票出力画面に遷移後の表示が異なります。<br>

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

* 2021年8月25日新規作成
* 2024年3月28日更新


{% include footer.md %}
