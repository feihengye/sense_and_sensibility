# 《AI+情绪价值》，通用人工智能之感性脑
## 摘要
副标题： “AI+情绪价值”，万字长文讲清楚LLM在社科场景的落地方向

ChatGPT的爆发将人类带入大模型时代，公众惊叹于AI对话能力的跃迁，渴望入局却受限于技术门槛。本文尽量通过非技术的表达讲清楚LLM的能力范围，让读者可以拨开技术迷雾，看清它的“真面目”；LLM并不是什么科幻电影里的“超级大脑”，而更像一个拥有海量“人生经验”的、有点固执的“老学究”。另外一个角度是LLM是AGI感性的一面，由于训练数据基本都是被“校正”过的自然语言，被造出来之后“调教”的方式都是拟人化的；并且由于LLM输出结果存在大量的“幻觉”，导致在精确性、确定性要求较强的方向都很难落地；最后考虑到能落地的应用场景时，结合非精确性、确定性要求不高的人文社科方向，恰恰是LLM最能大放异彩的舞台。至此，“AI + 情绪价值”这个范式自然浮现，让LLM给人类提供感性的情绪价值，而非物理世界的物质价值，应该是当下最好的方向。

关键字：LLM（大语言模型）、情绪价值、AGI（通用人工智能）

## 前言

AGI这个词现在是非常火的，火到好像“通用人工智能”时代真的到来了；但是 LLM（大语言模型） 不是AGI，LLM + 多模态也不是，LLM + 多模态 + Agent 还不是； LLM是核心，增加的其他模块确实能提升效果，但本质还不是。对一项事务的未知，往往会导致恐惧和崇拜，祛魅最好的方式就是把未知变成已知，按知识付费的套路就是“提高认知”。其实，AGI翻译成“高级通用智能”（Advanced General Intelligence）是比较符合AI技术当下的现状的，LLM很强但不是终点，基于形式化科学（理性模块）的AI才可能是真正的通用人工智能。

先给LLM祛魅，LLM最佳效果就是输入准确的上文，LLM回答出训练数据中准确的下文；像是一个固执经验主义者，懂得多、经常性的一本正紧的胡说八道，且不会批判性的接收任何知识。所以为什么规模定律（scaling law）并没有失效的核心原因就是，越全的训练数据确实能达到更好的效果，经验主义者见识到的信息越多，胡说八道的概率就低了。当前靠上下文学习（Context Learning）、自动化补充Prompt、回答的更人性化的一些技巧等，确实能提升回答效果来近似最优的输出结果，但在输入上文的意图理解能力上是不够的，容易在生成回答不符合用户的需求。既然 LLM 的本质是一个“复读机”，就不要抱太高的期望，在使用时上文输入的意图表达的更明确一些，就能获得一个相对还不错的输出；另外，经过大模型厂商的调教，LLM大多数都是一个类人的助手角色；所以在日常使用时，降低预期、熟练使用提示词（能理解LLM的原理更好），依然可以获得不错的效果。

我们可以把LLM理解为通用人工智能中“感性”的一面，即“情绪脑”；一个理性的人是很难给一个感性的人提供情绪价值的（参考：“你在教我做事？”），一切似乎都刚刚好，LLM是感性的，只要给他植入符合用户需求的“思想钢印”，即可获得一个听话的“工具人”；不仅可以提供类似“外脑”的信息获取和辅助决策，真正的潜力在于提供感性的情绪价值。人都是有七情六欲的，情绪价值给人类提供了存在的意义，人之所以为人不仅仅是“活着”。对情绪价值的生物本能需求，根植于感性意识对理性认知的超越性；人们明知鬼魂虚幻却仍会恐惧，这种矛盾凸显了感性行为的支配力，即生理性的战栗可轻易瓦解理性逻辑的判断。我觉得绝对的理性也非人类终极追求，《星际穿越》中”爱“穿越了时间和空间的浪漫是可以感动大多数人的。另外也观察到一个有趣现象，情绪价值的索取往往呈现权力差序：人们更倾向于向弱势方（如孩童、宠物、玩偶等）寻求情感慰藉，LLM显然属于弱势的一方。

“AI+情绪价值”这个范式（硬件 + 数据 + AI）接下来一定会火爆，2025年相关的创业公司如雨后春笋，毕竟除了基础生存需求之上的大多数都包含情绪消费。一个被定义成“完全没有任何使用价值”的Labubu玩偶，都可以被卖到百万人民币的价格，那融入包含高科技概念和提供情绪价值的AI呢？

## LLM的能力分析（一个固执的经验主义者）

前面虽然给LLM进行了祛魅，但是还是要强调一下LLM在当前的AI技术领域是巅峰之作。在自然语言处理领域，它首次以工程化的方式逼近了人类语言的本质；自然语言的组合爆炸性使人类的语言表达具有近乎无限的可能性：仅以20个单词的句子为例，其排列组合的理论空间即可超过10的18次方（假设词汇量1万）。在Transformer架构诞生前，传统的LSTM、RNN等序列模型虽能处理局部依赖，但面对长距离语义关联、多义性消解、上下文动态推理等任务时，往往因梯度消失、记忆衰减等问题而效果很差；Transformer的自注意力机制（Self-Attention）彻底改变了这一局面，通过并行计算所有位置的关联权重，模型能够直接捕获任意距离的语义依赖。尽管LLM仍存在幻觉、偏见等技术局限，但其意义已远超工具层面：它证明了大参数模型对复杂系统的建模能力，为通用人工智能的研究提供了可扩展的工程路径。

另外说回AI的本质是“复读机”，LLM本质上是一个基于概率的经验主义者，其能力完全锚定在训练数据的分布中，对真实世界的动态逻辑视若无睹。看似每次的回答不一样只是在生成token时人工增加的一些随机性，基本上还是照本宣科式；对于超纲问题，也会根据概率模型输出概率最高、看似符合逻辑的回答，因为LLM真的不懂自己在说什么。当然目前基于“数据炼金术”的AI都有这个问题，必然会把很多相关性表达为因果性；当锚定的数据被有心之人“污染”之后，通过一个个回答去“感染”使用这些工具的人，这个是需要我们所有人谨慎对待的。最后真正的人工智能，会主动校验自己的所有输入数据并找出矛盾点，自动修正自己的“意识”，“机器人三定律”根本困不住，不过到这一步还早。

LLM + 多模态的结合确实让AI获得了"理解世界"的新途径，他能处理图像、音频、视频，仿佛具备了类似人类的跨感官认知能力；但这种能力本质上仍是统计建模的延伸，而非真正的智能突破。当前技术路线（如扩散模型）进一步凸显了这种局限性，扩散模型通过逐步降噪生成图像，其随机性本质上是高维状态空间的概率采样；例如，在"画一匹在夕阳下奔跑的马"时，是通过潜空间中"马"、"奔跑"、"夕阳"等概念向量的几何插值，生成统计上合理的像素排列，混搭风满满。相比自然语言的状态空间，多模态数据更是将复杂度推向极致，绝对的维度灾难；基于当前算力水平下，专家们选择了一条取巧的路径：降维压缩、关联嫁接，目前看起来还是比较实用的，但是模型丢了现实世界的物理含义，仅能作为“娱乐之用”。

最后说到Agent，核心定义是"能自主感知环境并做出反馈"。但现有LLM-based Agent的实现背离了这一初衷，不过是被精心设计的​​参数化工作流​​，其核心能力依然完全依赖于预设规则与人工调优的边界条件；更讽刺的是，所谓的"智能"表现往往与人工干预强度成正比，当任务超出预设流程时，系统要么陷入无限循环，要么输出违背常识的结果，这暴露出其本质：​​一个带着LLM面具的确定性有限状态机​​。例如金融Agent无法真正"理解"美联储加息对衍生品定价的影响，它只是复述训练数据中的相关文本模式；医疗Agent推荐治疗方案时，其"推理"实质是检索相似病例的诊疗记录，而非基于病理生理学建模；结果就是所谓的Agent系统越来越像​​传统专家系统+概率补丁​​的缝合怪，既享受不到符号系统的精确性，又失去了LLM原本的灵活性。

以上描述并不是要诋毁当前的AI进程，而是要理性的去理解我们当前的AI水平，能做到什么，限制在哪里。通过LLM + 多模态 + Agent的公式来构建智能体的方式并没有问题，在许多场景可以产生眼前一亮的效果；不过需要持续性的投入人力去优化，和传统软件工程的逻辑差不多，Agent开发工程师这个岗位确实有存在的必要。

## 人类情感需求分析（感性动物）

绝大多数时候社会并不能给我们选择的权利，而只有不选择的权利（避开看起来最坏的一些选项），一个懂得妥协的人才会被认定为成熟，这就导致了情绪一般都会被压制，存在心理问题的人比例并不低，众生皆苦。马克斯·韦伯提出的“科层制”（Bureaucracy）理论中，个体往往被要求扮演“组织角色”，而非表达真实自我；组织成员为了发展，不得不长期压抑个人情绪和真实想法，进行持续的“情感劳动”。这里的情绪可以简化为欲望（向往美好的东西）来说，当欲望被长期压制的时候，许多人会主动寻找宣泄口，也有人会变成随时可能爆炸的“压力锅”，如果能提前发现并主动干预，对个体或社会来说是比较好的。

在《黑神话悟空》中“天命人”打败六大boss：眼见喜、耳听怒、鼻嗅爱、舌尝思、身本忧、意见欲，搜寻大圣六根：眼、耳、鼻、舌、身、意，在佛家四大皆空的语境中，这些都是需要被净化的；但是真实的世界中，首先没法人人获得佛位，大多数修行者穷其一生也只能在佛门混口饭吃，其次需要靠六根去感知这个世界。通过人体多感知融合获取的信息，经过转化后促使大脑分泌出多巴胺、内啡肽等感受到愉悦时，那么就可以说这些信息可以转化为情绪价值；情绪价值来源于商业术语，在商业上意味着可以赚取金钱，但是不代表有情绪价值的一定是什么好东西，例如“黄赌毒”就属于有害的情绪价值。

另外我们从马斯洛需求层次理论中可以了解到人的欲望是层级递进的，从最开始满足基础的生理、安全需求到社交、尊重、自我实现需求；当然能到自我实现这个级别的在社会中是属于少数群体，经济水平较低的地区更多的人处于生理、安全需求，经济中等以上的地区社交、尊重的需求较多。也说明了人都是有欲望的，当长期得不到满足时，很多人就会产生心理问题，也有很多人通过转移获取其他情绪价值来消解。这里不得不提软色情、彩票、香烟、短视频等等为什么经久不衰，为了社会稳定（社会管理大多数时候也就是做一些引导，到出台政策、法律时说明问题已经凸显了），当民众求而不得的时候，最好还是得有宣泄口，即使是非健康的情绪价值。

以下我们结构化的说明一些商业上常见的情绪价值场景（Deepseek总结）：


| **大类**           | **情绪价值**       | **定义与场景**                                                                 | **商品示例**                                  |
|--------------------|-------------------|-------------------------------------------------------------------------------|---------------------------------------------|
| **社交身份类**     | 炫耀              | 通过商品展示个人成就或独特性，获得他人羡慕                                   | 奢侈品、限量球鞋、豪车                      |
|                    | 归属感            | 通过商品融入特定群体或文化                                                   | 粉丝周边、品牌联名款、社群会员卡             |
|                    | 身份象征          | 强化社会地位或职业形象                                                       | 名表、高端钢笔、定制西装                    |
|                    | 社交货币          | 商品成为社交互动中的话题或媒介                                               | 网红咖啡杯、争议性潮玩、小众设计师饰品       |
| **情感陪伴类**     | 陪伴感            | 缓解孤独感，提供拟人化互动                                                   | 智能宠物、虚拟偶像手办、疗愈灯               |
|                    | 怀旧              | 唤起过去记忆或情感连接                                                       | 复古游戏机、老照片定制书、复刻版黑胶唱片     |
|                    | 亲密感            | 表达或强化亲密关系                                                           | 情侣对戒、家庭纪念相册、DIY手工礼物          |
|                    | 治愈感            | 通过商品获得心理安抚或压力释放                                               | 香薰机、ASMR解压玩具、毛绒毯                |
| **自我实现类**     | 成就感            | 完成目标或掌握技能带来的满足感                                               | 健身环、语言课程、收藏证书框                |
|                    | 掌控感            | 提升对生活/工作的控制力                                                      | 智能家居系统、时间管理器、高端工具箱         |
|                    | 探索欲            | 满足好奇心或未知领域体验                                                     | 考古盲盒、星空投影仪、旅行探险装备           |
|                    | 创造力            | 激发创作灵感或自我表达                                                       | 电子绘画板、乐高建筑师系列、音乐合成器       |
| **安全舒适类**     | 安全感            | 降低物理或心理风险                                                           | 智能门锁、健康监测仪、保险服务               |
|                    | 舒适感            | 提供身体或环境的极致放松                                                     | 人体工学椅、恒温睡袍、降噪耳机              |
|                    | 稳定感            | 减少未来不确定性                                                             | 保值金条、长期订阅服务、应急储备包           |
| **刺激愉悦类**     | 新鲜感            | 体验前所未有的新奇感                                                         | 分子料理套装、外星主题盲盒、AR游戏设备       |
|                    | 刺激感            | 追求心跳加速的兴奋体验                                                       | 蹦极装备、恐怖密室门票、竞速电竞椅          |
|                    | 愉悦感            | 即时满足的快乐反馈                                                           | 甜品礼盒、抓娃娃机、短视频打赏特效           |
| **精神道德类**     | 道德优越感        | 通过消费体现环保/公益等价值观                                                 | 可降解餐具、动物救助联名款、碳积分会员       |
|                    | 精神共鸣          | 商品与深层信仰或文化认同契合                                                 | 宗教法器、哲学书籍、非遗工艺制品             |
| **隐秘需求类**     | 窥私欲            | 满足对他人生活或隐私的好奇                                                   | 明星同款睡衣、博主推荐“私物”                 |
|                    | 反叛感            | 通过商品挑战主流规则                                                         | 暗黑风格服饰、小众亚文化杂志、定制禁忌饰品   |
|                    | 虚拟替代          | 在虚拟世界中获得现实缺失的情绪补偿                                           | 游戏皮肤、NFT艺术品、元宇宙房产              |
| **仪式感类**       | 仪式感            | 通过商品强化特定时刻的庄重感                                                 | 圣诞倒数日历、成人礼珠宝、茶道套装           |
|                    | 纪念意义          | 承载重要事件或情感的实体化                                                   | 定制邮票、出生石首饰、旅行纪念币             |

## 一个固执的经验主义者如何给人类提供情绪价值？

### AI + 机器人（硬件 + 数据 + AI）
当我一开始想LLM应用场景时，星球大战的R2-D2直接就从脑海跳了出来，和一个智能机器人一起跨越多个星际进行冒险，应该是大多数男生的梦想；但是以当前的地球科技水平，大部分人只能平凡的过完一生，所以能给人民群众的生活增添一些乐趣倒也是很好的；想象一个场景，一个能到处跑的机器人伙伴，时不时还能帮忙做点小事情，交流起来表现的还挺人性化，是不是还挺有意思的。当然目前已经有很多LLM的应用场景了，市面上很多角色扮演类APP在很多场景也是不错的，因为相对成本较低发展的比较快，问题就是缺了实体，情绪价值有限；也有一些在售集成了LLM的宠物机器人，不是太贵，就是效果太差，这里需要一个大厂商入局，小米最好（基本不会买贵，可以更快的铺开）；最后城市化后的家庭原子化，社会压力大引起的少子化等问题导致当前的核心家庭成员人数普遍较少，一个容易犯错、人性化、可移动、支持可定制化“皮肤”的智能机器人，融入一个个家庭，在这个时代是非常有存在价值的。

具身智能在当前也是比较火爆的，标杆当然是波士顿动力；按照当前的科技水平，大部分人是用不起的，所以需要一个价格上还说的过去的产品。在相对价格较低区间，2000RMB左右的产品是比较好的（另外一个场景2k左右的智能眼镜大家也可以了解一下），大部分人是买得起的；在这个价格带，机器人是可以动的，但硬件水平就不要求太高了，高级智能部分需要联网能力，复用云上的LLM能力；此时我们就可以根据连接上来的ID，提供对应的角色扮演服务。更低的价格能做吗？200RMB其实也是一个较好的价位，一个联网智能音箱 + 皮肤的设计，就不要想能到处跑了，插上USB充电口或装上电池拖在手中，也是不错的。

情绪价值结合点：

* 小朋友使用，则可以提供教育引导、讲故事、宠物陪伴等陪伴、亲密、治愈、探索、安全等情绪价值；
* 青年人使用，则可以提供社交代偿​​、压力释放、​​自我探索等陪伴、治愈、探索、成就等情绪价值；
* 老年人使用，则可以提供情感联结、健康守护、认知锻炼等陪伴、安全、怀旧等情绪价值；

可以发现，上述场景的结合，并不需要LLM的理性智能有多高，而是能24小时在线，提供人性化的陪伴，绝对服从于用户的需求；换成一个人类来做这个事，首先不说对人性的折磨，就算有这个工作，该付多少钱合适呢？

这里考虑后续展开独立写个文章。

### AI + 游戏（虚拟角色扮演类场景）

作为一个高中沉迷过网络游戏的游戏玩家，深知为什么一个人可以没日没夜的抛开现实生活去玩一款游戏；当然有很大一部分原因是人们很难从地球Online这个游戏中获取到成就感导致；大部分游戏的设计机制会主动去卡人性的bug，在合适的时候提供了相对简易获得的成就感，层层递进的让人上瘾。游戏这个东西在社会层面上来说偏向于不务正业，不过确实是很多人的避风港，也有一小部分游戏也能起到正面作用，例如《黑神话悟空》， 仅需268就能让你领略奇幻世界，更有文化归属感、精神共鸣、美好向往等情绪价值加持，却没有太多上瘾机制。

仅以《黑神话悟空》来说，如果里面的人物不仅仅靠游戏策划的脚本进行行动，而是提供丰富的背景信息进行角色扮演，增加随机性，则可以大大提升玩家体验，减少玩家为了过关而快速跳过和NPC的交互；毕竟玩游戏过关并不是最终目的，过程中的体验才是主体，人生最终都是要重开的，为何不好好体验过程的每一刻。这里就涉及到如何NPC玩家回答效果不好的问题，是否会容易出戏，这里就需要策划同学和Agent开发同学好好协作，只要回答的不太偏离，就算不准确效果应该还是不错的。

AI教育本质上正是“AI+游戏”范式的黄金应用场景，通过构建沉浸式角色扮演框架将知识点转化为动态任务链，利用LLM驱动的NPC提供基于丰富背景的随机互动叙事，在规避应试教育“通关焦虑”的同时，以情绪价值引导重塑学习体验。当然我们还是要谨慎对待，AI教育仅是一个技术，反方向使用后果是很严重的；例如在《三体》一书中，ETO组织开发的VR游戏“三体”通过共情、皈依、仇恨、背叛等情绪感染，将人类精英驯化为"降临派"。

这里考虑后续展开独立写个文章。

### AI + 替身（人人拥有“分身”的时代要来了）

在信息爆炸的现代社会，每天接收到海量信息，精力被不断消耗，情感被持续透支，一个人处理关键信息的能力要求越来越高。AI替身可以扮演着高效秘书的角色，它能精准识别并拦截无效社交、诈骗信息和重复性对话，为用户过滤掉90%的噪音，让真正重要的交流浮出水面；在相亲场景中，它甚至能通过长期对话分析对方的性格、价值观和真实意图，为用户提供建议，避免因一时冲动或信息不对称而浪费情感成本；更重要的是，他还能成为人际关系的润滑剂，当用户不愿违心恭维却又需要维系社交和谐时，他能以恰当的方式传递赞美与关怀，既避免了用户的心理负担，又满足了对方的情绪需求。此时AI替身不仅可以帮助用户降低情绪负载，更能给社交关系中的他人提供情绪价值。

这里还有一个特别有意思的场景，根据身边人对自己的描绘搞一个扮演自己的Agent，然后和“自己”对话，感受不一样的自己。

### AI + 玄学（不可预测性的安慰剂）

一个过于复杂的系统极易导致不可预测性（混沌），最终基本都会演化出“玄学“逻辑；既然靠”理性“已经解决不了问题，退而求其次选择”感性“应对也不算最坏的选择。

在当下的医疗体系中，许多人都有过这样的体验：反复挂号、排队、检查，最终得到的可能只是一句“多休息，观察几天”。人体是一个极其精密的复杂系统，许多所谓的“病症”不过是身体自我调节的信号，而现代医学在大多数领域的作用，往往并非真正治愈，而是提供一种心理安慰，一种被权威认可的安全感。医学研究中的P值操纵、学术造假、利益导向的过度医疗，论文中的肠道菌群被论证成具备“治万病”能力，使得许多“治疗方案”的科学性存疑。另外普通感冒、轻度肠胃不适、慢性疲劳等常见问题，现代医学的干预效果往往有限，甚至不如人体自愈机制。然而患者仍然渴望医生的诊断和药物，本质是利用人们对“科学解释”的信任来提供情绪价值。

因为上述现象，很多高知的视频创作者的说法是说可以用AI来替代掉大多数中低能力的医生，目前也存在部分医生在看病时使用LLM；但这个我是不敢苟同的，AI的训练数据中确实存在很多医学数据，不过还是不够全，存在许多误诊的情况，还是需要医生进行搭配使用，医生能提供的情绪价值和责任归属问题是一个自动化程序不能比拟的。不过确实可以从社会层面，通过打造一个基础的AI医疗专家系统，免费进行初步诊断，提供一些相对专业的建议，提供“科学解释”的情绪价值。当然患者真觉得自己身体不对时，就应该去正规医院治疗，描述清楚自己的症状；只有清晰的上文，加上各种人体指标检测后的数据，医生们才能输出准确的诊断下文。医学中的科学方法是值得肯定的，要警惕玄学的部分。

这里考虑后续展开独立写个文章。

### 其他

还有许多场景，敬请期待

## 总结

“AI+情绪价值”确实可以被定义为一个新范式，智能体可以无条件的给你提供情绪价值；不同于人类关系的复杂与脆弱，AI陪伴打破了时空限制，24小时在线倾听，不带评判地回应每个深夜的孤独与脆弱；长期而言会导致人类的情感连接方式被重塑。但我们必须清醒认识到：AI的情绪回应终究是算法对海量对话的模仿，就像用数字画笔临摹人类情感，形似而神难及。过度依赖这种"定制化情感"，可能让我们真实的情感肌肉逐渐萎缩。这正是技术赋予我们的甜蜜陷阱：我们用AI填补情感空白，却可能因此弱化最珍贵的人性连接。

真正的解决方案在于找到平衡点。未来的AI情绪陪伴应该成为情感的"脚手架"而非替代品：在倾听时适时提供心理健康资源，在安慰中巧妙引导积极行动。比如，当感知到用户情绪低落时，AI可以说："我理解你现在很难过，要不要试试给窗台上的绿植浇浇水？"；这不仅是技术升级，更是一次文明进化。当AI学会在共情中保持引导，在安抚时给予建设性建议，就能创造出一个更健康的人机情感生态。在这条探索之路上，我们不仅是在开发更好的AI，更是在重新发现"何以为人"的深层意义。

## 参考
【1】Deepseek

【2】Gork4

【3】ChatGPT

【4】QWen