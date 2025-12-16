# ケーブル接続（表＋ラベル）

> **No順に刺せば完成**するように並べます。会場ごとの差分は「備考」に追記。  
> ラベルは「両端」に貼る（V/A/U いずれも）。

## 0) 事前：ラベル貼り
- 映像：`V1` `V2` `V3` `V4` `V5`
- 音声：`A1` `A2`
- USB：`U1` `U2` `U3` `U4`

---

## 1) 映像（スライド：ATEM経由）
|No|From|To|ケーブル/変換|ラベル|備考|
|---:|---|---|---|---|---|
|V1|Windows PC（PowerPoint）|ATEM HDMI IN1|HDMI|V1|スライド映像＋PC音声|
|U1|ATEM USB-C|Anker343 USB-C → Mac USB-C|USB-C|U1|Macで「ATEM」がカメラとして見える|
|V2|ATEM HDMI OUT|kksmart モバイルモニター|HDMI|V2|Multiview/プレビュー用|

---

## 2) 映像（カメラ：iPad→HDMIキャプチャ→Mac）
|No|From|To|ケーブル/変換|ラベル|備考|
|---:|---|---|---|---|---|
|V4|iPad Pro（USB-C）|USB-C→HDMIアダプタ|変換|V4|iPad側の出力方式を固定|
|V5|USB-C→HDMIアダプタ|HDMIケーブル|HDMI|V5|—|
|U2|HDMIケーブル|HDMI→USB-Aキャプチャ → Anker343 USB-A → Mac|キャプチャ|U2|Macで「USB Capture」等として認識|

> ※記載の「HDMIメス→USB typeA 変換アダプタ」は **HDMIキャプチャ（UVC）** として扱う（名称・型番は追記推奨）。

---

## 3) 音声（会場→AG06）
|No|From|To|ケーブル/変換|ラベル|備考|
|---:|---|---|---|---|---|
|A1|演台システム 音声OUT|AG06 入力5/6（RCA）|RCA 20m|A1|会場側の出力レベルを確認|

## 4) 音声（卓上/補助：AT2050→AG06）
|No|From|To|ケーブル|ラベル|備考|
|---:|---|---|---|---|---|
|A2|AT2050 マイク|AG06 入力1（XLR）|XLR 15m|A2|48Vファンタム要否は運用で固定|

## 5) AG06→Mac（USB）
|No|From|To|ケーブル|ラベル|備考|
|---:|---|---|---|---|---|
|U3|AG06 USB|Mac USB-C（直 or Hub）|USB|U3|音声入力デバイスをAG06に|

## 6) Mac→FlipGo（外部モニター）
|No|From|To|ケーブル|ラベル|備考|
|---:|---|---|---|---|---|
|V3|Mac HDMI OUT|FlipGo Pro（miniHDMI）|HDMI→miniHDMI|V3|画面拡張（監視/操作）|

## 7) ClickShare（会場投影）
|No|From|To|ケーブル|ラベル|備考|
|---:|---|---|---|---|---|
|U4|Mac USB-C|ClickShare 無線アダプタ|USB-C|U4|会場の運用（アプリ/権限）に従う|

---

## 8) 参考（接続写真）
- 配信卓：`assets/photos/desk_setup.jpg`
- AG06：`assets/photos/ag06_ports.jpg`
