# 配信オペレーションマニュアル（Draft v2）

このリポジトリは、**持ち込み配信機材**＋**会場設備（プロジェクター/音響/無線マイク）**を前提に、
設営〜配信〜撤収までを **再現性高く** 回すための Runbook＋設計資料です。

- 対象：フラットチャンネルの月例ハイブリッド運用（想定）
- 更新方針：当日運用で気づいた点は `docs/80_change_log.md` に追記 → 次回に反映

## Quick Start（最短で本番まで）
1. `docs/60_runbook_dayof.md` を上から実行（設営）
2. `docs/40_software.md` の「配信開始チェック」を通す
3. `docs/70_troubleshooting.md` を手元に開いた状態で本番開始

## 今回の構成の要点（機材/経路）
- 映像（スライド）：**Windows PC → ATEM Mini Pro（HDMI IN1）→ Mac（USB-C / UVC）**
- 映像（カメラ）：**iPad Pro → USB-C→HDMI → HDMI→USB-Aキャプチャ → Mac（Anker343経由）**
- 音声（会場）：**演台システム OUT → AG06（CH5/6 RCA）→ Mac（USB）**
- 音声（卓上/会場近接）：**AT2050 → AG06（CH1 XLR）**
- 会場投影：**Mac → ClickShare（USB-C）→ プロジェクター**
- モニタ：
  - **kksmart 13.3"**：ATEM HDMI OUT（ATEMプレビュー用）
  - **FlipGo Pro**：Mac HDMI出力（操作用）

## まず読むドキュメント
- 全体像：`docs/00_overview.md`
- 構成図：`docs/10_system_architecture.md`
- ケーブル接続：`docs/30_cabling.md`
- 当日Runbook：`docs/60_runbook_dayof.md`

## 参考写真
- 配信卓：`assets/photos/desk_setup.jpg`
- AG06（ポート周り）：`assets/photos/ag06_ports.jpg`

## 公開時の注意（GitHub）
- SSID/パスワード、会場担当者の個人情報、Zoom/配信URL、録画保存先の個人情報などは **記載しない**。
- 設定ファイルのコミットは「公開可能な範囲」に限定（例：配信キーはNG）。
