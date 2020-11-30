
# LSTMを用いた自動音楽生成
目的：VAEよりも表現の幅を求める。LSTMニューラルネットワークアーキテクチャを用いて、入力楽曲のデータの特徴を捉えた音楽を生成する。

jupyter notebookが表示されないときは nbviewer(https://nbviewer.jupyter.org/)で見る。


## LSTM（Long Short-Term Memory）とは
LSTMはRNNの中間層のユニットをLSTM blockと呼ばれるメモリと3つのゲートを持つブロックに置き換えることで実現されるRNNの一種。LSTMは過去のデータをsigmoidやtanhではなく「線形和」で保持するため、逆伝播しても勾配が極端に大きくなったり小さくなったりしないため、勾配消失問題が発生しない

![image](https://user-images.githubusercontent.com/57475794/92686999-af89fa80-f375-11ea-9339-b721fd330813.png)



![image](https://user-images.githubusercontent.com/57475794/92687258-2aebac00-f376-11ea-8d2b-b20d568c465f.png)
LSTMの詳細については以下を参考にした。
（参考：https://qiita.com/t_Signull/items/21b82be280b46f467d1b ）


## データの作成・前処理
訓練データとなる元データはmidiファイルの音楽データある。
これを行が128段階(0~127)の音階（ピッチ）と列が時間（タイムステップ）を表す行列としてアーキテクチャの入力・出力において取り扱う。行列の要素にはvelocityとして、音量を表す値が0以上の数次が格納されている。
この形式はピアノロールと呼ばれている。ピアノロールへの変換はライブラリ pypianoroll を用いて行う。
また、pypianorollを使って、ピアノロール形式の行列をmidiファイルへと出力することができる。


入力データに使うmidiファイルは以下のヴェートーヴェンの曲を用いた。

## 構築した深層学習モデル
編集中。。

## 結果
ファイルを上げてます。
評価については追々記述したいです。

