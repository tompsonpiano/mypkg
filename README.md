# mypkg
* ![test](https://github.com/tompsonpiano/ros2_ws/actions/workflows/test.yml/badge.svg)

ロボットシステム学の練習用パッケージです。

ROS 2のノード通信により、パブリッシャー(talker)が発信した内容をサブスクライバー(listener)が受け取り表示します。

本パッケージに含まれるノードは"countup"と呼ばれるトピックを使用して通信が行われます。

## 使用方法
本パッケージを、ROS 2のワークスペースのsrcに以下のように配置してください。
```
...
└── src
    ├── mypkg       #本パッケージ
    │   ├── LICENSE
    │   ├── README.md
    │   ├── launch
    │   │   └── ...
    │   ├── ...
```
```
ros2 run mypkg talker
```

サブスクライバーのターミナルには以下のコマンドを入力してください
```
ros2 run mypkg listener
```

実行すると、パブリッシャーのターミナルには何も表示されませんが、サブスクライバーには以下のような表示がされます。
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
* ROS 2 
    * foxy または humble

## テスト環境
* Ubuntu


## ライセンス
* このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます．
* このパッケージのコードは，下記のスライド（CC-BY-SA 4.0 by Ryuichi Ueda）のものを，本人の許可を得て自身の著作としたものです．
    * [ryuichiueda/my_slides/robosys_2022](https://github.com/ryuichiueda/my_slides/tree/master/robosys_2022)
© 2023 Tomohiro Hayashi