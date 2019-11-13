# FindとFFMPegを一緒に使う

大量のwavファイルを16bit, 44100Hz, ステレオに変換したい

```bash
find . -name "*.wav" -print0 | xargs -0 -I {} ffmpeg -ac 2 -ar 44100 -acodec pcm_s16le {}
```

* findで `-print0` する理由([findとxargsコマンドで-print0オプションを使う理由(改)](https://qiita.com/maskedw/items/2dfdf6fa7eee991ddc45))
* xargsのIオプションを知った([xargs のオプションいろいろ](https://qiita.com/hitode7456/items/6ba8e2d58f9b8db9de11))
* ffmpegべんり([最新ffmpegのオプションまとめ](http://mobilehackerz.jp/archive/wiki/index.php?%BA%C7%BF%B7ffmpeg%A4%CE%A5%AA%A5%D7%A5%B7%A5%E7%A5%F3%A4%DE%A4%C8%A4%E1#lc678013))
