---
layout: post
title: CentOSにNumPyとSciPyとmatplotlibをインストール
date: 2016-08-10
categories: python
---

### ライブラリの説明


```
NumPy：数学関数ライブラリ
SciPy：科学技術計算用ライブラリ
matplotlib：グラフ描画ライブラリ
```

### NumPyインストール

```
# pip install --upgrade pip
# pip install numpy
# pip list
```

### SciPyインストール

```
# yum -y install lapack-devel
# pip install scipy
# pip list
```

### matplotlibインストール

```
# yum install devtoolset-2-gcc-c++
scl enable devtoolset-2 bash

# yum install freetype
# yum install freetype-devel
# yum install libpng-devel

# pip install matplotlib

# pip list
```

### scikit-learnインストール

```
# pip install scikit-learn
# pip list
```



