## 問題

There is a nice program that you can talk to by using this command in a shell: `$ nc mercury.picoctf.net 21135`, but it doesn't speak English...

## 解法

```
nc mercury.picoctf.net 21135
```

実行すると改行区切りの数字の羅列が返ってくる。
Ascii 10 進数でデコードするとフラグになる。
