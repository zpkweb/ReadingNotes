# TensorFLow.js

在深度学习中，典型的「内循环」训练如下：

1. 获取输入和 true_output

2. 根据输入和参数计算「推测」值

3. 根据推测与 true_output 之间的差异计算「损失」

4. 根据损失的梯度更新参数