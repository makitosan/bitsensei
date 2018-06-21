---
description: ARM社製のDAPLinkが組み込まれている
---

# micro:bit の USB について

## micro:bit の USB デバイス情報

ARM社製の [DAPLink](https://github.com/ARMmbed/DAPLink) が組み込まれている。これによりドラッグアンドドロップでのファームウェアの書き換えが可能になっている。Macの場合（Windowsは未確認）USBでmicro:bitを接続すると、デバイスとして「MICROBIT」が認識されるがこの文字列をどこから取得しているのかは不明。

### USB デバイス情報詳細

* 製品ID 0x0204
* 製造元ID 0x0d28

上記2つのIDは複数の micro:bit で一致し、シリアル番号は各 micro:bit によって異なることは確認した。

## WebUSB を使用した検証

Chrome v61 からWebUSB が使用できる。micro:bit を使ってブラウザ上でユーザーを認証することも技術的には可能。

