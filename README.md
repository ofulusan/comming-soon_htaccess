# comming-soon_htaccess
//カミングスーンページの設定方法

■ファイルの詳細
.htaccess //カミングスーンページへリダイレクトさせるプログラム
comming-soon.html //カミングスーンページ(別途で任意のページを準備してください)

■使い方 (.htaccessの設定)

1行目
ErrorDocument 503 /comming-soon.html
カミングスーンのページを設定してください。(デフォルトだとcomming-soon.htmlのファイルがカミングスーンとして表示されます)

6行目
RewriteCond %{TIME_YEAR}%{TIME_MON}%{TIME_DAY}%{TIME_HOUR}%{TIME_MIN} ">開始時間の設定"
カミングスーンページを適応させたい開始時間を設定してください。(例:2022年01月01日午前0時に開始したい場合 → 202201010000)

7行目
RewriteCond %{TIME_YEAR}%{TIME_MON}%{TIME_DAY}%{TIME_HOUR}%{TIME_MIN} "<終了時間の設定"
カミングスーンページを適応させたい終了時間を設定してください。(例:2022年12月01日午前0時に終了したい場合 → 202212010000)

8行目
RewriteCond %{REQUEST_URI} !=/comming-soon.html
カミングスーンのページを設定してください。(デフォルトだとcomming-soon.htmlのファイルがカミングスーンとして表示されます)

9行目
RewriteCond %{REMOTE_ADDR} !8.8.8.8
カミングスーンページの表示を除外させる設定(自分のグローバルIPを設定すると自分のネットワークにはカミングスーンページが表示されなくなります)



■その他
わからない点がありましたらTwitterにて連絡ください!!
(@ofulusan)

作成日:2022/09/06
更新日:2022/09/07
