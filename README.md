# robosys2023_ros2_mypkg
ロボットシステム学2023で制作したROS 2のパッケージです。

## ノード
![test](https://github.com/asutosato/robosys2023_ros2_mypkg/actions/workflows/test.yml/badge.svg)

### talker
数字をカウントしてトピック/countupを通じて送信する。

実行例
```
$ ros2 run mypkg talker        #端末1
 (なにも表示されない)

$ ros2 topic echo /countup     #端末2
data: 8 
---
data: 9
---
data: 10
---
・・・
```

### listener
/countupから受け取った数字を標準出力する。

実行例
```
$ ros2 run mypkg talker        #端末1
(なにも表示されない)

$ ros2 run mypkg listener     #端末2
[INFO] [1703490568.725823014] [listener]: Listen: 12
[INFO] [1703490569.080992382] [listener]: Listen: 13
[INFO] [1703490569.581275049] [listener]: Listen: 14
[INFO] [1703490570.080755689] [listener]: Listen: 15
・・・
```

## 必要なソフトウェア

## テスト環境
Ubuntu 20.04.5 LTS

## ライセンス
