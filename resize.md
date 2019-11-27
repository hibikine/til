# 画像のリサイズ

convertかmogrifyを使う

mogrifyは元ファイルを上書きする代わりにワイルドカードが使える(細かいことまでは調べてない)

```bash
# 幅1260以上の場合、幅1260に縮小
convert hoge.png -resize 1260x> hoge_min.png
```
