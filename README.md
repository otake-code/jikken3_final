# 徘徊高齢者検知システム

このプロジェクトは、Pythonで開発された徘徊高齢者検知システムです。
このシステムはjetson nanoのような小型デバイスを玄関口に置くことで徘徊高齢者が外出するのを防ぐためのものです。

## 機能

- 指定された高齢者の顔を埋め込みベクトル化
- カメラで顔を検知し、顔識別を行う
- コサイン類似度を使用して顔の一致を判定
- 本人であれば、家族にLINE通知を送信
- 本人であれば、SWITCHBOTロックを施錠

## 使用技術

- モデルにはVGG16を使用
- 顔切り取りにはOpenCVを使用

## インストール

1. このリポジトリをクローンします。
```
git clone https://github.com/otake-code/jikken3_final.git
```
2. 必要なPythonライブラリをインストールします。

## 使用方法
1. LINE notifyとswitchbotのAPIを設定します

2. 認証したい顔をベクトル化します
```
python embedding_arcface.py
```
  
3. 顔認証を実行します。
```
python predict_aki.py
```
4. システムがカメラを起動し、顔を検知します。
5. 指定された高齢者の顔との一致を判定します。
6. 本人であれば、LINE通知が送信され、SWITCHBOTロックが施錠されます。

## 今後の改善予定

- より高度な顔認証技術の導入
- カメラの精度や安定性の向上
- システムの柔軟性やカスタマイズ性の向上

## 貢献

- バグの報告や改善提案は、Issueを作成してください。
- 新しい機能の提案や開発への参加は、Pull Requestを送信してください。

## 作者

- [otake-code](https://github.com/your_username)
