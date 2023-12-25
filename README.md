# robosys2023_ros2_mypkg
ロボットシステム学2023で制作したROS 2のパッケージです。

![test](https://github.com/asutosato/robosys2023_ros2_mypkg/actions/workflows/test.yml/badge.svg)

## ノード

### talker
数字をカウントしてトピックを通じて送信する。

### listener
トピックから受け取った数字を標準出力する。

## トピック

### countup
talkerから送られた信号をlistenerに送る。
メッセージの型は16ビット符号付き整数を使用する。

## 実行例
talkerとlistenerを二つの端末で個別に立ち上げる。

```
#端末1
$ ros2 run mypkg talker
(なにも表示されない)

#端末2
$ ros2 run mypkg listener
[INFO] [1703490568.725823014] [listener]: Listen: 12
[INFO] [1703490569.080992382] [listener]: Listen: 13
[INFO] [1703490569.581275049] [listener]: Listen: 14
[INFO] [1703490570.080755689] [listener]: Listen: 15
・・・
```

launchファイルを使用してtalkerとlistenerを一つの端末で立ち上げる。

```
$ ros2 launch mypkg talk_listen.launch.py
[listener-2] [INFO] [1703496258.256578689] [listener]: Listen: 0
[listener-2] [INFO] [1703496258.746302212] [listener]: Listen: 1
[listener-2] [INFO] [1703496259.246264140] [listener]: Listen: 2
[listener-2] [INFO] [1703496259.745889194] [listener]: Listen: 3
[listener-2] [INFO] [1703496260.246123046] [listener]: Listen: 4
```

## 必要なソフトウェア

## テスト環境
Ubuntu 20.04.5 LTS

## ライセンス
* このソフトウェアパッケージは、3条項BSDライセンスの下、再配布および使用が許可されます。
* このパッケージのコードの一部は、下記のスライド(CC-BYSA 4.0 by Ryuiti Ueda)のものを本人の許可を得て自身の著作としたものです。

©2023　Asuto Sato
