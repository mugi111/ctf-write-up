## 問題

Python scripts are invoked kind of like programs in the Terminal... Can you run `this Python script` using `this password` to get `the flag`?

### ファイル

`ende.py`
`pw.txt`
`flag.txt.en`

## 解法

`ende.py`を実行して、暗号化されたフラグファイル`flag.txt.en`を復号化する。
`-e`: 暗号化，`-d`: 復号化

```
python3 ende.py -d flag.txt.en
```
