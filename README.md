# 測試將 Flask 佈署到 Heroku 上面去

步驟1-3是註冊Heroku帳戶，安裝命令列工具，並使用heroku login在local產生credentials。

1. 註冊[Heroku](https://www.heroku.com/)帳戶
2. 下載並安裝[Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli)
3. 在命令列上，執行heroku login

步驟4-5是建立虛擬環境，並編寫我們的程式。

4. 建立虛擬環境 (VirtualEnv)
5. 安裝必要的套件、寫好程式、測試程式是否可運行

步驟6-9是準備佈署上Heroku需要的東西。

6. 安裝 gunicorn (Heroku上面用來接收requests再轉到我們的App的套件)
7. 建立 runtime.txt (跟Heroku說明Python直譯器的版本)
8. 建立 Procfile (說明Heroku上面要怎麼執行我們的程式的設定)
9.  建立 requirements.txt (告訴Heroku我們安裝了那些套件，以及套件的版本)

步驟11-13是使用git管理我們的程式 (可以直接使用Visual Studio Code來做即可！)

10. 安裝 [git](https://git-scm.com/)
11. 初始化版本管理 (git init)
12. 將所有檔案加入版本管理系統 (git add .)
13. 將檔案放進檔案管理系統 (git commit -m "版本訊息")

步驟14除了在Heroku上面建立一個App之外，還會在版本管理系統中加入遠端的repo的連結，如此使用 git push 的時候，才能將檔案推上 Heroku 上面。

14. heroku create `App名稱` (也可以在Heroku上面設定AppName再用git remote add 加入遠端連結)
15. git push heroku master