* 列出現有的 screen

     screen -r

* 強制進入已被 attach 的 screen
    
     screen -r -x

* 下一個 screen

     **Ctrl** + a + n 

* 上一個 screen

     **Ctrl** + a + p 

* 離開 screen

     **Ctrl** + a + d 

* ???

     **Ctrl** + a + a

* 將已開啟的 screen 以選單方式呈現 ???

     **Ctrl** +  a + **Shift-**

* split screen

     **Ctrl** +  a + S

* 切換 screen

     **Ctrl** +  a + **Tab**

* 關掉 screen

     **Ctrl** +  a + Q




sudo apt-get install screen
screen -q

接下來，用 vi 隨便編輯一個檔案或執行 top 指令，之後，請按下「Ctrl - A」，然後，再按下一個 「c」，這樣，就會建立並切換到一個新的虛擬終端機上，接著，再按一次「Ctrl - A」之後，再按一個「n」，畫面就會切回剛剛的 vi 編輯畫面或 top 畫面了哩 ! 有沒有覺得很方便.... ^^=

所以，當要同時用多個終端機來操作的時候，也就可以用上面提到的方式在一個終端機上建立二個以上的虛擬終端機來操作和切換哩 ! 阿舍用過後，覺得比開多個實體的終端機畫面來的容易和快速哩 !

下面是前面提到的操作方式的相關鍵盤操作的說明，screen 可以做的事很多，不過，阿舍說的這個方式是最實用的，更多的 screen 指令說明請參考 這篇 和 這篇 ，都有詳細的說明哩 ! ^^=

Ctrl - A  :  screen 的所有操作都要先按下 Ctrl- A 後，再按下面的字母按鍵來操作的。
c  : 建立並切換到新終端機。
n  : 切換到下一個終端機。
p  : 切換到上一個終端機。
?  : 顯示指令和按鍵說明。
\   : 結束 screen 程式。 

Read more: http://www.arthurtoday.com/2013/12/ubuntu-screen-quickly-switch-between-terminals.html#ixzz43jPABNnj