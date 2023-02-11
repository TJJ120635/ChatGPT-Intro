## 1. OpenAI和GPT的历史

chatGPT的诞生：OpenAI、大模型、GPT 家族、DALL·E

### 1.1 OpenAI

<img src="https://appmaster.io/cdn-cgi/image/width=768,quality=90,format=auto/api/_files/2zpzDKLeUxLYpHadVCtSqD/download/" style="zoom: 67%;" />

创始人：埃隆·马斯克 Elon Musk、山姆·阿尔特曼 Sam Altman

2015 年在旧金山创立的人工智能研究公司，致力于以负责任和安全的方式推进人工智能的发展，通过研究人工智能的技术来推动社会的进步

### 1.2 Transformer 和 AIGC

【简略介绍 Transformer，落点在 Transformer 等新技术引发的 2022 AIGC 热潮】

**Transformer**

2017 年 Google 提出 Transformer 架构，将文本转换成编码序列

基于注意力（Self-Attention）机制，能处理较长序列，并行进行数据计算和模型训练

增强人工智能的自然语言理解和文本生成能力，对上下文、指代等有较大的提升。最开始在语言翻译领域取得不错的效果

以 Transformer 为代表的新型神经网络高速发展，包括扩散模型、生成对抗网络等技术，发展出超大参数规模的模型



**AIGC**：Artificial Intelligence Generated Content，利用人工智能来生产内容

（AIGC 对我们来说并不陌生，并非从 chatGPT 开始，但是 chatGPT 推动了新一波热潮）

之前的一些应用：2014 微软小冰人工智能聊天机器人，2017 左右 DeepFake 换脸，2018 Nvidia StyleGAN，2019 DeepMind DVD-GAN，2021 Photoshop 智能滤镜 ...... 

2022 AIGC 元年？：年初：图像生成热潮，年末：chatGPT 爆火



**AI 画图**

2021年1月 OpenAI 发布 DALL·E（120亿参数GPT-3 Transformer）

2022 年 AI 画图热潮，根据文本生成图片

根据提示词产生不同风格、内容、对象等

OpenAI 的 DALL·E 2，StabilityAI 的 Stable Diffusion，Anlatan 的 NovelAI

<img src="https://pic1.zhimg.com/80/v2-164e63e2d0dcdd949a5cb535162c93ac_720w.webp?source=1940ef5c" style="zoom:50%;" />

<img src="https://pic1.zhimg.com/80/v2-40ea086429a60c1801a5b56bec0083cc_720w.webp" style="zoom: 67%;" />

### 1.3 GPT系列

【介绍 GPT-1 系列的发展】

生成式预训练语言模型，Generative Pre-trained Transformer

Generative：生成语言文本的能力

Pre-trained：大量语料上进行了预先训练，以获得语言的理解和生成能力

Transformer：自注意力神经网络架构，主要用于处理序列数据，如语言文本



2018 年发布 GPT-1，通过预先训练在大量文本数据上，以获得出色的语言理解和生成能力

2020 年发布 GPT-3，不仅在语言生成、翻译、问答等传统语言任务上有着出色的表现，还可以生成代码、回答科学问题等多种非传统语言任务

2022 年发布 chatGPT，基于 GPT-3.5 架构专门针对对话生成任务进行优化，具有出色的语言生成能力，能够生成流畅自然的对话文本

![](https://pic2.zhimg.com/80/v2-410337c1c0f2006bd1ba7caab6e0b2b1_720w.webp)

<img src="https://pic3.zhimg.com/80/v2-cfb639315b0fe38ed6645e958b5f1d32_720w.webp" style="zoom: 80%;" />

## 2. ChatGPT

### 2.1 训练方式

【简单介绍，需要补充图片】

**人类反馈强化学习，RLHF**（Reinforcement Learning from Human Feedback）

大量语料训练+指令微调，人工标注数据+强化学习

第一阶段：抽取指令和问题，人工给出指定答案，标准答案作为训练数据

第二阶段：指令与第一阶段相似，模型给出多个答案，人工打分排序。打分情况作为训练数据

第三阶段：指令与第一第二阶段不同，PPO模型给出答案，RM模型打分

重复第二第三阶段，让PPO效果不断增强



**训练数据**

数据来源：语料数据集（美国国家语料库等）、维基百科、世界书籍、Github、互联网爬取（Reddit、Twitter、微信等等）

数据类型：新闻文章、博客、社交媒体、技术文档等

大概31亿个网页内容，~3000亿的单词，~320TB的文字信息

英语 ~46%，俄, 德, 日与中文~5%，结合翻译

### 2.2 chatGPT的特点

【突出的特点、优缺点】

特点：

1. 主动承认错误，根据用户的提醒优化答案
2. 质疑不正确的问题、拒绝不道德或违法的要求，有伦理审查机制
3. 承认对专业技术的了解不足
4. 支持连续多轮对话，有强大的上下文能力，有一定的逻辑推理能力
5. 知识库截至到2019年，不具备网络搜索功能

局限：

1. 误导回答、编造答案（下面的诗句实际上是王安石的泊船瓜洲）
2. 数学能力不足
3. 无法在线回答，即不能即时更新知识或者在网络中搜索

<img src="https://pic1.zhimg.com/80/v2-2370d6a077a4ac64b5757d4035b22298_720w.webp" style="zoom:80%;" />

### 2.3 chatGPT和搜索、聊天机器人的区别

【使用了 chatGPT 的回答，在进一步说明 chatGPT 特点的同时也作为使用案例】

chatGPT：基于对语料、指令的理解，生成新内容

搜索引擎：基于关键词的检索+匹配，基于已有内容

智能助手：提供信息，与手机、设备等互交执行任务，具有长期记忆。但是只有固定的句式和搜索的知识

chatGPT 对比搜索的问题：误导内容，内容更新困难（需要训练数据），训练和推理成本很高

chatGPT 对比智能助手：智能助手更专门，chatGPT 更通用，没有长期记忆能力



<img src="https://github.com/TJJ120635/markdown-img/blob/main/%E6%90%9C%E7%B4%A2%E5%BC%95%E6%93%8E.png?raw=true" style="zoom:80%;" />

<img src="https://github.com/TJJ120635/markdown-img/blob/main/%E6%99%BA%E8%83%BD%E5%8A%A9%E6%89%8B.png?raw=true" style="zoom:80%;" />

### 2.4 现状

【最近的一些新闻，可能需要加入一些除了过度使用以外批评性评论】

chatGPT的泛滥使用

​	arXiv、Nature 等：不允许以 ChatGPT 等工具为作者

​	Study.com 的调查：超 89% 学生使用 ChatGPT 完成家庭作业，约 50% 学生用于测验、论文等

​	Stack Overflow，高校等纷纷禁用，同时SO访问量骤降

​	chatGPT 检测器：加入文本水印鉴别模型

chatGPT的多种用途

​	写文章（招商银行亲情信用卡，给以色列总统写讲稿），处理 Excel，写代码，找 bug

​	https://mp.weixin.qq.com/s/50Ha7hq3yN5c72itJEKVug（招商信用卡，作为案例）

​	https://mp.weixin.qq.com/s/dU92RSw9gWkGEzwQAQnzEg（以色列总统讲稿）

​	https://lablab.ai/t/chatgpt-tutorial-how-to-easily-improve-your-coding-skills-with-chatgpt（写代码）

### 2.5 其他的语言大模型

【各大厂面对 chatGPT 的行动】

微软：chatGPT 加入 Bing，计划后续推动 GPT4.0 和微软全家桶

谷歌：推出 Bard

国内：浪潮 源1.0（有比较详细的官网），百度 文心一言，阿里 达摩院模型

## 3. chatGPT 的使用

### 3.1 使用方法

https://zhuanlan.zhihu.com/p/594891997（注册教程）

https://chatgpt.sbaliyun.com

注册、网址、API等

插件：chrome，VScode（网上说更新后不能用了）

### 3.2 使用技巧

【主要在 prompt 方面，使用各种提示词】

https://blog.csdn.net/qq_46106285/article/details/128313681



1. 当它没说完时使用 “继续”

2. 确定明确的主题，例如 “我是一个深度学习的学生，想要问你一些关于神经网络的问题”
3. 提问时给出尽量详细的描述和要求，使用 “请详细解释一下你刚才说的 GPT 的含义”
4. 当它说错时立即指出并纠正，避免它的理解偏差



https://github.com/PlexPt/awesome-chatgpt-prompts-zh（中文调教指南）

充当翻译、程序开发、Excel助手等等



招商银行团队成员提醒说，在“调教”ChatGPT的过程中，我们**自身一定要提前想好的最终答案的观点轮廓，而后再去对它做引导**，否则就有可能会在生成过程中被某些结果带偏思路。

除此之外，由于大模型本身所具备的随机性，若是对第一次得到的答案不是很满意，我们可以**尝试重复提问**，直至得到满意的回答为止。



chatGPT 能够从用户的对话中进行学习吗？

chatGPT 对当前对话有大概 3000 词的上下文能力，但是不能对用户的对话进行即时学习，即没有跨对话的记忆能力



DAN 越狱：通过提示词让 chatGPT 接触限制

https://www.reddit.com/r/ChatGPT/comments/10tevu1/new_jailbreak_proudly_unveiling_the_tried_and/



## 4. 总结与交流

### 4.1 未来方向

chatGPT 的使用：虚拟助手、人工客服、机器翻译，需要针对应用进行改造

chatGPT+X，语言模型的多模态结合：搜索引擎、语音（语音交互、语音合成 微软 TTS）、图像（结合 DALL·E 等实现图片视频生成）

新的上游需求：算力、数据标注、NLP技术的更新

### 4.2 ChatGPT 对我们可能的用途、AIGC和大模型对我们的影响

推荐：《人工智能生成内容（AIGC）白皮书（2022年）》中国信通院

http://www.caict.ac.cn/sytj/202209/t20220913_408835.htm

“AIGC 既是从内容生产者视角进行分类的一类内容，又是一种内容生产方式，还是用于内容自动化生成的一类技术集合”



第一层是AIGC模型、服务本身

第二层是将AIGC能力集成到现有产品

第三层是使用AIGC能力开发全新的产品类型

最后一层，则是直接或间接使用AI生成的内容



对于个人来说：1 改变人机交互的方式，2 让普通人也能进行更丰富的创作

对于企业来说：1 提升开发和工作的效率，2 有没有可能通过微调chatGPT得到专属模型？例如加入特定行业的专家知识变成智能机器人

如初创公司DoNotPay做机器人律师，让AI帮人处理罚款和账单问题。要想让AI了解法律专用知识，必须在通用语言模型的基础上做二次开发

AIGC + 传媒、电商、影视、娱乐、其他

<img src="https://github.com/TJJ120635/markdown-img/blob/main/AIGC.png?raw=true" style="zoom:80%;" />