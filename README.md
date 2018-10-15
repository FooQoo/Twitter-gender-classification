## Twitter-gender-classification project

kaggle-data -> https://www.kaggle.com/crowdflower/twitter-user-gender-classification

### アプローチ

#### ツイートテキストベース
1. ナイーブベイズ分類器
2. 分散表現 + LSTM

#### カラーベース
1. ロジスティック回帰

#### プロフィールベース
1. ナイーブベイズ分類器

#### ネームベース
1. Character based LSTM

### 結果

accuracyが高い順に  
1. プロフィール + ナイーブベイズ 68%
2. ネーム + Character based LSTM 64%
3. ツイートテキスト + ナイーブベイズ 61%
4. ツイートテキスト + (分散表現 + LSTM) 60%
5. カラー + ロジスティック回帰 59%

でした．  

### 考察

- ナイーブベイズ分類器は単純ながらも高い精度を出す．
- ネーム + Character based LSTMはEpochが進むごとにaccuracyがともに伸びていったのでepochsを増やせば高い精度が出る可能性がある．
- カラーの精度が最も低かったことが残念，データ分析して特徴量などを工夫してみたい．