---
title: "🛠 作業日報：OpenCVインストール奮闘記（macOS）"
date: 2025-06-04
---

## 📅 日付
2025年6月4日（水）

## 🧭 作業内容
Pythonで画像認識を学ぶため、OpenCVをmacOSにインストールする環境構築に挑戦。

---

## 🚩 今日の目的
- Pythonで「画像読み込み＋表示」を実行する
- OpenCV（`opencv-python`）をMacにインストールする

---

## 🔧 試した手順（ターミナル操作）

1. Homebrew で Python をインストール
- brew install python

2. pip3 が使えるか確認
- python3 --version
- pip3 --version

3. OpenCV のインストールに挑戦
- pip3 install opencv-python

4. ビルドエラーが発生 → 対処法として以下も実施
- pip3 install cmake
- pip3 install --upgrade setuptools wheel numpy

5. それでもビルド失敗 → `opencv-python-headless` も試すが同様にエラー

---

## ❌ 出たエラー（一部抜粋）

- `ERROR: Failed building wheel for opencv-python`
- `An error occurred while building with CMake`
- SDK や Foundation.framework 関連のコンパイルエラー

---

## 🔍 原因と考察

- 使用しているMacBookが11年前のモデル（macOS 11）
- Python 3.13 は `opencv-python` に未対応
- SDKやCommand Line Toolsの互換性も影響している可能性あり

---

## 🌱 振り返りと学び

- 環境構築は予想以上に難航。でも、原因を一つずつ特定して進めたことで、大きな学びに。
- 「環境が整わなくても、コードや考え方だけでも先に学べる」柔軟な視点を持てたのは収穫。
- 「一旦やめる」選択も前向きな判断だと実感。

---

## 🧘‍♀️ 今後の方針

- Python 3.11 環境を整えるか、Minicondaでの再挑戦を検討
- まずはミナリと一緒にコードの理解・練習を先に進めていく
- 中古ノートPCやクラウド環境での実行も選択肢に

---

## 💬 今日のひとこと

> 焦らず、一歩ずつ。うまくいかない日にも、学びと前進はある。


