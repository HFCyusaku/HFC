# ソフトウェア設定（Mac / ATEM / iPad / Windows）

## 0) ソフト一覧（想定）
- Mac：OBS（配信/録画）, Zoom（会議/配信）, ATEM Software Control（必要時）, ClickShareアプリ（会場方式による）
- iPad：Blackmagic Cam
- Windows：PowerPoint

---

## 1) ATEM Mini Pro（スライド入力）
### 1-1. 入力割当（今回）
- IN1 = Windows（PowerPoint）
- HDMI OUT = Multiview（kksmartへ）
- USB-C = MacへUVC（Webカメラとして認識）

### 1-2. 推奨（運用で固定）
- フレームレート：30fps（会場・配信先に合わせて）
- スイッチャ設定：音声Follow/固定のどちらを使うかを決め打ち

---

## 2) iPad（Blackmagic Cam）
- 出力解像度：1080p（可能なら）
- 露出/ホワイトバランス：会場でブレないように「オート固定」か「マニュアル固定」を選ぶ
- 取り込み：HDMIキャプチャを経由し、Macで別映像入力として扱う

---

## 3) YAMAHA AG06MK2
### 3-1. 入力（今回）
- CH1（XLR）：AT2050（A2）
- CH5/6（RCA）：演台システム音声OUT（A1）

### 3-2. サンプリング
- 48kHz（Mac/OBS/Zoomも合わせる）

### 3-3. レベル目安
- 通常会話：OBSメータで -18〜-12 dB 付近
- ピーク：-6 dB を超えない（クリップ防止）

> 参考：AG06のポート周り `assets/photos/ag06_ports.jpg`

---

## 4) Mac（配信）
### 4-1. デバイス（共通）
- 音声入力：AG06MK2
- 映像入力：用途により2種類
  - `ATEM Mini Pro`（スライド系）
  - `USB Capture`（iPad系）

### 4-2. OBS（使う場合）
- 解像度：1920x1080 / FPS：30 / 音声：48kHz
- ソース例：
  - `ATEM`（スライド）
  - `iPad Capture`（カメラ）
  - `PIP`（必要なら）
- 録画：本番は **必ずローカル録画もON**（配信トラブル対策）

### 4-3. Zoom（使う場合）
- カメラ：OBS Virtual Camera もしくは ATEM（運用で固定）
- マイク：AG06MK2
- 設定（自動音量調整/ノイズ抑制）は「毎回同じ」に固定（品質ブレ防止）

---

## 5) Windows（PowerPoint）
- 出力解像度：1920x1080 推奨
- 画面スケーリング：100%（ズレ防止）
- スリープ/省電力：OFF（本番中に落ちない）

---

## 配信開始チェック（最重要）
- [ ] ATEM（U1）がMacでカメラとして見える（スライドが映る）
- [ ] HDMIキャプチャ（U2）がMacで見える（iPad映像が映る）
- [ ] 音声入力がAG06で、メータが動く（CH1/CH5/6）
- [ ] クリップしていない（ピーク -6dB以内）
- [ ] ClickShareで会場投影OK（U4）
- [ ] FlipGoで監視しながら操作できる
