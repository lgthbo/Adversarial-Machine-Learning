Adversarial Machine Learning
===
## 需求

將**cat1.png**、**cat2.png**、**dog1.png**加入雜訊讓**predict.py**產生錯誤的預測。

## 實作方式

基本上是使用 Fast Gradient Sign Method

把原本的model往錯誤的方向train

關鍵程式有參考網路上的open source

https://github.com/soumyac1999/FGSM-Keras

## 使用方式

攻擊方式如下：

    python3 adv.py [attack target]

會產生出 `afterAdv` 加上目標png的一張改過的圖片。

可以使用 `predict.py` 來預測：

    python3 predict.py  [attack result]

## 成果
| BEFORE | AFTER |
| -------- | -------- |
|![](https://i.imgur.com/JxcgrST.jpg)|![](https://i.imgur.com/ubXjsoP.png)|
|![](https://i.imgur.com/Gcazfhi.png)|![](https://i.imgur.com/kA3ligZ.png)|
|![](https://i.imgur.com/jZko1yZ.jpg)|![](https://i.imgur.com/967cg4l.png)|
|![](https://i.imgur.com/pmXhEUK.png)|![](https://i.imgur.com/hQcyYrF.png)|
|![](https://i.imgur.com/kRqIgez.png)|![](https://i.imgur.com/8cB7i1K.jpg)|
|![](https://i.imgur.com/yrkrfsN.png)|![](https://i.imgur.com/WBLJA0V.png)|

## 備註

model.h5因為太大沒有上傳
