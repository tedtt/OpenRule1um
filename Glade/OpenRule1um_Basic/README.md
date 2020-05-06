OpenRule1um StdCells
=====

## これは何

* OpenRule1umで使えるスタンダードセル（基本論理ゲート）です。
* 各セルの内部は、OpenRule1umのルールに準拠していない（1umグリッドに載っていない）ものもありますが、外部接点となる電源・入出力端子は1umグリッドに載っています。

## セル一覧

* an21 : 2入力AND
* an31 : 3入力AND
* an41 : 4入力AND
* buf1 : バッファ(駆動力1)
* buf2 : バッファ(駆動力1x2)
* buf4 : バッファ(駆動力1x4)
* buf8 : バッファ(駆動力1x8)
* cinv : クロックト・インバータ
* dff1 : Dフリップフロップ(立ち下がりトリガ)
* dff1m2 : Dフリップフロップ(ML2使用)(立ち下がりトリガ)
* dff1_r : Dフリップフロップ(立ち上がりトリガ)
* dff1m2_r : Dフリップフロップ(ML2使用)(立ち上がりトリガ)
* exnr : Ex.NOR
* exor : Ex.OR
* inv1 : インバータ(駆動力1)
* inv2 : インバータ駆動力1x2
* inv4 : インバータ駆動力1x4
* inv8 : インバータ駆動力1x8
* na21 : 2入力NAND
* na212 : 2入力NAND+入力の内1つが2入力OR
* na222 : 2入力nand+入力2つ共2入力OR
* na31 : 3入力NAND
* na41 : 4入力NAND
* nr21 : 2入力NOR
* nr212 : 2入力NOR+入力の内1つが2入力AND
* nr222 : 2入力NOR+入力2つ共2入力AND
* nr31 : 3入力NOR
* or21 : 2入力OR
* or31 : 3入力OR
* rff1 : リセット付きDフリップフロップ(立ち下がりトリガ)
* rff1m2 : リセット付きDフリップフロップ(ML2使用)(立ち下がりトリガ)
* rff1_r : リセット付きDフリップフロップ(立ち上がりトリガ)
* rff1m2_r : リセット付きDフリップフロップ(ML2使用)(立ち上がりトリガ)
* sff1 : セット付きDフリップフロップ(立ち下がりトリガ)
* sff1m2 : セット付きDフリップフロップ(ML2使用)(立ち下がりトリガ)
* sff1_r : セット付きDフリップフロップ(立ち上がりトリガ)
* sff1m2_r : セット付きDフリップフロップ(ML2使用)(立ち上がりトリガ)
* dcont : diff<->ML1 接続
* pcont : POL<->ML1 接続
* nsubcont : NWL基板　バルク（バックバイアス）
* psubcont : Psub基板　バルク（バックバイアス）
* Via : ML1<->ML2 接続

* 使用上の注意など
1. セルは　外形（長方形）をFRAME Layerで表示しています。FRAMEがきれいに並んで隙間のないように、重ならないように並べて下さい。きれいに並べると、特別なことをしない限り、近接セル間では　デザインルールエラーにはなりません。またVDD, VSSは並べるだけで　セル間接続されます。念のためVDD, VSSのML1配線の外形もFRAME Layer で表しています。
2. セルは　0.5umグリッド格子点にセル(FRAME図形)の左下角を合わせておいて下さい。角を合わせると横幅方向・高さ方向ともに　0.5umグリッド格子の整数倍になります。
3. セルを並べる際に　隙間を意図的に空けたい場合には　セルFRAMEとセルFRAMEの間隔を1um上離して下さい。
4. セルへの接続はVDD, VSSはML1で行います。入力・出力は　端子名の記載されているML2のところに、ML2配線で接続してください。
5. VDD, VSSの上下方向の配線利用間隔は、セルのレイアウトにおいてはVDD, VSS共に　FRAMEの上下2グリッド離れたグリッドにML1もしくはML2の線幅1umのメタルで配線し、Viaを配置することで　エラーが出ないようにしています。

## Author

Junichi Akita (@akita11, akita@ifdl.jp)
Akihiro Yamada (A.LSI Design Co., Ltd.)