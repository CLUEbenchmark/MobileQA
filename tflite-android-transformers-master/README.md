

####  中文机器阅读理解Andoid客户端Demo

#### Tensorflow Lite Transformers Andorid  Chinese Machine Reading Comprehension Demo

- 在CMRC中微调的ALBERT[Albert_tiny_google](#)
- 转换ALBERT to TFLite
- 离线进行答案预测

#### 示例数据

我们提供 CMRC2018 Dev中的数据作为示例

真机示例程序[app.arm.apk](https://6a75-junzeng-uxxxm-1300734931.tcb.qcloud.la/app-armeabi-v7a-debug.apk?sign=483115f1519321a8ca59f2428cfe5153&t=1574871565)

虚拟机示例程序[app.x86.apk](https://6a75-junzeng-uxxxm-1300734931.tcb.qcloud.la/app-debug.apk?sign=8e5eb09bcb0c46a525c7b1b8ea328946&t=1574871756)

效果如下

#### 下一步计划

开发基于IOS coreml的示例程序



#### 基于Android的开发流程

##### 前提

- 安装 Android Studio （最新） [官网](https://developer.android.com/studio/index.html)

- 你应该有一台Android设备，或者 虚拟器（建议修改虚拟机目录，贼大）

  

#####  Android Studio步骤

1. 打开 Android Studio  ，依次**File**  >>  **Open an existing Android Studio project**
2. 等待哈
3. 选择运行设备，并点击运行
4. gradle 下载预训练TFlite模型，并自动构建APP，并在目标设备上运行

##### 命令行步骤

1. 切换到当前工作目录，通过以下命令构建

   ```shell
   ./gradlew build
   ```

1. 通过**adb**安装应用

   ```shell
   adb install app/build/outputs/apk/debug/app-debug.apk
   ```

   

#### 模型转换过程

[doing](#)

---

#### 参考

Demo参考TFlite官方例子: [tensorflow/examples](https://github.com/tensorflow/examples)

中文预训练ALBERT: [Albert_tiny_google](https://github.com/zhongbin1/bert_tokenization_for_java)

[BERT Tokenization For JAVA](https://github.com/zhongbin1/bert_tokenization_for_java)



#### License

[Apache License 2.0](LICENSE)
