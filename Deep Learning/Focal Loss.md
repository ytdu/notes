论文：[Focal Loss for Dense Object Detection](https://arxiv.org/abs/1708.02002)

Focal Loss可以使模型更加关注在分错的类别上。

普通的Cross Entropy在类别t上的Loss公式为$CE(p_t) = \alpha_tlog(p_t)$，其中$\alpha_t$是类别t的权重。

而Focal Loss对应的公式为$ FL(p_t) = \alpha_t(1-p_t)^\gamma p_t $。

可以看到，Focal Loss多了一项$(1-p_t)^\gamma$，从而当此类别预测正确时该项较小，预测错误时该项较大。其中$\gamma$的经验值为2时在一些任务上效果最好。