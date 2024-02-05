# mypkg
* ![test](https://github.com/tompsonpiano/ros2_ws/actions/workflows/test.yml/badge.svg)

ロボットシステム学の練習用ディレクトリです。

ROS2のノード通信により、talkerが発信した内容をlistenerが受け取ります。

## インストール方法
```
# ROS2内のsrcディレクトリで以下のコマンドを実行し、リポジトリをダウンロードしてください
git clone https://github.com/tompsonpiano/mypkg.git

# パッケージのビルド
cd ~/ros2_ws
colcon build
source devel/setup.bash
```

## 使用方法
本ソフトウェアの使用にはターミナルを二つ開く必要があります。
片方のターミナルには以下のコマンドを、
```
ros2 run mypkg talker
```

もう片方のターミナルには以下のコマンドを入力してください
```
ros2 run mypkg listener
```

talkerを実行したターミナルには何も表示されませんが、listenerには以下のような表示がされます。
```
...
[INFO] [1707039923.484239559] [listener]: Listen: 7
[INFO] [1707039923.976229233] [listener]: Listen: 8
[INFO] [1707039924.476286816] [listener]: Listen: 9
[INFO] [1707039924.976169939] [listener]: Listen: 10
[INFO] [1707039925.476523051] [listener]: Listen: 11
[INFO] [1707039925.976315101] [listener]: Listen: 12
[INFO] [1707039926.476422452] [listener]: Listen: 13
...
```


## 必要なソフトウェア
* Python 3
* ROS 2 foxy または ROS 2 humble

## テスト環境
* Ubuntu 20.04 LTS
* Ubuntu 22.04 LTS


## ライセンス
* このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます．
* このパッケージのコードは，下記のスライド（CC-BY-SA 4.0 by Ryuichi Ueda）のものを，本人の許可を得て自身の著作としたものです．
* [ryuichiueda/my_slides/robosys_2022](https://github.com/ryuichiueda/my_slides/tree/master/robosys_2022)
* © 2023 Tomohiro Hayashi