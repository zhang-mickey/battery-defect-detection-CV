# Battery defect detection 目标检测



生产过程表面缺陷检测
![image](https://github.com/zhang-mickey/battery-defect-detection-CV/assets/145342600/71a3b8c7-b070-4d42-a1d6-865dcc2dbf07)

实时要求： FPS 

## 场景
工业缺陷样本较少 ：数据增强：镜像、旋转、平移 




## 涂布
检测正、负极材料漏涂、毛刺等缺陷

极片偏移

## 隔膜

## 卷绕 
## 叠片
![image](https://github.com/zhang-mickey/retinanet-CV/assets/145342600/74bf6264-ab1a-4a0d-9e5d-e648103446c9)

mixed defect
主要类型 
![image](https://github.com/zhang-mickey/retinanet-CV/assets/145342600/8633c509-ad66-47eb-9dbe-2613e8e96d00)


## scratch defect

## 褶皱
![image](https://github.com/zhang-mickey/retinanet-CV/assets/145342600/a1cd0f5a-d880-45c3-beb3-43c77956ffe2)

## 卷绕
## 气泡 

# yolo系列

## yolov6

### label assignment标签分配策略
#### OTA
### Decoupled Head 解耦头
原始 YOLOv5 的检测头是通过分类和回归分支融合共享的方式来实现的，而 YOLOX 的检测头则是将分类和回归分支进行解耦，同时新增了两个额外的 3x3 的卷积层，虽然提升了检测精度，但一定程度上增加了网络延时
## YoLov7


#  text-to-speech （TTS）

## 语音合成 Tacotron2

### seq2seq （序列到序列）

# Diffusion

# Length Extrapolation 长度外推
![image](https://github.com/zhang-mickey/retinanet-CV/assets/145342600/79ee682a-4721-448b-a1c9-b85ece60d110)

Length - Extrapolation Methods for LLMs
长文本大模型的关键技术主要是相对位置嵌入、旋转位置嵌入、位置插值、线性偏置

一种是没有资源去做长文本微调，希望能够从短文本模型直接得到一个可用的长文本模型，这种需求对长度外推的效果要求会比较高，位置内插就不适合他们了；另一种是有资源去做长文本微调，研究长度外推纯粹是为了得到一个更好的初始化模型，这种情况对模型修改带来的初始损失容忍度比较高，只要能够通过微调快速弥补回损失掉的效果即可，位置内插正好是属于此类方法。
# Context Window Extension
Train Short, Test Long
# Agent tuning
目前的agents的方法需要prompt示例进行行为约束，而prompt示例会在推理阶段占用很多的token数目，会增加推理的成本，还对模型的长序列能力提出了更高的要求。

# RAG Retrieve Augment Generation 检索增强生成
![image](https://github.com/zhang-mickey/retinanet-medical-CV/assets/145342600/d3692c8e-15bd-4d0f-9807-1d8bfb2594bc)

允许大语言模型在从固定的数据库中抽取相关内容的基础上生成答案，从而限制随意发挥，提升答案的可靠性

利用大语言模型的情境学习（In-context learning）能力，对于某个prompt，如果可以在提交给大语言模型生成答案之前，先把prompt当做查询，（从某个外部资料库中）检索出一些相关的段落，一并提交给大语言模型，就能降低答案的困惑度（Perplexity）

相比大模型另一条道路——微调，RAG具有以下优点：
1. 微调需要较高的门槛（代码能力）与算力支撑，RAG则易于零基础人群上手，只需要用户提供知识（大模型的参考数据即可）并调用API即可；
2. 微调的大模型更新所需知识需要进行再次微调，每次更新知识都需要创建数据集并重新调用算力微调，而RAG则只需要向知识库上传文档即可，不需要算力支撑。
3. 微调大模型在面对微调时数据集未曾出现的问题时会出现大模型幻觉现象（即一本正经说假话），而RAG说的每句话都是通过参考文献生成的，即使在面对知识库中未曾涉及的问题也可以通过设计prompt（提示）来规避大模型幻觉。

RAG的局限性：RAG最初是为简单问题和小型文档集设计的，它通常包括数据解析、索引检索和简单的问答。然而，它在处理更复杂的问题时存在局限性，例如总结整个年度报告、比较问题、结构化分析和语义搜索等。

Agent的引入：为了解决RAG的局限性，文档提出了引入Agent的概念。Agent是一种更高级的系统，它能够执行多轮对话、查询/任务规划、工具使用、反思和记忆维护等更复杂的功能。
## 召回

# 位置编码
## RoPE

### Out-of-Distribution


#### Perplexity (PPL)



#### Few-Shot（FS）
指模型在推理时给予少量样本，但不允许进行权重更新

少样本学习（few-shot learning）技术顾名思义是只使用少量监督数据训练模型的技术
#### CoT


## 
## CBAM 


非线性问题在简单的单层神经网络的模型里是无解的，无论给出多少训练数据
## Stable Diffusion模型种类

### CheckPoint 
文件类型ckpt，safetensors
### LoRA

