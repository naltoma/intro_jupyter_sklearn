# jupyter + sklearn 入門
## 動作確認環境(2017/10/16時点)
- anaconda3-4.4.0
  - Python: 3.6.1
  - sklearn: 0.18.1
  - jupyter: 1.0.0

## howto
- jupyterの起動。
```
git clone https://github.com/naltoma/intro_jupyter_sklearn.git
cd intro_jupyter_sklearn
jupyter notebook
```
- intro_sklearn.ipynbを開く。
  - 後はノート内の指示に従って動かそう。

## Tips
- 1d arrays問題
  - scikit-learn 0.17から「1サンプル」時のデータをreshapeする必要が出てきた。
  - 例えば ``svm.predict(data[-1])`` のように、データセットの最後の1サンプルに対して予測したい場合、 ``svm.predict(data[-1:]`` のように記述するか、numpy.reshapeする必要がある。
  - Warning文
    - DeprecationWarning: Passing 1d arrays as data is deprecated in 0.17 and will raise ValueError in 0.19. Reshape your data either using X.reshape(-1, 1) if your data has a single feature or X.reshape(1, -1) if it contains a single sample.
  - 関連: [Preprocessing in scikit learn - single sample - Depreciation warning
](https://stackoverflow.com/questions/35082140/preprocessing-in-scikit-learn-single-sample-depreciation-warning)
