

## 手順
```
#　ビルド
docker-compose build

# 起動
docker-compose up -d

# 停止
docker-compose stop
```

`./nginx/images`に適当な画像をいれる。


## 機能試し

- リサイズ(サイズ指定)
    - http://localhost:8000/small_light(dw=200,dh=200)/images/test1.jpg
- リサイズ(nginx内で指定したリサイズ仕様)
    - http://localhost:8000/small_light(p=small)/images/test1.jpg
- jpeg->webp変換
    http://localhost:8000/small_light(of=webp)/images/test1.jpg


## tips

### webpの確認

```
◯ osxの場合、以下のオプションを付けてimagemagickインストール
$ brew install imagemagick --with-webp

◯imagemagickでtest1.jpgのフォーマットを確認
$ identify test1.jpg
test1.jpg WEBP 1600x877 1600x877+0+0 8-bit sRGB 129KB 0.000u 0:00.000

```


## 参考

- https://github.com/cubicdaiya/ngx_small_light
