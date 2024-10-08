# Laravel 11 從 Eloquent 模型自動產生模型工廠

引入 thedoctor0 的 laravel-factory-generator 套件來擴增從 Eloquent 模型自動產生模型工廠，方便產生大量的資料庫記錄。

## 使用方式
- 把整個專案複製一份到你的電腦裡，這裡指的「內容」不是只有檔案，而是指所有整個專案的歷史紀錄、分支、標籤等內容都會複製一份下來。
```sh
$ git clone
```
- 將 __.env.example__ 檔案重新命名成 __.env__，如果應用程式金鑰沒有被設定的話，你的使用者 sessions 和其他加密的資料都是不安全的！
- 當你的專案中已經有 composer.lock，可以直接執行指令以讓 Composer 安裝 composer.lock 中指定的套件及版本。
```sh
$ composer install
```
- 產生 Laravel 要使用的一組 32 字元長度的隨機字串 APP_KEY 並存在 .env 內。
```sh
$ php artisan key:generate
```
- 執行 __Artisan__ 指令的 __migrate__ 來執行所有未完成的遷移。
```sh
$ php artisan migrate
```
- 執行 __Artisan__ 指令的 __generate:model-factory__ 來執行既有的 Eloquent 模型自動產生模型工廠假資料設定。
```sh
$ php artisan generate:factory {--force/recursive/dir 模型目錄/namespace 客製命名空間}
```
- 執行 __Artisan__ 指令的 __db:seed__ 來執行資料庫填充。
```sh
$ php artisan db:seed
```

----

## 畫面截圖
![](https://i.imgur.com/FO2Y62t.png)
> 執行既有的 Eloquent 模型自動產生模型工廠假資料設定

![](https://i.imgur.com/kNJFVfI.png)
> 建立 10 筆公司

![](https://i.imgur.com/74Ohp0c.png)
> 建立 50 位使用者，並為每個用戶建立一個公司關聯
