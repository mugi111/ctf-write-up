## 問題

Files can always be changed in a secret way. Can you find the flag? `cat.jpg`

### ファイル

`cat.jpg`

## 解法

`exiftool`でメタデータを確認。

```
exiftool cat.jpg
...
XMP Toolkit                     : Image::ExifTool 10.80
License                         : cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9
Rights                          : PicoCTF
...
```

License の値がおかしい
Base64 デコード
