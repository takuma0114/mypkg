## ros2

![test](https://github.com/takuma0114/robosys202x/actions)

## インストール方法
```
$ git clone https://github.com/takuma0114/robosys202x.git
$ cd ros2_ws
```

## 内容
talker.py（パブリッシャ）で0.5秒周期でカウントし送信、
listener.py（サブスクライバー）で受信してターミナルにカウントを表示する。

## 使用方法および使用例1
まず端末を2つ用意する。
* 端末1
```
$ ros2 run mypkg talker
```
* 端末2
```
$ ros2 topic echo /countup
```
```
data: 11
---
data: 12
---
data: 13
---
```

## 使用方法および使用例2
まず端末を2つ用意する。
* 端末1
```
$ ros2 run mypkg talker
```
* 端末2
```
$ ros2 run mypkg listener
```
```
[INFO] [1672490213.658525300] [listener]: Listen: 11
[INFO] [1672490214.158737700] [listener]: Listen: 12
[INFO] [1672490214.658751800] [listener]: Listen: 13
```

## 必要なソフトウェア
* python3.7～3.10
 * テスト済み

## 動作確認済み環境
* Ubuntu 22.04.1LTS

## 著作権とライセンスについて
* このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます。
* このパッケージのコードは，下記のスライド（CC-BY-SA 4.0 by Ryuichi Ueda）のものを，教育目的で本人の許可を得て自身の著作としたものです。
* https://github.com/ryuichiueda/my_slides/tree/master/robosys_2022
* © 2022 Takuma Abe

