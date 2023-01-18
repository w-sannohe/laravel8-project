# laravel8-project
laravel8
  
### 実際に使いたい時  
[タグ](https://github.com/w-sannohe/laravel8-project/tags)から最新をダウンロードするといいよ  
他に困ったことやビルド方法は[こちら](https://github.com/w-sannohe/php-project-php7)  
  
### もし`laravel8-project`のディレクトリ名を変えたい時  
ディレクトリ名変えるとエラーになるので、、、、  
laravelを再構築するといいよ  
(もしかしたらprojectを変えるといいのかな？今度試してみよう〜)  
  
```
$ pwd
laravel8-project // laravel8-projectにいると想定
// project配下を全削除
$ rm -rf project/
// 名前変更
$ cd ../
$ mv laravel8-project 変えたいディレクトリ名 
// laravelを再構築
$ cd 変えたいディレクトリ名 
$ docker-compose up --build
$ docker exec -it laravel8-project-php_1 /bin/bash // laravel8-project-php_1はphpコンテナ名(もし違ったらdocker psで確認)
$ composer create-project --prefer-dist "laravel/laravel=8.*" .
$ php artisan -v
Laravel Framework 8.*.* // 8のバージョンが表示されたら成功
```  
