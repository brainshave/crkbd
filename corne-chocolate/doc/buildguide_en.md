# Build Guide

This is the build guide for Corne Chocolate,
[the build guide for Corne Cherry is here (in Japanese)](https://github.com/foostan/crkbd/blob/master/corne-cherry/doc/buildguide_jp.md).

## Parts

### Required

| Name | Amount | Comment | 
|:-|:-|:-|
| PCB | 2 | reversible |
| top plate | 2 | |
| bottom plate | 2 | either PCB or acrylic plate |
| ProMicro protective plate | 2 | |
| ProMicro controller | 2 | |
| TRRS (jack) socket | 2 | |
| tact switch | 2 | |
| diode | 42 | チップ部品のみに対応 |
| Kailh Choc PCB sockets | 42 | |
| keyswitch | 42 | only "Choc" type |
| key cap | 42 | 1u * 40, 1.5u * 2 |
| OLED module | 2 | |
| 4-pin header | 2 | |
| 4-pin header socket | 2 | |
| M2 3.5mm stand-off | 10 | |
| M2 8mm stand-off | 4 | |
| M2 3mm screw | 28 | |
| cushion rubber | 8 | |
| 3-pole TRS cable | 1 | 4-pole cable works too |
| Micro USB cable | 1 | |

### Optional

| Name | Amount | Comment |
|:-|:-|:-|
| SK6812MINI | 54 | downward-facing 42, upward-facing 12 |

## Before Getting Started

It's probably best to start preparing your build environment for the ProMicro's firmware ahead of time. Some steps of installation take a bit of time so perhaps they can run while you're putting the keyboard together.

https://docs.qmk.fm/#/newbs_getting_started 

## Build

PCBs are reversible so decide now which one is going be the left and which is going to be the right one.

![01](https://user-images.githubusercontent.com/736191/52534345-dcce8b00-2d83-11e9-9b6a-b1f9f4b75519.png)

### Diodes

**Please solder diodes on the back side of the PCB.** It's important because otherwise they'll be interfering with the top plate. (This is different from Corne Cherry where they can be put on either side.)

It's recommened to handle diodes with tweezers because of their miniscule size. **Remember that electric current in diodes only goes one way**. To make it easier to orientate diodes correctly, align your PCBs like on the picture below.

![02](https://user-images.githubusercontent.com/736191/52534466-1b187a00-2d85-11e9-8ce3-bb13067a1b29.png)

Here's how to align diodes with the markings on PCB: the diode has a "|||" mark on one side. This side of the diode must be on the side where the "|" of the "|◁" mark on the PCB is. (picture borrowed from Corne Cherry guide)

![03](https://user-images.githubusercontent.com/736191/54487560-cb285800-48da-11e9-9e1e-aafaacf5723c.jpg)

Remeber how we aligned the boards two pictures back? Great, now put some solder on the right contact plate of each socket. (**on the "◁" side**, not the "|" side)

![04](https://user-images.githubusercontent.com/736191/52534531-0c7e9280-2d86-11e9-9636-ba582cdae265.png)

Now solder the diode to the contact plate we've just prepared. This is best done by holding the diode with reverse-action tweezers (so you don't have to use any force just to keep the diode in tweezers and you can concentrate on proper alignment). Remember that this time you're soldering on the umarked side of the diode, **not** the one with "|||" mark.

またはんだごてがあつすぎたり、はんだを触りすぎたりするとはんだに含まれるフラックスが気化してきれいにはんだの山ができることがありますが、あとで修復できるのでこの時点ではパーツを付けることだけを意識すれば大丈夫です。

![05](https://user-images.githubusercontent.com/736191/52534541-320b9c00-2d86-11e9-982c-45ec7f7b7741.png)

Now solder in the other side of the diode. Use only very small amount of solder. If you put in too much, take it out with desoldering wire or with the soldering iron.

![06](https://user-images.githubusercontent.com/736191/52534553-56677880-2d86-11e9-872e-ea374c8f6824.png)

If you put in too little solder, you can always add a bit more. If it piles up, try applying flux and heat it with soldering iron.

![07](https://user-images.githubusercontent.com/736191/52534577-b78f4c00-2d86-11e9-9c6d-64893dce2754.png)

### TRRS Sockets, Reset Buttons and 4-Pin Header Sockets

![08](https://user-images.githubusercontent.com/736191/52534580-bfe78700-2d86-11e9-9fa6-bdde5283af5b.png)

Solder the TRRS sockets, reset buttons and 4-pin header sockets to the **top** sides of PCBs. Remember that diodes go on the **bottom side**, so this is going to be the **opposite side from diodes**.

![09](https://user-images.githubusercontent.com/736191/52534621-40a68300-2d87-11e9-9749-14459d2b1eac.png)

### Jumpers for OLED Modules

To support OLED modules, make a jumper with solder between these 4 pairs of pins like on the picture, **on the top surface**.

![10](https://user-images.githubusercontent.com/736191/52534622-4d2adb80-2d87-11e9-8935-f7dc5fab4c38.png)

Put in enough solder to make a permanent jumper. If it doesn't work, flux that was in the solder might've evaporated. Apply more solder or add separate flux.

ジャンパがうまくいかない場合はおそらくはんだの量が少ないか、はんだに含まれるフラックスが気化してしまっています。
その場合は、はんだを多めに使うか、別途フラックスを塗るとうまくジャンパができます。

### ProMicro

![11](https://user-images.githubusercontent.com/736191/52534637-99761b80-2d87-11e9-958a-c6ca836a7936.png)

ピンヘッダを白い枠に当てはめるようにはんだづけし、そこにProMicroの裏面を上にしてはんだづけします。

![12](https://user-images.githubusercontent.com/736191/52534641-a266ed00-2d87-11e9-8dcb-832b90556ac2.png)
![13](https://user-images.githubusercontent.com/736191/52534643-aa269180-2d87-11e9-9c05-67924d235968.png)

なおスプリングピンヘッダを利用する場合は [Helix のビルドガイド](https://github.com/MakotoKurauchi/helix/blob/master/Doc/buildguide_jp.md#pro-micro)を参考にしてください。

### OLED Module

![14](https://user-images.githubusercontent.com/736191/52534716-4bade300-2d88-11e9-9fc4-e96787870d07.png)

OLED用のピンソケットにピンヘッダを先に差し込み、その後からピンヘッダとOLEDモジュールをはんだづけします。
このときOLEDモジュールが浮きやすいので指で押さえつけながら浮かないように気をつけます。

![15](https://user-images.githubusercontent.com/736191/52534720-5e281c80-2d88-11e9-9b76-164d9b63692f.png)
![16](https://user-images.githubusercontent.com/736191/52534722-67b18480-2d88-11e9-94d0-e3c899bcc020.png)

### 動作確認
ProMicroとOLEDモジュールを付けた段階で動作確認をすることをおすすめします(一番最後にやると問題の切り分けが難しくなる)。

動作確認をする場合は先に下記の「ファームウェア」の章を参考にしてcrkbd用のファームウェアをProMicroに入れてください（必ず両側に入れてください）。

動作確認は左手側はMicroUSBでPCとつなぎ、左手側と右手側をTRSケーブルで接続させて行います。ジャック等の不良等もありえるので、片方ずつではなく必ず左右を接続させてから動作確認をしてください。ここまで正しくできていれば、PCBソケットを取り付けるパッドをピンセット等でショートさせるとOLEDモジュールに押されたキーが表示されます。

![17](https://user-images.githubusercontent.com/736191/52534757-b95a0f00-2d88-11e9-9a81-467a9efbb935.png)

## LED（オプション）

![18](https://user-images.githubusercontent.com/736191/52534775-fd4d1400-2d88-11e9-8fcc-9916160a6478.png)

SK6812MINIを取り付けていきます。
なお、LEDの取り付けは完成後からでも行えるので、実装が心配な方はこの章を飛ばして、まずは完成させることをおすすめします。

SK6812MINIは非常に熱に弱く、簡単に壊れます。
温調機能がついたはんだごてを利用し、220℃ ~ 270℃ぐらいの温度で作業することをおすすめします。
また温度を調整しても長い時間コテをLEDに当てていると破損するので、なるべくすばやくはんだづけすることを心がけます。
LEDは４つずつはんだづけを行いますが、一度に４つ行わず、２つずつ行ってLEDの温度の上昇を防ぐと破損しづらくなるのでおすすめです。

まずは取り付ける位置の確認です。

1 ~ 6は裏面側(Undergrow)が光るようにし、7 ~ 27は表側（Backlight）が光るようにはんだづけを行います。下記がLEDを取り付ける位置です(画像はCorne Cherryから転記)。

![19](https://user-images.githubusercontent.com/736191/46822561-c6f58d00-cdc6-11e8-90d4-de015410a7a4.png)
![20](https://user-images.githubusercontent.com/736191/46822569-cc52d780-cdc6-11e8-9602-f6265a2c876d.png)

1 ~ 6 は下記のように丸印で囲った黒い部分を下にしたとき、矢印で示したシルクの目印が上になるようにはんだづけを行います。
1 ~ 3 と 4 ~ 5 で向きが変わるので注意してください。

![21](https://user-images.githubusercontent.com/736191/46822428-6d8d5e00-cdc6-11e8-8858-06e8dbdb8ee8.png)

7 ~ 27 は下記のように、丸印で囲った一番大きなパッドと、矢印で示したシルクの目印が隣り合うようにはんだづけを行います。

![22](https://user-images.githubusercontent.com/736191/46822434-6ebe8b00-cdc6-11e8-9686-69ac88bb4389.png)

すべて正常にはんだづけができれば下記のように光ります。
もし途中までしか光らない場合は数字の順番でLEDがつながっているので、光らないLEDもしくはその前のLEDのはんだづけミスやLEDの破損を疑ってください。

![23](https://user-images.githubusercontent.com/736191/52534803-751b3e80-2d89-11e9-9588-75576942ba46.png)
![24](https://user-images.githubusercontent.com/736191/52534807-7c424c80-2d89-11e9-9580-0daffc862ebb.png)
![25](https://user-images.githubusercontent.com/736191/52534811-85331e00-2d89-11e9-9752-c40ffab23419.png)

### Kailh PCBソケット
![26](https://user-images.githubusercontent.com/736191/52534832-be6b8e00-2d89-11e9-82e6-be53dd82bf59.png)

裏面の両側のパッドにはんだを盛ります。後から追加するのが難しいので予め多めに盛ってください。

![27](https://user-images.githubusercontent.com/736191/52534834-c75c5f80-2d89-11e9-987e-d1ca43cf6bc3.png)

ソケットをはめこみ、持ったはんだを溶かすようにして取り付けます。
このときソケットが浮かないようにピンセットや指で押さえつけながら行います。

![28](https://user-images.githubusercontent.com/736191/52534839-d0e5c780-2d89-11e9-8579-d6967b801229.png)

はんだづけはこれで完了です。

![29](https://user-images.githubusercontent.com/736191/52534855-05f21a00-2d8a-11e9-8a63-a9f8b09a730a.png)
![30](https://user-images.githubusercontent.com/736191/52534859-0c809180-2d8a-11e9-959a-83c58da83844.png)

### プレート、スイッチ

![31](https://user-images.githubusercontent.com/736191/52534879-55384a80-2d8a-11e9-9648-e9e9b81625c1.png)

トッププレートとボトムプレート用のスペーサーは3.5mm、OLED用のスペーサーは8mmを使用します。

![32](https://user-images.githubusercontent.com/736191/52534882-67b28400-2d8a-11e9-987d-00b5e14a8f2c.png)

なおプレートの側面を黒のマジックで塗りつぶすと見栄えが良くなるのでおすすめです。

![33](https://user-images.githubusercontent.com/736191/52534914-00e19a80-2d8b-11e9-8005-7e0b157e09e4.png)

## ファームウェア
https://docs.qmk.fm/#/newbs_getting_started こちらを参照して頂き、ファームウェアを書き込む環境を用意します。

環境ができましたら、下記コマンドで Crkbd 用にファームウェアをビルドします。

```
make crkbd:default
```

ビルドが完了したら下記コマンドを実行します。

```
make crkbd:default:avrdude
```

実行すると下記のようなログがでて、`.` が増えていくことが確認出来ると思います。
この間にリセットスイッチを **2回** 押すとファームウェアの書き込みが完了します。

```
<省略>

Checking file size of crkbd_rev1_default.hex                                                        [OK]
 * File size is fine - 27328/28672
Copying crkbd_rev1_default.hex to qmk_firmware folder                                               [OK]
Detecting USB port, reset your controller now........
```

片側のProMicroにファームウェアの書き込みが完了したら、もう片方も同じ手順で書き込みを行います。

以上で完成です。

![34](https://user-images.githubusercontent.com/736191/52534969-be6c8d80-2d8b-11e9-82ac-a2cd09ab96d1.png)



