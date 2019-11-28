## MobileQA

[TensorFlow Lite BERT QA Android Example Application](https://github.com/tensorflow/examples/tree/master/lite/examples/bert_qa/android) 与 [tflite-android-transformers](https://github.com/huggingface/tflite-android-transformers) 展示了基于Bert/DistilBERT的离线QA例子，但是只支持英文和安卓设备。

本项目计划实现基于中文的机器阅读理解在手机端的离线应用，并且同时支持安卓和苹果设备。

Targeting to release before Dec 5th. 目标是12月5日前发布。



## 数据集

使用[CMRC 2018 公开数据集](https://github.com/ymcui/cmrc2018/blob/master/README_CN.md)，该数据集是第二届讯飞杯中文机器阅读理解评测所使用的数据。数据集已被计算语言学顶级国际会议[EMNLP 2019](http://emnlp-ijcnlp2019.org/)录用



## 模型

使用 [albert_zh_small](https://github.com/brightmart/albert_zh) 预训练模型，额外加上一层全连接做answer span预测

* 模型训练

​		已完成，待提交

* 用tflite转换模型

​		已完成，待提交



## Android Demo

已完成第一版，详见 [tflite-android-transformers-master](https://github.com/CLUEbenchmark/MobileQA/tree/master/tflite-android-transformers-master) 



## IOS Demo

进行中

## Updates

2019-11-27: Add first version of Android Demo, details see [tflite-android-transformers-master](https://github.com/CLUEbenchmark/MobileQA/tree/master/tflite-android-transformers-master) 

## Contribution

如果你感兴趣或希望提供帮助，发送邮件ChineseGLUE@163.com

If you're interested or want to help, send an email to ChineseGLUE@163.com

