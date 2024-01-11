# udemy Laravel講座　第三弾

##　ダウンロード方法

git clone

git clone https://github.com/rei1091/laravel_uReserve

git clone ブランチを指定してダウンロードする場合

git clone -b ブランチ名 https://github.com/rei1091/laravel_uReserve

若しくはzipファイルでダウンロードして下さい

## インストール方法

-cd laravel_uReserve
-composer install
-npm install
-npm run dev

.env.exampleをコピーしてファイルを作成

.envファイルの中の下記をご利用の環境に合わせて変更してください。

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=laravel_ureserve
DB_USERNAME=ureserve
DB_PASSWORD=password123

XAMPP/MAMP又はほかの開発環境でDBを起動した後に、

php artisan migrate:flesh --seed

と実行して下さい。(データベーステーブルとダミーデータが追加されればOK)

最後にphp artisan key:generate
と入力してキーを生成後、

php artisan seve
で簡易サーバーを立ち上げ、表示確認して下さい。

##インストール後の実施事項

画像のリンク
php artisan storage:link

プロフィールページで画像アップロード機能を使う場合は、
.envのAPP_URLを下記に変更してください。

# APP_URL=http:/localhost
APP_URL=http://127.0.0.1:8000

Tailwindcss 3.xの、JustInTime機能により、
使ったHTML内クラスのみ反映されるようになっていますので、
HTMLをhwン周する際は、
npm run watchも実行しながら編集するようにして下さい。