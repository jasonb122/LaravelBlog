# Project Title

> 前言:
    看到測驗內容後，評估公司未來是使用laravel框架，雖然之前沒有接觸過，但是嘗試使用該框架搭配一些網路教學寫出該專案，
    但是因為尚在初學階段，所以該專案目前我是使用框架原本的MVC架構，尚未做前後端分離。


> 名稱:LaravelBlog

> 簡介:有基本布告欄CRUD以及用戶註冊登入

## Getting Started 
项目使用条件、如何安装部署、怎样运行使用以及使用演示

使用條件:安裝PHP、MYSQL

1.根目錄env檔內有設定好DB位置名稱，可根據設定檔創建laravel_blog資料庫或是根據個人本地設置做調整  
2.執行 php artisan migrate生成相應資料表  
3.在專案底下輸入 php artisan serve指令啟動專案  

### Usage example 


1/網址輸入:
http://127.0.0.1:8000/
會進入laravel預設歡迎頁

2.右上角有login及register，初次進入用戶請點擊register

3.此功能為laravel內建，只有初步做資料格式檢查。

4.註冊登入後點擊左上角公佈欄，於畫面中間會看到我要貼文按鈕，可以進行新貼文創建，送出後可以針對該文做編輯刪除操作

5.點擊公佈欄即可回到部落格列表






## API Introduction

### 新增文章  
Api Url：/post  
Api呼叫方式：post 

| Body參數 | 格式 | 必填 | 說明 |
| :----: | :----: | :----: | :----: |
| _token | string | Required | 登入取得的Token |
| title | string | Required | 文章標題 |
| content | string | Required | 文章內容 |


### 取得文章內容
Api Url：/post/文章ID/edit
Api呼叫方式：get

### 更新文章
Api Url：/post/文章ID
Api呼叫方式：post

| Body參數 | 格式 | 必填 | 說明 |
| :----: | :----: | :----: | :----: |
| _token | string | Required | 登入取得的Token |
| _method | string | Required | 輸入PUT |
| title | string | Required | 文章標題 |
| content | string | Required | 文章內容 |

### 刪除文章  
Api Url：/post  
Api呼叫方式：post 

| Body參數 | 格式 | 必填 | 說明 |
| :----: | :----: | :----: | :----: |
| _token | string | Required | 登入取得的Token |
| _method | string | Required | 輸入DELETE |


### 取得文章列表  
Api Url：/post
Api呼叫方式：post 

| Body參數 | 格式 | 必填 | 說明 |
| :----: | :----: | :----: | :----: |
| _token | string | Required | 登入取得的Token |