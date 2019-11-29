## 基于中文的机器阅读理解模型

代码引用自 https://github.com/ewrfcas/bert_cn_finetune

## 模型训练

1. 下载albert_small_zh_google放入文件夹中。地址：https://storage.googleapis.com/albert_zh/albert_small_zh_google.zip

2. python cmrc2018_finetune_tf_albert.py 

   （注意：由于后期转tflite文件,训练过程中不要使用tf.float16)

## 模型转换

1. 将生成的模型转pb(在转pb以及tflite的过程中要确保tensorflow版本为1.15.0)

   ```
   pip install tensorflow==1.15.0
   freeze_graph --input_checkpoint albert_model.ckpt \
                --output_graph albert_tiny_zh.pb \
                --output_node_names finetune_mrc/truediv \
                --checkpoint_version 1 \
                --input_meta_graph albert_model.ckpt.meta \
                --input_binary true
   
   ```

   

2. pb文件转tflite文件

   ```
   pip install tf-nightly
   tflite_convert --graph_def_file albert_tiny_zh.pb \
                  --input_arrays 'input_ids,input_masks,segment_ids' \
                  --output_arrays 'finetune_mrc/add, finetune_mrc/add_1'\
                  --input_shapes 1,512:1,512:1,512 \
                  --output_file saved_model.tflite \
                  --enable_v1_converter \
                  --experimental_new_converter
   ```

   