ロボットシステム学 課題1

---

## 概要 
  
  課題: 講義で作ったデバイスドライバを改造して、LEDやモータ、あるいはその他なにかデバイスを動かせるようにして、動かしている様子を動画に撮影する。
  (講義中に作成したドライバhttps://github.com/ryuichiueda/robosys_device_drivers/blob/master/myled.c)
  
---

## 動作環境
  
・Ubuntu 18.04  
  
---

## 用意したもの
  
  ・Raspberry Pi 4 Model B：1台  
  ・ブレッドボード：1個  
  ・青色LED：1個  
  ・ジャンパー線(M-M)：1本  
  ・ジャンパー線(M-F)：2本  
  ・抵抗220Ω：2個  
  
---

## インストール方法
  
  実行する手順は以下の通りです。  
  
  `$ git clone https://github.com/ryogakawamura/myled.git  `  
  `$ cd myled  `  
  `$ make  `  
  `$ sudo insmod myled.ko `  
  `$ sudo chmod 666 /dev/myled0  `  
  `$ sudo [0 or 1] > /dev/myled0  `  
  
---

## 使用方法

  `$ echo 0 > /dev/myled0  `：LED消灯  
  `$ echo 1 > /dev/myled1  `：LED点灯  
  
---

## デモ動画へのリンク
  
  https://youtu.be/qW_FI0jH4sk
  
---

## ライセンス
  
  GNU General Public License v3.0

---
