## 問題

wabash, its a river, but also a new shell! Flag is in /flag.txt

## ファイル

## 解法

スペースが間に入ると`wa`が挿入される。
スペースを使わないようにすれば良さそう

どうやら`$IFS`で代用できるらしい

問題文に従って`cat /flag.txt`を実行すれば取得できる

文頭の`wa`を回避するために`|`で区切る

`|cat$IFS/flag.txt`
