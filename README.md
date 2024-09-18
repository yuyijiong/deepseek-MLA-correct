# deepseek-MLA-correct
* deepseek-v2使用了MLA注意力，可以大幅减少 KV cache，然而huggingface上deepseek-v2的代码只使用了传统的MHA，并没有节约显存这一功能。
* 我修改了 ``modeling_deepseek.py``，改写了 KV cache 存储的逻辑，使其能够大幅节约 KV cache 。但可能稍微增加推理时的计算量。
