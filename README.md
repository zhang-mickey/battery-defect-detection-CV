# Length Extrapolation 长度外推

Length - Extrapolation Methods for LLMs
长文本大模型的关键技术主要是相对位置嵌入、旋转位置嵌入、位置插值、线性偏置
# Context Window Extension
Train Short, Test Long
# Agent tuning
一种是没有资源去做长文本微调，希望能够从短文本模型直接得到一个可用的长文本模型，这种需求对长度外推的效果要求会比较高，位置内插就不适合他们了；另一种是有资源去做长文本微调，研究长度外推纯粹是为了得到一个更好的初始化模型，这种情况对模型修改带来的初始损失容忍度比较高，只要能够通过微调快速弥补回损失掉的效果即可，位置内插正好是属于此类方法。
# RAG Retrieve Augment Generation 检索增强生成
![image](https://github.com/zhang-mickey/retinanet-medical-CV/assets/145342600/d3692c8e-15bd-4d0f-9807-1d8bfb2594bc)

允许大语言模型在从固定的数据库中抽取相关内容的基础上生成答案，从而限制随意发挥，提升答案的可靠性

利用大语言模型的情境学习（In-context learning）能力，对于某个prompt，如果可以在提交给大语言模型生成答案之前，先把prompt当做查询，（从某个外部资料库中）检索出一些相关的段落，一并提交给大语言模型，就能降低答案的困惑度（Perplexity）
## 召回

# 位置编码
## RoPE

### Out-of-Distribution


#### Perplexity (PPL)

## CBAM 


非线性问题在简单的单层神经网络的模型里是无解的，无论给出多少训练数据
## Stable Diffusion模型种类

### CheckPoint 
文件类型ckpt，safetensors
### LoRA

