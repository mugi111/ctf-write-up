## 問題

Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: `this`

### ファイル

`doll.jpg`

## 解法

ダウンロードした`jpg`を見てみるとただのマトリョーシカの画像。
`exiftool`試す、特に異常なし。
`binwalk`で中身を見てみる。

```
binwalk dolls.jpg

DECIMAL       HEXADECIMAL     問題
--------------------------------------------------------------------------------
0             0x0             PNG image, 594 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378950, uncompressed size: 383938, name: base_images/2_c.jpg
651608        0x9F158         End of Zip archive, footer length: 22
```

Zip ファイルが紛れ込んでる。

取り出して繰り返すとフラグが書いてあるテキストファイルが出てくる。
