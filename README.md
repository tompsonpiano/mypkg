# mypkg
![test](https://github.com/tompsonpiano/ros2_ws/actions/workflows/test.yml/badge.svg)

ロボットシステム学の練習用パッケージです。

ROS 2のノード通信により、パブリッシャー(talker)が発信した内容をサブスクライバー(listener)が受け取り表示します。

# 使用方法
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
    ...
```
# ノード
本パッケージには以下の2つのノードが含まれます。



## talker
本ノードはcountupトピックを通して、カウントした数字を発信するパブリッシャです。

以下のコマンドで実行できます。
```
$ ros2 run mypkg talker
```
なお、実行してもターミナルには何も表示されません。

## listener
本ノードはcountupトピックを受信し、パブリッシャが配信した数字を表示するサブスクライバです。

以下のコマンドで実行できます。
```
$ ros2 run mypkg listener
```

2つのターミナルでtalker.pyとlistener.pyをそれぞれ実行すると、以下のように表示されます。
```
...
[INFO] [1707039923.484239559] [listener]: Listen: 7
[INFO] [1707039923.976229233] [listener]: Listen: 8
[INFO] [1707039924.476286816] [listener]: Listen: 9
[INFO] [1707039924.976169939] [listener]: Listen: 10
...
```

# talk_listen.launch.py
本プログラムは一つのターミナル内でtalkerとlistenerを実行することができます。

以下のコマンドで実行できます。
```
$ ros2 launch mypkg talk_listen.launch.py
```

実行されると、以下のように表示されます。
```
...
[listener-2] [INFO] [1709293046.146829839] [listener]: Listen: 1
[listener-2] [INFO] [1709293046.646651069] [listener]: Listen: 2
[listener-2] [INFO] [1709293047.146969288] [listener]: Listen: 3
[listener-2] [INFO] [1709293047.646416228] [listener]: Listen: 4
...
```


# 必要なソフトウェア
* Python 3
* ROS 2 
    * foxy (Ubuntu 20.04) または humble (Ubuntu 22.04)

# テスト環境
* Ubuntu


# ライセンス
* このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます．
* このパッケージのコードは，下記のスライド（CC-BY-SA 4.0 by Ryuichi Ueda）のものを，本人の許可を得て自身の著作としたものです．
    * [ryuichiueda/my_slides/robosys_2022](https://github.com/ryuichiueda/my_slides/tree/master/robosys_2022)

© 2023 Tomohiro Hayashi