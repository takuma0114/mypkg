## mypkg

![tesst](https://github.com/takuma0114/mypkg/actions/workflows/test.yml/badge.svg)

## 内容
* talker.pyというノードにパブリッシャを持たせて0.5秒周期でカウントし送信、listener.pyというノードにサブスクライバーを持たせて受信してターミナルにカウントを表示する。
* メッセージの型は16ビット符号付きの整数。

## 使用方法および使用例1
まず端末を2つ用意する。
それぞれの端末に以下のコードを入力する。
* 端末1（パブリッシャ）
```
$ ros2 run mypkg talker
```
* 端末2（サブスクライバー）
```
$ ros2 topic echo /countup
```
端末2に以下のように標準出力される。（一部表示）
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
それぞれの端末に以下のコードを入力する。
* 端末1（パブリッシャ）
```
$ ros2 run mypkg talker
```
* 端末2（サブスクライバー）
```
$ ros2 run mypkg listener
```
端末2に以下のように標準出力される。（一部表示）
```
[INFO] [1672490213.658525300] [listener]: Listen: 11
[INFO] [1672490214.158737700] [listener]: Listen: 12
[INFO] [1672490214.658751800] [listener]: Listen: 13
```

## 必要なソフトウェア
* ROS2
 * テスト済み

## 動作確認済み環境
* Ubuntu 22.04.1LTS

## 著作権とライセンスについて
* このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます。
* このパッケージのコードは，下記のスライド（CC-BY-SA 4.0 by Ryuichi Ueda）のものを，教育目的で本人の許可を得て自身の著作としたものです。
    * https://github.com/ryuichiueda/my_slides/tree/master/robosys_2022
* © 2022 Takuma Abe

