# 必要性说明(TODO)
## 简历云主机和本地机器的ssh的端口映射
> `ssh -CNg -L 7860:127.0.0.1:7860 root@RemoteIPAddress -p RemoteSSHPort`

## 模型地址
> `/root/dataDisk/models/chatglm3-6b`

## LORA微调结果
> `[lora_finetune_result.ipynb](lora_finetune_result.ipynb)`
```text
Setting eos_token is not supported, use the default one.
Setting pad_token is not supported, use the default one.
Setting unk_token is not supported, use the default one.
Loading checkpoint shards: 100%|██████████████████| 7/7 [01:30<00:00, 12.89s/it]
trainable params: 1,949,696 || all params: 6,245,533,696 || trainable%: 0.0312
--> Model

--> model has 1.949696M params

Setting num_proc from 16 back to 1 for the train split to disable multiprocessing as it only contains one shard.
Generating train split: 114599 examples [00:00, 624951.95 examples/s]
Setting num_proc from 16 back to 1 for the validation split to disable multiprocessing as it only contains one shard.
Generating validation split: 1070 examples [00:00, 218081.80 examples/s]
Setting num_proc from 16 back to 1 for the test split to disable multiprocessing as it only contains one shard.
Generating test split: 1070 examples [00:00, 224597.40 examples/s]
Map (num_proc=16): 100%|██████| 114599/114599 [00:01<00:00, 57558.03 examples/s]
train_dataset: Dataset({
    features: ['input_ids', 'labels'],
    num_rows: 114599
})
Map (num_proc=16): 100%|███████████| 1070/1070 [00:00<00:00, 1440.60 examples/s]
val_dataset: Dataset({
    features: ['input_ids', 'output_ids'],
    num_rows: 1070
})
Map (num_proc=16): 100%|███████████| 1070/1070 [00:00<00:00, 1462.60 examples/s]
test_dataset: Dataset({
    features: ['input_ids', 'output_ids'],
    num_rows: 1070
})
--> Sanity check
           '[gMASK]': 64790 -> -100
               'sop': 64792 -> -100
          '<|user|>': 64795 -> -100
                  '': 30910 -> -100
                '\n': 13 -> -100
                  '': 30910 -> -100
                '类型': 33467 -> -100
                 '#': 31010 -> -100
                 '裤': 56532 -> -100
                 '*': 30998 -> -100
                 '版': 55090 -> -100
                 '型': 54888 -> -100
                 '#': 31010 -> -100
                '宽松': 40833 -> -100
                 '*': 30998 -> -100
                '风格': 32799 -> -100
                 '#': 31010 -> -100
                '性感': 40589 -> -100
                 '*': 30998 -> -100
                '图案': 37505 -> -100
                 '#': 31010 -> -100
                '线条': 37216 -> -100
                 '*': 30998 -> -100
                 '裤': 56532 -> -100
                 '型': 54888 -> -100
                 '#': 31010 -> -100
                 '阔': 56529 -> -100
                 '腿': 56158 -> -100
                 '裤': 56532 -> -100
     '<|assistant|>': 64796 -> -100
                  '': 30910 -> 30910
                '\n': 13 -> 13
                  '': 30910 -> 30910
                '宽松': 40833 -> 40833
                 '的': 54530 -> 54530
                 '阔': 56529 -> 56529
                 '腿': 56158 -> 56158
                 '裤': 56532 -> 56532
                 '这': 54551 -> 54551
                '两年': 33808 -> 33808
                '真的': 32041 -> 32041
                 '吸': 55360 -> 55360
                 '粉': 55486 -> 55486
                '不少': 32138 -> 32138
                 '，': 31123 -> 31123
                '明星': 32943 -> 32943
                '时尚': 33481 -> 33481
                 '达': 54880 -> 54880
                '人的': 31664 -> 31664
                '心头': 46565 -> 46565
                 '爱': 54799 -> 54799
                 '。': 31155 -> 31155
                '毕竟': 33051 -> 33051
                 '好': 54591 -> 54591
                 '穿': 55432 -> 55432
                '时尚': 33481 -> 33481
                 '，': 31123 -> 31123
                 '谁': 55622 -> 55622
                '都能': 32904 -> 32904
                 '穿': 55432 -> 55432
                 '出': 54557 -> 54557
                 '腿': 56158 -> 56158
                 '长': 54625 -> 54625
                 '2': 30943 -> 30943
                 '米': 55055 -> 55055
               '的效果': 35590 -> 35590
                '宽松': 40833 -> 40833
                 '的': 54530 -> 54530
                 '裤': 56532 -> 56532
                 '腿': 56158 -> 56158
                 '，': 31123 -> 31123
               '当然是': 48466 -> 48466
                 '遮': 57148 -> 57148
                 '肉': 55343 -> 55343
                 '小': 54603 -> 54603
                '能手': 49355 -> 49355
                 '啊': 55674 -> 55674
                 '。': 31155 -> 31155
                '上身': 51605 -> 51605
                 '随': 55119 -> 55119
                 '性': 54642 -> 54642
                '自然': 31799 -> 31799
                 '不': 54535 -> 54535
                 '拘': 57036 -> 57036
                 '束': 55625 -> 55625
                 '，': 31123 -> 31123
                '面料': 46839 -> 46839
                 '亲': 55113 -> 55113
                 '肤': 56089 -> 56089
                '舒适': 33894 -> 33894
                 '贴': 55778 -> 55778
                '身体': 31902 -> 31902
                 '验': 55017 -> 55017
                 '感': 54706 -> 54706
                 '棒': 56382 -> 56382
                 '棒': 56382 -> 56382
                 '哒': 59230 -> 59230
                 '。': 31155 -> 31155
                 '系': 54712 -> 54712
                 '带': 54882 -> 54882
                '部分': 31726 -> 31726
                '增加': 31917 -> 31917
                '设计': 31735 -> 31735
                '看点': 45032 -> 45032
                 '，': 31123 -> 31123
                 '还': 54656 -> 54656
                 '让': 54772 -> 54772
                '单品': 46539 -> 46539
               '的设计': 34481 -> 34481
                 '感': 54706 -> 54706
                '更强': 43084 -> 43084
                 '。': 31155 -> 31155
                '腿部': 46799 -> 46799
                '线条': 37216 -> 37216
                 '若': 55351 -> 55351
                 '隐': 55733 -> 55733
                 '若': 55351 -> 55351
                 '现': 54600 -> 54600
                 '的': 54530 -> 54530
                 '，': 31123 -> 31123
                '性感': 40589 -> 40589
                 '撩': 58521 -> 58521
                 '人': 54533 -> 54533
                 '。': 31155 -> 31155
                '颜色': 33692 -> 33692
                 '敲': 57004 -> 57004
                '温柔': 34678 -> 34678
                 '的': 54530 -> 54530
                 '，': 31123 -> 31123
                 '与': 54619 -> 54619
                '裤子': 44722 -> 44722
                '本身': 32754 -> 32754
                 '所': 54626 -> 54626
                '呈现': 33169 -> 33169
               '的风格': 48084 -> 48084
                '有点': 33149 -> 33149
                 '反': 54955 -> 54955
                 '差': 55342 -> 55342
                 '萌': 56842 -> 56842
                 '。': 31155 -> 31155
                  '': 2 -> 2
Detected kernel version 5.4.0, which is below the recommended minimum of 5.5.0; this can cause the process to hang. It is recommended to upgrade the kernel to the minimum version or higher.
max_steps is given, it will override any value given in num_train_epochs
***** Running training *****
  Num examples = 114,599
  Num Epochs = 1
  Instantaneous batch size per device = 4
  Total train batch size (w. parallel, distributed & accumulation) = 4
  Gradient Accumulation steps = 1
  Total optimization steps = 3,000
  Number of trainable parameters = 1,949,696
{'loss': 4.8305, 'grad_norm': 2.254749059677124, 'learning_rate': 4.9833333333333336e-05, 'epoch': 0.0}
{'loss': 4.602, 'grad_norm': 3.1739087104797363, 'learning_rate': 4.966666666666667e-05, 'epoch': 0.0}
{'loss': 4.4906, 'grad_norm': 3.0274832248687744, 'learning_rate': 4.9500000000000004e-05, 'epoch': 0.0}
{'loss': 4.1268, 'grad_norm': 3.457089424133301, 'learning_rate': 4.933333333333334e-05, 'epoch': 0.0}
{'loss': 4.1188, 'grad_norm': 2.737689971923828, 'learning_rate': 4.9166666666666665e-05, 'epoch': 0.0}
{'loss': 3.8662, 'grad_norm': 2.972133159637451, 'learning_rate': 4.9e-05, 'epoch': 0.0}
{'loss': 3.8432, 'grad_norm': 2.9303576946258545, 'learning_rate': 4.883333333333334e-05, 'epoch': 0.0}
{'loss': 3.7467, 'grad_norm': 2.9594051837921143, 'learning_rate': 4.866666666666667e-05, 'epoch': 0.0}
{'loss': 3.6348, 'grad_norm': 3.22481369972229, 'learning_rate': 4.85e-05, 'epoch': 0.0}
{'loss': 3.7195, 'grad_norm': 3.4170687198638916, 'learning_rate': 4.8333333333333334e-05, 'epoch': 0.0}
{'loss': 3.6695, 'grad_norm': 3.651639699935913, 'learning_rate': 4.8166666666666674e-05, 'epoch': 0.0}
{'loss': 3.8449, 'grad_norm': 3.875155448913574, 'learning_rate': 4.8e-05, 'epoch': 0.0}
{'loss': 3.6137, 'grad_norm': 3.5069241523742676, 'learning_rate': 4.7833333333333335e-05, 'epoch': 0.0}
{'loss': 3.7303, 'grad_norm': 4.484037399291992, 'learning_rate': 4.766666666666667e-05, 'epoch': 0.0}
{'loss': 3.6832, 'grad_norm': 3.668231248855591, 'learning_rate': 4.75e-05, 'epoch': 0.01}
{'loss': 3.7436, 'grad_norm': 3.9909703731536865, 'learning_rate': 4.7333333333333336e-05, 'epoch': 0.01}
{'loss': 3.5768, 'grad_norm': 4.1281561851501465, 'learning_rate': 4.716666666666667e-05, 'epoch': 0.01}
{'loss': 3.5754, 'grad_norm': 4.387509346008301, 'learning_rate': 4.7e-05, 'epoch': 0.01}
{'loss': 3.5479, 'grad_norm': 4.897694110870361, 'learning_rate': 4.683333333333334e-05, 'epoch': 0.01}
{'loss': 3.5771, 'grad_norm': 4.581422805786133, 'learning_rate': 4.666666666666667e-05, 'epoch': 0.01}
{'loss': 3.5525, 'grad_norm': 4.998153209686279, 'learning_rate': 4.6500000000000005e-05, 'epoch': 0.01}
{'loss': 3.6449, 'grad_norm': 4.127691745758057, 'learning_rate': 4.633333333333333e-05, 'epoch': 0.01}
{'loss': 3.6113, 'grad_norm': 4.865299224853516, 'learning_rate': 4.6166666666666666e-05, 'epoch': 0.01}
{'loss': 3.5088, 'grad_norm': 4.615352630615234, 'learning_rate': 4.600000000000001e-05, 'epoch': 0.01}
{'loss': 3.4781, 'grad_norm': 5.499984264373779, 'learning_rate': 4.5833333333333334e-05, 'epoch': 0.01}
{'loss': 3.6039, 'grad_norm': 5.3849196434021, 'learning_rate': 4.566666666666667e-05, 'epoch': 0.01}
{'loss': 3.5465, 'grad_norm': 5.430337905883789, 'learning_rate': 4.55e-05, 'epoch': 0.01}
{'loss': 3.6135, 'grad_norm': 4.570376396179199, 'learning_rate': 4.5333333333333335e-05, 'epoch': 0.01}
{'loss': 3.6303, 'grad_norm': 4.818716526031494, 'learning_rate': 4.516666666666667e-05, 'epoch': 0.01}
{'loss': 3.5395, 'grad_norm': 5.891198635101318, 'learning_rate': 4.5e-05, 'epoch': 0.01}
{'loss': 3.467, 'grad_norm': 5.406421184539795, 'learning_rate': 4.483333333333333e-05, 'epoch': 0.01}
{'loss': 3.6063, 'grad_norm': 5.834434986114502, 'learning_rate': 4.466666666666667e-05, 'epoch': 0.01}
{'loss': 3.4168, 'grad_norm': 5.314158916473389, 'learning_rate': 4.4500000000000004e-05, 'epoch': 0.01}
{'loss': 3.4918, 'grad_norm': 5.4781060218811035, 'learning_rate': 4.433333333333334e-05, 'epoch': 0.01}
{'loss': 3.5207, 'grad_norm': 5.569215774536133, 'learning_rate': 4.4166666666666665e-05, 'epoch': 0.01}
{'loss': 3.5727, 'grad_norm': 5.286966323852539, 'learning_rate': 4.4000000000000006e-05, 'epoch': 0.01}
{'loss': 3.3598, 'grad_norm': 4.928376197814941, 'learning_rate': 4.383333333333334e-05, 'epoch': 0.01}
{'loss': 3.5291, 'grad_norm': 5.200712203979492, 'learning_rate': 4.3666666666666666e-05, 'epoch': 0.01}
{'loss': 3.5227, 'grad_norm': 5.271636486053467, 'learning_rate': 4.35e-05, 'epoch': 0.01}
{'loss': 3.4742, 'grad_norm': 5.641286849975586, 'learning_rate': 4.3333333333333334e-05, 'epoch': 0.01}
{'loss': 3.6896, 'grad_norm': 5.5333967208862305, 'learning_rate': 4.316666666666667e-05, 'epoch': 0.01}
{'loss': 3.4973, 'grad_norm': 5.026886463165283, 'learning_rate': 4.3e-05, 'epoch': 0.01}
{'loss': 3.6248, 'grad_norm': 5.667610168457031, 'learning_rate': 4.2833333333333335e-05, 'epoch': 0.02}
{'loss': 3.416, 'grad_norm': 6.70228385925293, 'learning_rate': 4.266666666666667e-05, 'epoch': 0.02}
{'loss': 3.4146, 'grad_norm': 6.136542797088623, 'learning_rate': 4.25e-05, 'epoch': 0.02}
{'loss': 3.4238, 'grad_norm': 5.609162330627441, 'learning_rate': 4.233333333333334e-05, 'epoch': 0.02}
{'loss': 3.535, 'grad_norm': 5.661261558532715, 'learning_rate': 4.216666666666667e-05, 'epoch': 0.02}
{'loss': 3.4469, 'grad_norm': 7.169975757598877, 'learning_rate': 4.2e-05, 'epoch': 0.02}
{'loss': 3.4578, 'grad_norm': 5.85629940032959, 'learning_rate': 4.183333333333334e-05, 'epoch': 0.02}
{'loss': 3.5611, 'grad_norm': 6.0166802406311035, 'learning_rate': 4.166666666666667e-05, 'epoch': 0.02}
 17%|██████▋                                 | 500/3000 [04:48<26:58,  1.54it/s]***** Running Evaluation *****
  Num examples = 50
  Batch size = 16

  0%|                                                     | 0/4 [00:00<?, ?it/s]
 50%|██████████████████████▌                      | 2/4 [00:03<00:03,  1.68s/it]
 75%|█████████████████████████████████▊           | 3/4 [00:05<00:01,  1.94s/it]
100%|█████████████████████████████████████████████| 4/4 [00:21<00:00,  7.18s/it]Building prefix dict from the default dictionary ...
Dumping model to file cache /tmp/jieba.cache
Loading model cost 0.519 seconds.
Prefix dict has been built successfully.
                                                                                
{'eval_rouge-1': 32.160414, 'eval_rouge-2': 6.759078, 'eval_rouge-l': 24.500572000000002, 'eval_bleu-4': 0.03267148479257676, 'eval_runtime': 26.1249, 'eval_samples_per_second': 1.914, 'eval_steps_per_second': 0.153, 'epoch': 0.02}
 17%|██████▋                                 | 500/3000 [05:14<26:58,  1.54it/s]
100%|█████████████████████████████████████████████| 4/4 [00:22<00:00,  7.18s/it]
                                                                                Saving model checkpoint to ./output/checkpoint-500
/root/.local/lib/python3.11/site-packages/peft/utils/save_and_load.py:195: UserWarning: Could not find a config file in /root/dataDisk/models/chatglm3-6b - will assume that the vocabulary was not modified.
  warnings.warn(
{'loss': 3.3223, 'grad_norm': 5.810793876647949, 'learning_rate': 4.15e-05, 'epoch': 0.02}
{'loss': 3.5455, 'grad_norm': 6.690789222717285, 'learning_rate': 4.133333333333333e-05, 'epoch': 0.02}
{'loss': 3.5826, 'grad_norm': 6.110449314117432, 'learning_rate': 4.116666666666667e-05, 'epoch': 0.02}
{'loss': 3.4889, 'grad_norm': 5.494697570800781, 'learning_rate': 4.1e-05, 'epoch': 0.02}
{'loss': 3.5256, 'grad_norm': 5.3679280281066895, 'learning_rate': 4.0833333333333334e-05, 'epoch': 0.02}
{'loss': 3.6477, 'grad_norm': 5.811570644378662, 'learning_rate': 4.066666666666667e-05, 'epoch': 0.02}
{'loss': 3.4924, 'grad_norm': 5.878842830657959, 'learning_rate': 4.05e-05, 'epoch': 0.02}
{'loss': 3.3723, 'grad_norm': 5.658172607421875, 'learning_rate': 4.0333333333333336e-05, 'epoch': 0.02}
{'loss': 3.4248, 'grad_norm': 6.336036682128906, 'learning_rate': 4.016666666666667e-05, 'epoch': 0.02}
{'loss': 3.49, 'grad_norm': 6.464826583862305, 'learning_rate': 4e-05, 'epoch': 0.02}
{'loss': 3.4439, 'grad_norm': 6.220681190490723, 'learning_rate': 3.983333333333333e-05, 'epoch': 0.02}
{'loss': 3.4535, 'grad_norm': 6.645595073699951, 'learning_rate': 3.966666666666667e-05, 'epoch': 0.02}
{'loss': 3.4461, 'grad_norm': 6.034765720367432, 'learning_rate': 3.9500000000000005e-05, 'epoch': 0.02}
{'loss': 3.457, 'grad_norm': 6.316323280334473, 'learning_rate': 3.933333333333333e-05, 'epoch': 0.02}
{'loss': 3.5334, 'grad_norm': 6.070063591003418, 'learning_rate': 3.9166666666666665e-05, 'epoch': 0.02}
{'loss': 3.483, 'grad_norm': 6.418892860412598, 'learning_rate': 3.9000000000000006e-05, 'epoch': 0.02}
{'loss': 3.543, 'grad_norm': 6.153814315795898, 'learning_rate': 3.883333333333333e-05, 'epoch': 0.02}
{'loss': 3.3035, 'grad_norm': 7.080769062042236, 'learning_rate': 3.866666666666667e-05, 'epoch': 0.02}
{'loss': 3.3994, 'grad_norm': 6.729435443878174, 'learning_rate': 3.85e-05, 'epoch': 0.02}
{'loss': 3.3559, 'grad_norm': 6.321923732757568, 'learning_rate': 3.8333333333333334e-05, 'epoch': 0.02}
{'loss': 3.5021, 'grad_norm': 7.157541275024414, 'learning_rate': 3.816666666666667e-05, 'epoch': 0.02}
{'loss': 3.5275, 'grad_norm': 6.858126163482666, 'learning_rate': 3.8e-05, 'epoch': 0.03}
{'loss': 3.2451, 'grad_norm': 6.9111104011535645, 'learning_rate': 3.7833333333333336e-05, 'epoch': 0.03}
{'loss': 3.5711, 'grad_norm': 5.836596488952637, 'learning_rate': 3.766666666666667e-05, 'epoch': 0.03}
{'loss': 3.3959, 'grad_norm': 6.54299783706665, 'learning_rate': 3.7500000000000003e-05, 'epoch': 0.03}
{'loss': 3.4795, 'grad_norm': 6.253952980041504, 'learning_rate': 3.733333333333334e-05, 'epoch': 0.03}
{'loss': 3.618, 'grad_norm': 6.437897205352783, 'learning_rate': 3.7166666666666664e-05, 'epoch': 0.03}
{'loss': 3.4711, 'grad_norm': 6.371791362762451, 'learning_rate': 3.7e-05, 'epoch': 0.03}
{'loss': 3.3244, 'grad_norm': 6.64915132522583, 'learning_rate': 3.683333333333334e-05, 'epoch': 0.03}
{'loss': 3.5572, 'grad_norm': 6.91436767578125, 'learning_rate': 3.6666666666666666e-05, 'epoch': 0.03}
{'loss': 3.2926, 'grad_norm': 6.579039096832275, 'learning_rate': 3.65e-05, 'epoch': 0.03}
{'loss': 3.3576, 'grad_norm': 6.562108516693115, 'learning_rate': 3.633333333333333e-05, 'epoch': 0.03}
{'loss': 3.4611, 'grad_norm': 7.162087917327881, 'learning_rate': 3.6166666666666674e-05, 'epoch': 0.03}
{'loss': 3.4078, 'grad_norm': 6.449375629425049, 'learning_rate': 3.6e-05, 'epoch': 0.03}
{'loss': 3.5043, 'grad_norm': 6.307328701019287, 'learning_rate': 3.5833333333333335e-05, 'epoch': 0.03}
{'loss': 3.5338, 'grad_norm': 6.278844356536865, 'learning_rate': 3.566666666666667e-05, 'epoch': 0.03}
{'loss': 3.2967, 'grad_norm': 7.138107776641846, 'learning_rate': 3.55e-05, 'epoch': 0.03}
{'loss': 3.4895, 'grad_norm': 6.858454704284668, 'learning_rate': 3.5333333333333336e-05, 'epoch': 0.03}
{'loss': 3.4576, 'grad_norm': 7.598515510559082, 'learning_rate': 3.516666666666667e-05, 'epoch': 0.03}
{'loss': 3.2627, 'grad_norm': 7.9184393882751465, 'learning_rate': 3.5e-05, 'epoch': 0.03}
{'loss': 3.468, 'grad_norm': 7.884007930755615, 'learning_rate': 3.483333333333334e-05, 'epoch': 0.03}
{'loss': 3.4164, 'grad_norm': 7.10396671295166, 'learning_rate': 3.466666666666667e-05, 'epoch': 0.03}
{'loss': 3.4594, 'grad_norm': 7.585606098175049, 'learning_rate': 3.45e-05, 'epoch': 0.03}
{'loss': 3.5695, 'grad_norm': 7.360101222991943, 'learning_rate': 3.433333333333333e-05, 'epoch': 0.03}
{'loss': 3.3623, 'grad_norm': 6.506255626678467, 'learning_rate': 3.4166666666666666e-05, 'epoch': 0.03}
{'loss': 3.4406, 'grad_norm': 7.9200568199157715, 'learning_rate': 3.4000000000000007e-05, 'epoch': 0.03}
{'loss': 3.5373, 'grad_norm': 6.047525405883789, 'learning_rate': 3.3833333333333334e-05, 'epoch': 0.03}
{'loss': 3.3232, 'grad_norm': 7.2912797927856445, 'learning_rate': 3.366666666666667e-05, 'epoch': 0.03}
{'loss': 3.4602, 'grad_norm': 7.407312870025635, 'learning_rate': 3.35e-05, 'epoch': 0.03}
{'loss': 3.3967, 'grad_norm': 7.954436302185059, 'learning_rate': 3.3333333333333335e-05, 'epoch': 0.03}
 33%|█████████████                          | 1000/3000 [09:56<19:36,  1.70it/s]***** Running Evaluation *****
  Num examples = 50
  Batch size = 16

  0%|                                                     | 0/4 [00:00<?, ?it/s]
 50%|██████████████████████▌                      | 2/4 [00:02<00:02,  1.22s/it]
 75%|█████████████████████████████████▊           | 3/4 [00:04<00:01,  1.73s/it]
                                                                                
{'eval_rouge-1': 32.332361999999996, 'eval_rouge-2': 7.029346, 'eval_rouge-l': 25.471156, 'eval_bleu-4': 0.03369208572233207, 'eval_runtime': 23.7371, 'eval_samples_per_second': 2.106, 'eval_steps_per_second': 0.169, 'epoch': 0.03}
 33%|█████████████                          | 1000/3000 [10:20<19:36,  1.70it/s]
100%|█████████████████████████████████████████████| 4/4 [00:20<00:00,  6.95s/it]
                                                                                Saving model checkpoint to ./output/checkpoint-1000
/root/.local/lib/python3.11/site-packages/peft/utils/save_and_load.py:195: UserWarning: Could not find a config file in /root/dataDisk/models/chatglm3-6b - will assume that the vocabulary was not modified.
  warnings.warn(
{'loss': 3.4486, 'grad_norm': 7.110916614532471, 'learning_rate': 3.316666666666667e-05, 'epoch': 0.04}
{'loss': 3.4588, 'grad_norm': 7.647634029388428, 'learning_rate': 3.3e-05, 'epoch': 0.04}
{'loss': 3.6523, 'grad_norm': 8.377150535583496, 'learning_rate': 3.283333333333333e-05, 'epoch': 0.04}
{'loss': 3.4016, 'grad_norm': 6.505376815795898, 'learning_rate': 3.266666666666667e-05, 'epoch': 0.04}
{'loss': 3.3939, 'grad_norm': 8.757610321044922, 'learning_rate': 3.2500000000000004e-05, 'epoch': 0.04}
{'loss': 3.3584, 'grad_norm': 7.85616397857666, 'learning_rate': 3.233333333333333e-05, 'epoch': 0.04}
{'loss': 3.3902, 'grad_norm': 7.178151607513428, 'learning_rate': 3.2166666666666665e-05, 'epoch': 0.04}
{'loss': 3.4631, 'grad_norm': 7.357961177825928, 'learning_rate': 3.2000000000000005e-05, 'epoch': 0.04}
{'loss': 3.5285, 'grad_norm': 7.108318328857422, 'learning_rate': 3.183333333333334e-05, 'epoch': 0.04}
{'loss': 3.4678, 'grad_norm': 6.550983905792236, 'learning_rate': 3.1666666666666666e-05, 'epoch': 0.04}
{'loss': 3.3477, 'grad_norm': 6.934013366699219, 'learning_rate': 3.15e-05, 'epoch': 0.04}
{'loss': 3.5287, 'grad_norm': 7.841541767120361, 'learning_rate': 3.1333333333333334e-05, 'epoch': 0.04}
{'loss': 3.4312, 'grad_norm': 7.333691596984863, 'learning_rate': 3.116666666666667e-05, 'epoch': 0.04}
{'loss': 3.3615, 'grad_norm': 8.108588218688965, 'learning_rate': 3.1e-05, 'epoch': 0.04}
{'loss': 3.3188, 'grad_norm': 7.702059745788574, 'learning_rate': 3.0833333333333335e-05, 'epoch': 0.04}
{'loss': 3.3631, 'grad_norm': 7.394345283508301, 'learning_rate': 3.066666666666667e-05, 'epoch': 0.04}
{'loss': 3.4527, 'grad_norm': 6.7195563316345215, 'learning_rate': 3.05e-05, 'epoch': 0.04}
{'loss': 3.4725, 'grad_norm': 6.603448390960693, 'learning_rate': 3.0333333333333337e-05, 'epoch': 0.04}
{'loss': 3.3572, 'grad_norm': 6.7667012214660645, 'learning_rate': 3.016666666666667e-05, 'epoch': 0.04}
{'loss': 3.4107, 'grad_norm': 6.459778308868408, 'learning_rate': 3e-05, 'epoch': 0.04}
{'loss': 3.2449, 'grad_norm': 6.8300700187683105, 'learning_rate': 2.9833333333333335e-05, 'epoch': 0.04}
{'loss': 3.3438, 'grad_norm': 7.455451488494873, 'learning_rate': 2.9666666666666672e-05, 'epoch': 0.04}
{'loss': 3.3791, 'grad_norm': 7.6735310554504395, 'learning_rate': 2.95e-05, 'epoch': 0.04}
{'loss': 3.3758, 'grad_norm': 11.65651798248291, 'learning_rate': 2.9333333333333336e-05, 'epoch': 0.04}
{'loss': 3.4449, 'grad_norm': 6.881354331970215, 'learning_rate': 2.916666666666667e-05, 'epoch': 0.04}
{'loss': 3.2887, 'grad_norm': 7.743050575256348, 'learning_rate': 2.9e-05, 'epoch': 0.04}
{'loss': 3.4574, 'grad_norm': 7.407034397125244, 'learning_rate': 2.8833333333333334e-05, 'epoch': 0.04}
{'loss': 3.3352, 'grad_norm': 7.3994011878967285, 'learning_rate': 2.8666666666666668e-05, 'epoch': 0.04}
{'loss': 3.3857, 'grad_norm': 7.04435920715332, 'learning_rate': 2.8499999999999998e-05, 'epoch': 0.05}
{'loss': 3.483, 'grad_norm': 7.582316875457764, 'learning_rate': 2.8333333333333335e-05, 'epoch': 0.05}
{'loss': 3.4613, 'grad_norm': 7.124838352203369, 'learning_rate': 2.816666666666667e-05, 'epoch': 0.05}
{'loss': 3.4545, 'grad_norm': 6.879702568054199, 'learning_rate': 2.8000000000000003e-05, 'epoch': 0.05}
{'loss': 3.4035, 'grad_norm': 10.599469184875488, 'learning_rate': 2.7833333333333333e-05, 'epoch': 0.05}
{'loss': 3.3045, 'grad_norm': 7.546622276306152, 'learning_rate': 2.7666666666666667e-05, 'epoch': 0.05}
{'loss': 3.3502, 'grad_norm': 7.719691753387451, 'learning_rate': 2.7500000000000004e-05, 'epoch': 0.05}
{'loss': 3.2945, 'grad_norm': 8.003908157348633, 'learning_rate': 2.733333333333333e-05, 'epoch': 0.05}
{'loss': 3.5125, 'grad_norm': 7.256562232971191, 'learning_rate': 2.716666666666667e-05, 'epoch': 0.05}
{'loss': 3.3863, 'grad_norm': 7.222826957702637, 'learning_rate': 2.7000000000000002e-05, 'epoch': 0.05}
{'loss': 3.3582, 'grad_norm': 7.247176170349121, 'learning_rate': 2.6833333333333333e-05, 'epoch': 0.05}
{'loss': 3.4166, 'grad_norm': 6.745693206787109, 'learning_rate': 2.6666666666666667e-05, 'epoch': 0.05}
{'loss': 3.3434, 'grad_norm': 7.496222496032715, 'learning_rate': 2.6500000000000004e-05, 'epoch': 0.05}
{'loss': 3.2662, 'grad_norm': 7.928985118865967, 'learning_rate': 2.633333333333333e-05, 'epoch': 0.05}
{'loss': 3.3865, 'grad_norm': 7.683612823486328, 'learning_rate': 2.6166666666666668e-05, 'epoch': 0.05}
{'loss': 3.3592, 'grad_norm': 7.227369785308838, 'learning_rate': 2.6000000000000002e-05, 'epoch': 0.05}
{'loss': 3.2697, 'grad_norm': 6.973321914672852, 'learning_rate': 2.5833333333333336e-05, 'epoch': 0.05}
{'loss': 3.3953, 'grad_norm': 7.290734767913818, 'learning_rate': 2.5666666666666666e-05, 'epoch': 0.05}
{'loss': 3.4379, 'grad_norm': 9.431782722473145, 'learning_rate': 2.5500000000000003e-05, 'epoch': 0.05}
{'loss': 3.2979, 'grad_norm': 6.762888431549072, 'learning_rate': 2.5333333333333337e-05, 'epoch': 0.05}
{'loss': 3.4441, 'grad_norm': 7.631354331970215, 'learning_rate': 2.5166666666666667e-05, 'epoch': 0.05}
{'loss': 3.4592, 'grad_norm': 6.995547771453857, 'learning_rate': 2.5e-05, 'epoch': 0.05}
 50%|███████████████████▌                   | 1500/3000 [15:01<12:30,  2.00it/s]***** Running Evaluation *****
  Num examples = 50
  Batch size = 16

  0%|                                                     | 0/4 [00:00<?, ?it/s]
 50%|██████████████████████▌                      | 2/4 [00:02<00:02,  1.48s/it]
 75%|█████████████████████████████████▊           | 3/4 [00:05<00:01,  1.86s/it]
                                                                                
{'eval_rouge-1': 32.580184, 'eval_rouge-2': 6.79634, 'eval_rouge-l': 25.868288000000003, 'eval_bleu-4': 0.03352773986836067, 'eval_runtime': 10.9525, 'eval_samples_per_second': 4.565, 'eval_steps_per_second': 0.365, 'epoch': 0.05}
 50%|███████████████████▌                   | 1500/3000 [15:12<12:30,  2.00it/s]
100%|█████████████████████████████████████████████| 4/4 [00:07<00:00,  1.99s/it]
                                                                                Saving model checkpoint to ./output/checkpoint-1500
/root/.local/lib/python3.11/site-packages/peft/utils/save_and_load.py:195: UserWarning: Could not find a config file in /root/dataDisk/models/chatglm3-6b - will assume that the vocabulary was not modified.
  warnings.warn(
{'loss': 3.3482, 'grad_norm': 6.996358394622803, 'learning_rate': 2.4833333333333335e-05, 'epoch': 0.05}
{'loss': 3.3924, 'grad_norm': 8.207653999328613, 'learning_rate': 2.466666666666667e-05, 'epoch': 0.05}
{'loss': 3.4424, 'grad_norm': 8.269200325012207, 'learning_rate': 2.45e-05, 'epoch': 0.05}
{'loss': 3.4002, 'grad_norm': 7.103425025939941, 'learning_rate': 2.4333333333333336e-05, 'epoch': 0.05}
{'loss': 3.5002, 'grad_norm': 7.339694499969482, 'learning_rate': 2.4166666666666667e-05, 'epoch': 0.05}
{'loss': 3.4002, 'grad_norm': 8.302146911621094, 'learning_rate': 2.4e-05, 'epoch': 0.05}
{'loss': 3.4705, 'grad_norm': 8.183927536010742, 'learning_rate': 2.3833333333333334e-05, 'epoch': 0.05}
{'loss': 3.4398, 'grad_norm': 7.714913368225098, 'learning_rate': 2.3666666666666668e-05, 'epoch': 0.06}
{'loss': 3.5121, 'grad_norm': 9.1541166305542, 'learning_rate': 2.35e-05, 'epoch': 0.06}
{'loss': 3.3846, 'grad_norm': 7.255307197570801, 'learning_rate': 2.3333333333333336e-05, 'epoch': 0.06}
{'loss': 3.3684, 'grad_norm': 8.048487663269043, 'learning_rate': 2.3166666666666666e-05, 'epoch': 0.06}
{'loss': 3.3674, 'grad_norm': 8.596814155578613, 'learning_rate': 2.3000000000000003e-05, 'epoch': 0.06}
{'loss': 3.4715, 'grad_norm': 7.541319370269775, 'learning_rate': 2.2833333333333334e-05, 'epoch': 0.06}
{'loss': 3.3168, 'grad_norm': 8.144546508789062, 'learning_rate': 2.2666666666666668e-05, 'epoch': 0.06}
{'loss': 3.3707, 'grad_norm': 7.700430393218994, 'learning_rate': 2.25e-05, 'epoch': 0.06}
{'loss': 3.307, 'grad_norm': 7.186675071716309, 'learning_rate': 2.2333333333333335e-05, 'epoch': 0.06}
{'loss': 3.4809, 'grad_norm': 8.749881744384766, 'learning_rate': 2.216666666666667e-05, 'epoch': 0.06}
{'loss': 3.3779, 'grad_norm': 7.332984924316406, 'learning_rate': 2.2000000000000003e-05, 'epoch': 0.06}
{'loss': 3.3824, 'grad_norm': 7.465500354766846, 'learning_rate': 2.1833333333333333e-05, 'epoch': 0.06}
{'loss': 3.5215, 'grad_norm': 7.0944318771362305, 'learning_rate': 2.1666666666666667e-05, 'epoch': 0.06}
{'loss': 3.4641, 'grad_norm': 7.188989162445068, 'learning_rate': 2.15e-05, 'epoch': 0.06}
{'loss': 3.5029, 'grad_norm': 7.496932029724121, 'learning_rate': 2.1333333333333335e-05, 'epoch': 0.06}
{'loss': 3.4043, 'grad_norm': 7.66967248916626, 'learning_rate': 2.116666666666667e-05, 'epoch': 0.06}
{'loss': 3.3975, 'grad_norm': 7.471658229827881, 'learning_rate': 2.1e-05, 'epoch': 0.06}
{'loss': 3.4658, 'grad_norm': 7.614603042602539, 'learning_rate': 2.0833333333333336e-05, 'epoch': 0.06}
{'loss': 3.4453, 'grad_norm': 7.848982810974121, 'learning_rate': 2.0666666666666666e-05, 'epoch': 0.06}
{'loss': 3.3582, 'grad_norm': 8.249115943908691, 'learning_rate': 2.05e-05, 'epoch': 0.06}
{'loss': 3.3533, 'grad_norm': 8.15967845916748, 'learning_rate': 2.0333333333333334e-05, 'epoch': 0.06}
{'loss': 3.3967, 'grad_norm': 8.422718048095703, 'learning_rate': 2.0166666666666668e-05, 'epoch': 0.06}
{'loss': 3.3408, 'grad_norm': 7.906637668609619, 'learning_rate': 2e-05, 'epoch': 0.06}
{'loss': 3.3777, 'grad_norm': 9.058789253234863, 'learning_rate': 1.9833333333333335e-05, 'epoch': 0.06}
{'loss': 3.3438, 'grad_norm': 7.802524089813232, 'learning_rate': 1.9666666666666666e-05, 'epoch': 0.06}
{'loss': 3.575, 'grad_norm': 8.010766983032227, 'learning_rate': 1.9500000000000003e-05, 'epoch': 0.06}
{'loss': 3.3469, 'grad_norm': 8.564404487609863, 'learning_rate': 1.9333333333333333e-05, 'epoch': 0.06}
{'loss': 3.4971, 'grad_norm': 9.052900314331055, 'learning_rate': 1.9166666666666667e-05, 'epoch': 0.06}
{'loss': 3.3799, 'grad_norm': 7.466693878173828, 'learning_rate': 1.9e-05, 'epoch': 0.06}
{'loss': 3.3158, 'grad_norm': 8.167703628540039, 'learning_rate': 1.8833333333333335e-05, 'epoch': 0.07}
{'loss': 3.3082, 'grad_norm': 7.937964916229248, 'learning_rate': 1.866666666666667e-05, 'epoch': 0.07}
{'loss': 3.3982, 'grad_norm': 7.377182483673096, 'learning_rate': 1.85e-05, 'epoch': 0.07}
{'loss': 3.3789, 'grad_norm': 7.982194900512695, 'learning_rate': 1.8333333333333333e-05, 'epoch': 0.07}
{'loss': 3.3963, 'grad_norm': 8.033982276916504, 'learning_rate': 1.8166666666666667e-05, 'epoch': 0.07}
{'loss': 3.4803, 'grad_norm': 7.566464900970459, 'learning_rate': 1.8e-05, 'epoch': 0.07}
{'loss': 3.2855, 'grad_norm': 7.877460956573486, 'learning_rate': 1.7833333333333334e-05, 'epoch': 0.07}
{'loss': 3.5033, 'grad_norm': 7.66441535949707, 'learning_rate': 1.7666666666666668e-05, 'epoch': 0.07}
{'loss': 3.3602, 'grad_norm': 6.981980800628662, 'learning_rate': 1.75e-05, 'epoch': 0.07}
{'loss': 3.2848, 'grad_norm': 8.893288612365723, 'learning_rate': 1.7333333333333336e-05, 'epoch': 0.07}
{'loss': 3.3709, 'grad_norm': 7.742636680603027, 'learning_rate': 1.7166666666666666e-05, 'epoch': 0.07}
{'loss': 3.24, 'grad_norm': 7.893410682678223, 'learning_rate': 1.7000000000000003e-05, 'epoch': 0.07}
{'loss': 3.4174, 'grad_norm': 7.204988956451416, 'learning_rate': 1.6833333333333334e-05, 'epoch': 0.07}
{'loss': 3.4672, 'grad_norm': 8.240935325622559, 'learning_rate': 1.6666666666666667e-05, 'epoch': 0.07}
 67%|██████████████████████████             | 2000/3000 [19:54<09:08,  1.82it/s]***** Running Evaluation *****
  Num examples = 50
  Batch size = 16

  0%|                                                     | 0/4 [00:00<?, ?it/s]
 50%|██████████████████████▌                      | 2/4 [00:02<00:02,  1.36s/it]
 75%|█████████████████████████████████▊           | 3/4 [00:18<00:07,  7.22s/it]
                                                                                
{'eval_rouge-1': 31.505186, 'eval_rouge-2': 6.5032820000000005, 'eval_rouge-l': 22.747351999999996, 'eval_bleu-4': 0.032260435589811516, 'eval_runtime': 36.3733, 'eval_samples_per_second': 1.375, 'eval_steps_per_second': 0.11, 'epoch': 0.07}
 67%|██████████████████████████             | 2000/3000 [20:30<09:08,  1.82it/s]
100%|█████████████████████████████████████████████| 4/4 [00:20<00:00,  5.37s/it]
                                                                                Saving model checkpoint to ./output/checkpoint-2000
/root/.local/lib/python3.11/site-packages/peft/utils/save_and_load.py:195: UserWarning: Could not find a config file in /root/dataDisk/models/chatglm3-6b - will assume that the vocabulary was not modified.
  warnings.warn(
{'loss': 3.3883, 'grad_norm': 8.96930980682373, 'learning_rate': 1.65e-05, 'epoch': 0.07}
{'loss': 3.4994, 'grad_norm': 7.852188587188721, 'learning_rate': 1.6333333333333335e-05, 'epoch': 0.07}
{'loss': 3.5566, 'grad_norm': 8.995851516723633, 'learning_rate': 1.6166666666666665e-05, 'epoch': 0.07}
{'loss': 3.4934, 'grad_norm': 8.352027893066406, 'learning_rate': 1.6000000000000003e-05, 'epoch': 0.07}
{'loss': 3.3715, 'grad_norm': 8.199395179748535, 'learning_rate': 1.5833333333333333e-05, 'epoch': 0.07}
{'loss': 3.3248, 'grad_norm': 8.007231712341309, 'learning_rate': 1.5666666666666667e-05, 'epoch': 0.07}
{'loss': 3.4436, 'grad_norm': 8.318451881408691, 'learning_rate': 1.55e-05, 'epoch': 0.07}
{'loss': 3.4145, 'grad_norm': 8.428586959838867, 'learning_rate': 1.5333333333333334e-05, 'epoch': 0.07}
{'loss': 3.4412, 'grad_norm': 7.652554512023926, 'learning_rate': 1.5166666666666668e-05, 'epoch': 0.07}
{'loss': 3.3592, 'grad_norm': 7.713926315307617, 'learning_rate': 1.5e-05, 'epoch': 0.07}
{'loss': 3.2941, 'grad_norm': 7.735483169555664, 'learning_rate': 1.4833333333333336e-05, 'epoch': 0.07}
{'loss': 3.5842, 'grad_norm': 7.9791083335876465, 'learning_rate': 1.4666666666666668e-05, 'epoch': 0.07}
{'loss': 3.26, 'grad_norm': 7.714377403259277, 'learning_rate': 1.45e-05, 'epoch': 0.07}
{'loss': 3.3658, 'grad_norm': 8.57121467590332, 'learning_rate': 1.4333333333333334e-05, 'epoch': 0.07}
{'loss': 3.3994, 'grad_norm': 7.428952217102051, 'learning_rate': 1.4166666666666668e-05, 'epoch': 0.08}
{'loss': 3.5186, 'grad_norm': 8.171857833862305, 'learning_rate': 1.4000000000000001e-05, 'epoch': 0.08}
{'loss': 3.3998, 'grad_norm': 6.827473163604736, 'learning_rate': 1.3833333333333334e-05, 'epoch': 0.08}
{'loss': 3.4209, 'grad_norm': 7.915588855743408, 'learning_rate': 1.3666666666666666e-05, 'epoch': 0.08}
{'loss': 3.3545, 'grad_norm': 7.885632038116455, 'learning_rate': 1.3500000000000001e-05, 'epoch': 0.08}
{'loss': 3.4383, 'grad_norm': 7.6390204429626465, 'learning_rate': 1.3333333333333333e-05, 'epoch': 0.08}
{'loss': 3.4494, 'grad_norm': 6.900352954864502, 'learning_rate': 1.3166666666666665e-05, 'epoch': 0.08}
{'loss': 3.4215, 'grad_norm': 8.044405937194824, 'learning_rate': 1.3000000000000001e-05, 'epoch': 0.08}
{'loss': 3.4225, 'grad_norm': 8.216194152832031, 'learning_rate': 1.2833333333333333e-05, 'epoch': 0.08}
{'loss': 3.3734, 'grad_norm': 8.302413940429688, 'learning_rate': 1.2666666666666668e-05, 'epoch': 0.08}
{'loss': 3.2377, 'grad_norm': 8.46757698059082, 'learning_rate': 1.25e-05, 'epoch': 0.08}
{'loss': 3.366, 'grad_norm': 8.11133098602295, 'learning_rate': 1.2333333333333334e-05, 'epoch': 0.08}
{'loss': 3.4279, 'grad_norm': 8.75830364227295, 'learning_rate': 1.2166666666666668e-05, 'epoch': 0.08}
{'loss': 3.4664, 'grad_norm': 7.905836582183838, 'learning_rate': 1.2e-05, 'epoch': 0.08}
{'loss': 3.2881, 'grad_norm': 8.376313209533691, 'learning_rate': 1.1833333333333334e-05, 'epoch': 0.08}
{'loss': 3.3604, 'grad_norm': 8.32606315612793, 'learning_rate': 1.1666666666666668e-05, 'epoch': 0.08}
{'loss': 3.3184, 'grad_norm': 8.478708267211914, 'learning_rate': 1.1500000000000002e-05, 'epoch': 0.08}
{'loss': 3.3322, 'grad_norm': 8.499276161193848, 'learning_rate': 1.1333333333333334e-05, 'epoch': 0.08}
{'loss': 3.3701, 'grad_norm': 9.254814147949219, 'learning_rate': 1.1166666666666668e-05, 'epoch': 0.08}
{'loss': 3.3631, 'grad_norm': 7.877616882324219, 'learning_rate': 1.1000000000000001e-05, 'epoch': 0.08}
{'loss': 3.2717, 'grad_norm': 8.665705680847168, 'learning_rate': 1.0833333333333334e-05, 'epoch': 0.08}
{'loss': 3.3855, 'grad_norm': 8.352750778198242, 'learning_rate': 1.0666666666666667e-05, 'epoch': 0.08}
{'loss': 3.3553, 'grad_norm': 7.923928737640381, 'learning_rate': 1.05e-05, 'epoch': 0.08}
{'loss': 3.4971, 'grad_norm': 8.748578071594238, 'learning_rate': 1.0333333333333333e-05, 'epoch': 0.08}
{'loss': 3.2361, 'grad_norm': 8.582392692565918, 'learning_rate': 1.0166666666666667e-05, 'epoch': 0.08}
{'loss': 3.4605, 'grad_norm': 7.8934197425842285, 'learning_rate': 1e-05, 'epoch': 0.08}
{'loss': 3.4539, 'grad_norm': 8.299188613891602, 'learning_rate': 9.833333333333333e-06, 'epoch': 0.08}
{'loss': 3.2846, 'grad_norm': 8.140109062194824, 'learning_rate': 9.666666666666667e-06, 'epoch': 0.08}
{'loss': 3.3686, 'grad_norm': 7.281005382537842, 'learning_rate': 9.5e-06, 'epoch': 0.08}
{'loss': 3.382, 'grad_norm': 8.155545234680176, 'learning_rate': 9.333333333333334e-06, 'epoch': 0.09}
{'loss': 3.277, 'grad_norm': 7.974005699157715, 'learning_rate': 9.166666666666666e-06, 'epoch': 0.09}
{'loss': 3.3137, 'grad_norm': 8.045210838317871, 'learning_rate': 9e-06, 'epoch': 0.09}
{'loss': 3.2639, 'grad_norm': 8.81456184387207, 'learning_rate': 8.833333333333334e-06, 'epoch': 0.09}
{'loss': 3.4404, 'grad_norm': 7.457502365112305, 'learning_rate': 8.666666666666668e-06, 'epoch': 0.09}
{'loss': 3.4732, 'grad_norm': 7.957787990570068, 'learning_rate': 8.500000000000002e-06, 'epoch': 0.09}
{'loss': 3.3895, 'grad_norm': 9.519887924194336, 'learning_rate': 8.333333333333334e-06, 'epoch': 0.09}
 83%|████████████████████████████████▌      | 2500/3000 [25:11<04:36,  1.81it/s]***** Running Evaluation *****
  Num examples = 50
  Batch size = 16

  0%|                                                     | 0/4 [00:00<?, ?it/s]
 50%|██████████████████████▌                      | 2/4 [00:15<00:15,  7.64s/it]
 75%|█████████████████████████████████▊           | 3/4 [00:30<00:10, 10.84s/it]
                                                                                
{'eval_rouge-1': 31.574694, 'eval_rouge-2': 7.259876, 'eval_rouge-l': 23.614966, 'eval_bleu-4': 0.032707104003988456, 'eval_runtime': 61.9937, 'eval_samples_per_second': 0.807, 'eval_steps_per_second': 0.065, 'epoch': 0.09}
 83%|████████████████████████████████▌      | 2500/3000 [26:13<04:36,  1.81it/s]
100%|█████████████████████████████████████████████| 4/4 [00:46<00:00, 12.49s/it]
                                                                                Saving model checkpoint to ./output/checkpoint-2500
/root/.local/lib/python3.11/site-packages/peft/utils/save_and_load.py:195: UserWarning: Could not find a config file in /root/dataDisk/models/chatglm3-6b - will assume that the vocabulary was not modified.
  warnings.warn(
{'loss': 3.3045, 'grad_norm': 8.517574310302734, 'learning_rate': 8.166666666666668e-06, 'epoch': 0.09}
{'loss': 3.3381, 'grad_norm': 10.105990409851074, 'learning_rate': 8.000000000000001e-06, 'epoch': 0.09}
{'loss': 3.2463, 'grad_norm': 8.23409366607666, 'learning_rate': 7.833333333333333e-06, 'epoch': 0.09}
{'loss': 3.401, 'grad_norm': 8.258499145507812, 'learning_rate': 7.666666666666667e-06, 'epoch': 0.09}
{'loss': 3.3957, 'grad_norm': 7.867544174194336, 'learning_rate': 7.5e-06, 'epoch': 0.09}
{'loss': 3.4047, 'grad_norm': 8.543951988220215, 'learning_rate': 7.333333333333334e-06, 'epoch': 0.09}
{'loss': 3.4744, 'grad_norm': 8.021391868591309, 'learning_rate': 7.166666666666667e-06, 'epoch': 0.09}
{'loss': 3.4809, 'grad_norm': 8.70193099975586, 'learning_rate': 7.000000000000001e-06, 'epoch': 0.09}
{'loss': 3.3768, 'grad_norm': 8.592949867248535, 'learning_rate': 6.833333333333333e-06, 'epoch': 0.09}
{'loss': 3.4793, 'grad_norm': 8.727974891662598, 'learning_rate': 6.666666666666667e-06, 'epoch': 0.09}
{'loss': 3.3605, 'grad_norm': 8.158490180969238, 'learning_rate': 6.5000000000000004e-06, 'epoch': 0.09}
{'loss': 3.4283, 'grad_norm': 7.835930824279785, 'learning_rate': 6.333333333333334e-06, 'epoch': 0.09}
{'loss': 3.5227, 'grad_norm': 7.622192859649658, 'learning_rate': 6.166666666666667e-06, 'epoch': 0.09}
{'loss': 3.4445, 'grad_norm': 8.733564376831055, 'learning_rate': 6e-06, 'epoch': 0.09}
{'loss': 3.409, 'grad_norm': 8.145842552185059, 'learning_rate': 5.833333333333334e-06, 'epoch': 0.09}
{'loss': 3.3504, 'grad_norm': 7.908388614654541, 'learning_rate': 5.666666666666667e-06, 'epoch': 0.09}
{'loss': 3.4143, 'grad_norm': 8.82931137084961, 'learning_rate': 5.500000000000001e-06, 'epoch': 0.09}
{'loss': 3.268, 'grad_norm': 7.644227027893066, 'learning_rate': 5.333333333333334e-06, 'epoch': 0.09}
{'loss': 3.4768, 'grad_norm': 8.745811462402344, 'learning_rate': 5.166666666666667e-06, 'epoch': 0.09}
{'loss': 3.4518, 'grad_norm': 9.04586124420166, 'learning_rate': 5e-06, 'epoch': 0.09}
{'loss': 3.4314, 'grad_norm': 8.43224048614502, 'learning_rate': 4.833333333333333e-06, 'epoch': 0.09}
{'loss': 3.2516, 'grad_norm': 7.765808582305908, 'learning_rate': 4.666666666666667e-06, 'epoch': 0.09}
{'loss': 3.3777, 'grad_norm': 8.194034576416016, 'learning_rate': 4.5e-06, 'epoch': 0.1}
{'loss': 3.3855, 'grad_norm': 7.980439186096191, 'learning_rate': 4.333333333333334e-06, 'epoch': 0.1}
{'loss': 3.458, 'grad_norm': 8.961882591247559, 'learning_rate': 4.166666666666667e-06, 'epoch': 0.1}
{'loss': 3.4033, 'grad_norm': 8.298755645751953, 'learning_rate': 4.000000000000001e-06, 'epoch': 0.1}
{'loss': 3.3463, 'grad_norm': 8.330297470092773, 'learning_rate': 3.833333333333334e-06, 'epoch': 0.1}
{'loss': 3.2605, 'grad_norm': 8.559603691101074, 'learning_rate': 3.666666666666667e-06, 'epoch': 0.1}
{'loss': 3.2828, 'grad_norm': 8.264541625976562, 'learning_rate': 3.5000000000000004e-06, 'epoch': 0.1}
{'loss': 3.2453, 'grad_norm': 7.755155086517334, 'learning_rate': 3.3333333333333333e-06, 'epoch': 0.1}
{'loss': 3.4465, 'grad_norm': 8.003844261169434, 'learning_rate': 3.166666666666667e-06, 'epoch': 0.1}
{'loss': 3.3779, 'grad_norm': 8.102858543395996, 'learning_rate': 3e-06, 'epoch': 0.1}
{'loss': 3.3934, 'grad_norm': 8.144600868225098, 'learning_rate': 2.8333333333333335e-06, 'epoch': 0.1}
{'loss': 3.4438, 'grad_norm': 9.136582374572754, 'learning_rate': 2.666666666666667e-06, 'epoch': 0.1}
{'loss': 3.4062, 'grad_norm': 8.5354642868042, 'learning_rate': 2.5e-06, 'epoch': 0.1}
{'loss': 3.3441, 'grad_norm': 8.451159477233887, 'learning_rate': 2.3333333333333336e-06, 'epoch': 0.1}
{'loss': 3.377, 'grad_norm': 8.76397705078125, 'learning_rate': 2.166666666666667e-06, 'epoch': 0.1}
{'loss': 3.5102, 'grad_norm': 9.291138648986816, 'learning_rate': 2.0000000000000003e-06, 'epoch': 0.1}
{'loss': 3.3064, 'grad_norm': 8.165060997009277, 'learning_rate': 1.8333333333333335e-06, 'epoch': 0.1}
{'loss': 3.3314, 'grad_norm': 9.14610481262207, 'learning_rate': 1.6666666666666667e-06, 'epoch': 0.1}
{'loss': 3.3064, 'grad_norm': 8.09565258026123, 'learning_rate': 1.5e-06, 'epoch': 0.1}
{'loss': 3.2504, 'grad_norm': 7.350383281707764, 'learning_rate': 1.3333333333333334e-06, 'epoch': 0.1}
{'loss': 3.3639, 'grad_norm': 8.816198348999023, 'learning_rate': 1.1666666666666668e-06, 'epoch': 0.1}
{'loss': 3.2617, 'grad_norm': 8.531412124633789, 'learning_rate': 1.0000000000000002e-06, 'epoch': 0.1}
{'loss': 3.3826, 'grad_norm': 8.157344818115234, 'learning_rate': 8.333333333333333e-07, 'epoch': 0.1}
{'loss': 3.2119, 'grad_norm': 9.016716003417969, 'learning_rate': 6.666666666666667e-07, 'epoch': 0.1}
{'loss': 3.4537, 'grad_norm': 9.010642051696777, 'learning_rate': 5.000000000000001e-07, 'epoch': 0.1}
{'loss': 3.432, 'grad_norm': 9.006465911865234, 'learning_rate': 3.3333333333333335e-07, 'epoch': 0.1}
{'loss': 3.476, 'grad_norm': 8.404202461242676, 'learning_rate': 1.6666666666666668e-07, 'epoch': 0.1}
{'loss': 3.3691, 'grad_norm': 7.905839443206787, 'learning_rate': 0.0, 'epoch': 0.1}
100%|███████████████████████████████████████| 3000/3000 [30:55<00:00,  1.88it/s]***** Running Evaluation *****
  Num examples = 50
  Batch size = 16

  0%|                                                     | 0/4 [00:00<?, ?it/s]
 50%|██████████████████████▌                      | 2/4 [00:15<00:15,  7.63s/it]
 75%|█████████████████████████████████▊           | 3/4 [00:30<00:10, 10.80s/it]
                                                                                
{'eval_rouge-1': 31.774255999999994, 'eval_rouge-2': 7.680910000000001, 'eval_rouge-l': 23.156868, 'eval_bleu-4': 0.033161295681659826, 'eval_runtime': 61.7639, 'eval_samples_per_second': 0.81, 'eval_steps_per_second': 0.065, 'epoch': 0.1}
100%|███████████████████████████████████████| 3000/3000 [31:57<00:00,  1.88it/s]
100%|█████████████████████████████████████████████| 4/4 [00:46<00:00, 12.52s/it]
                                                                                Saving model checkpoint to ./output/checkpoint-3000
/root/.local/lib/python3.11/site-packages/peft/utils/save_and_load.py:195: UserWarning: Could not find a config file in /root/dataDisk/models/chatglm3-6b - will assume that the vocabulary was not modified.
  warnings.warn(


Training completed. Do not forget to share your model on huggingface.co/models =)


{'train_runtime': 1917.3994, 'train_samples_per_second': 6.258, 'train_steps_per_second': 1.565, 'train_loss': 3.4471673177083333, 'epoch': 0.1}
100%|███████████████████████████████████████| 3000/3000 [31:57<00:00,  1.56it/s]
***** Running Prediction *****
  Num examples = 1070
  Batch size = 16
100%|███████████████████████████████████████████| 67/67 [12:29<00:00, 11.19s/it]
```
## 模型经过微调后的OutPath
> `/root/dataDisk/models/chatglm3-6b/finetune_demo/output/checkpoint-3000/`

