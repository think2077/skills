# 美仪自动化AI建设方案

## 一、项目背景

杭州美仪自动化技术股份有限公司始创于2006年，总部位于浙江杭州新加坡科技园，是一家集研发、制造、销售及服务于一体的国家级高新技术企业 。经过近二十年的深耕，美仪已发展成为中国仪器仪表学会理事单位，并荣获“浙江省科技型企业”、“最具成长型企业”等多项殊荣 。

美仪在数字化转型方面已具备一定基础，构建了包括“美仪通”、MES、ERP、WMS在内的信息化矩阵 。更为关键的是，美仪自主研发了“仪表云”平台，实现了仪器仪表的远程监测、数据记录与异常报警，并在最新的3.0版本中引入了“虚拟仪表”概念，展现了较强的数据化运营思维 。然而，这些系统目前仍处于相对独立的状态，数据孤岛现象明显，缺乏一个统一的智能化入口来串联各个业务系统，导致信息流转效率受限。

---

## 二、需求输入

| 模块 | 功能点 | 说明 |
| --- | --- | --- |
| 制度与产品智能问答 | 制度知识库（人力/行政/财务）支持文档人工导入、分类管理、问答溯源 | 产品说明书知识库（1000份文档） |
| 智能事务办理 | 请假/加班/差旅申请自然语言自动填报 | 调用用户信息与制度知识，生成合规表单，对接美仪通系统提交 |
| 智能问数 | 基于角色的营销数据自然语言查询 | 返回结构化数据或图表（饼图/柱状图/折线图），按角色权限隔离数据 |
| 仪表云指令化配置 | 自然语言触发仪表配置指令 | 支持指令匹配、参数生成、执行日志记录 |
| 售后场景智能客服 | 依托公司现有的售后知识库，实现自动化的问题解答、资料查询（含操作文档、操作视频、图片等内容）、工单创建，并在必要时无缝转接人工客服。 | 1、支持用户通过自然语言查询FAQ、知识问答、相关文档、操作视频、图片。<br>2、AI自动触发工单流程：自动识别建单场景--抓取关键信息预填充表单--提交表单确认。<br>3、AI转人工机制：用户明确要求“转人工”、AI回复时低于某个置信度评分、投诉、问题长时间未解决。<br>4、新增“是否解决？”的反馈评价通道。<br>【应用集成接入】<br>1、仪表堂堂APP、售后团队的微信公众号入口/小程序、公司官网。<br>【核心指标】<br>1、售后客服团队接待量中，智能客服自动解决占比。 |
| 统一入口与认证 | 美仪通免登单点登录集成 |  |

---

## 三、痛点分析

**知识资产碎片化**

企业内部积累了海量的制度文档（人力、行政、财务）以及超过1000份的产品说明书和技术文档 。这些高价值的知识资产分散在不同的文件服务器、个人电脑或纸质档案中。员工在面对客户咨询或内部流程时，往往需要耗费大量时间进行“大海捞针”式的查找。

**业务流程繁琐**

已有OA系统，但在请假、加班、差旅等高频事务办理上，员工仍需面对复杂的表单和僵化的审批流程。员工往往不清楚具体的制度细节（如不同城市的差旅补贴标准），导致填写错误、反复退回修改。

**数据分析门槛高**

企业的营销数据、生产数据沉淀在数据仓库中，但获取这些数据通常需要依赖IT部门开发专门的报表或编写SQL语句。对于一线的业务人员和管理层而言，数据获取的门槛过高，无法实现“即想即得”的敏捷决策。

**产品制约用户体验**

工业仪表的配置操作通常需要专业工程师通过复杂的按键组合或特定代码来完成。对于普通用户而言，调整一个阻尼时间参数或输出信号模式可能需要对照厚厚的操作手册进行数十步操作，且极易出错。

通过引入大模型+智能体技术，深度集成于美仪通App与PC端，构建一个覆盖制度问答、产品咨询、智能填报、智能问数、仪表云指令化配置的统一入口，实现从“人找服务”到“服务找人”的转变，最终达成降本增效、提升体验的战略目标 。 

---

## 四、建设方案

### 制度与产品智能问答

**BEFORE**

*   面对1000+份产品说明书和复杂的公司制度，传统的关键词搜索往往返回大量无关信息或无法精确定位到具体条款。
    
*   版本更新滞后，员工可能引用了过期的制度或产品参数，导致合规风险或选型错误。
    
*   大量故障排查经验存在于老员工脑中，未被结构化沉淀，新员工上手慢。
    

**AFTER**

*   AI助理精准理解意图，从海量文档中锁定相关信息，直接返回答案及确切出处，彻底告别无效浏览。
    
*   与文档管理系统深度集成，所有回答均附带明确的**生效日期与版本标识**。
    
*   将文档与经验从**静态的“资源库”** 转变为动态的**“智慧同事”**，确保组织知识**准确、易用、持续进化**，直接赋能于决策质量、运营效率与风险防控能力的全面提升。
    

面向企业知识资产，钉钉AI解决方案运用大模型技术，使AI能够学习并理解企业的产品的性能（产品的资料、测试数据）、应用场景、客户受众群体、案例及相关模板等内容，完成智能问答、智能分析等任务。

#### 产品架构

![image.png](https://alidocs.oss-cn-zhangjiakou.aliyuncs.com/res/KM7qeobNXQeXklpj/img/b9cea326-f520-4623-9183-595e1c7665f8.png)

落地案例

基于大模型技术，让AI学习并理解企业沉淀的产品知识、客户知识以及法律法规和经验等内容，为使用者提供即时的智能问答，增强使用者对产品知识的掌握度，提供更专业的服务，从而提升客户满意度。

[请至钉钉文档查看附件《录屏2025-05-28 13.11.47.mov》](https://alidocs.dingtalk.com/i/nodes/yQod3RxJKGewzDBZuQ035aGeJkb4Mw9r?doc_type=wiki_doc&iframeQuery=anchorId%3DX02mb7hsx5tfq246oqovi)

[请至钉钉文档查看附件《录屏2025-05-28 13.21.24.mov》](https://alidocs.dingtalk.com/i/nodes/yQod3RxJKGewzDBZuQ035aGeJkb4Mw9r?doc_type=wiki_doc&iframeQuery=anchorId%3DX02mb7i2qmipksle18gc5)

[https://agent.dingtalk.com/copilot?code=qJ76YQ7Axl: https://agent.dingtalk.com/copilot?code=qJ76YQ7Axl](https://agent.dingtalk.com/copilot?code=qJ76YQ7Axl)

---

### 智能事务处理

**BEFORE**

*   员工在申请差旅费时，往往记不清不同职级、不同城市的住宿标准，需要反复查询制度文档，不仅耗时且容易填错。
    
*   在填写表单时，大量基础信息（如部门、工号、直属领导）需要重复手动输入，系统未能充分利用已有的用户画像数据。
    
*   复杂的表单在手机端填写体验不佳，容易误触或显示不全。
    

**AFTER**

*   系统需能理解自然语言指令（如“我下周一要去北京出差三天”），自动提取时间、地点、事由等关键信息，并调用用户信息接口补全基础数据 
    
*   自动调用制度知识库进行合规性校验（如检查剩余年假天数、出差标准），对不合规的请求直接提示修正，从源头减少驳回率 。   
    

#### 案例展示

:::
[请至钉钉文档查看附件《演示1.mp4》](https://alidocs.dingtalk.com/i/nodes/yQod3RxJKGewzDBZuQ035aGeJkb4Mw9r?doc_type=wiki_doc&iframeQuery=anchorId%3DX02m0l7t72y3c2qnlw1li)

[请至钉钉文档查看附件《演示1.mp4》](https://alidocs.dingtalk.com/i/nodes/yQod3RxJKGewzDBZuQ035aGeJkb4Mw9r?doc_type=wiki_doc&iframeQuery=anchorId%3DX02md73ipy3zymdrlaxc1j)
:::

[请至钉钉文档查看附件《中超demo.mov》](https://alidocs.dingtalk.com/i/nodes/yQod3RxJKGewzDBZuQ035aGeJkb4Mw9r?doc_type=wiki_doc&iframeQuery=anchorId%3DX02mj9l3rngy6ehvv05vhi)

[https://agent.dingtalk.com/copilot?code=A5ATh1kuJo: https://agent.dingtalk.com/copilot?code=A5ATh1kuJo](https://agent.dingtalk.com/copilot?code=A5ATh1kuJo)

### 智能问数

**BEFORE**

*   营销数据分散在CRM、ERP等系统中，业务人员若想看“上季度华东区电磁流量计销售趋势”，通常需向IT部门提需求，等待排期开发报表，周期长达数天。
    
*   数据敏感度高，不同职级、不同区域的销售人员应只能看到其权限范围内的数据。传统报表工具难以实现细粒度的动态权限控制。
    
*    静态报表无法支持追问和多维度钻取，无法满足深度的分析需求。
    

**AFTER**

*   对接美仪数据仓库，通过自然语言转化为SQL语句
    
*   识别用户身份角色，在查询数据时注入权限过滤条件，确保数据隔离，杜绝越权访问
    
*   自动生成饼图、柱状图、折线图等图表，帮助用户直观洞察数据趋势。
    

:::
通过构建一个对话式的经营分析助理，管理者通过自然语言交互，即可轻松对经营数据进行智能化分析，快速呈现个性化的洞察结果，满足企业对**数据敏捷性与深度分析**的高标准，为企业运营过程中的数据分析与业务洞察带来新机遇，助力企业优化生产资源配置，提升经营效率。

安全可控的自助式、交互式数据分析，用户无需掌握复杂技能即可挖掘数据背后的洞察

可自定义多维度指标查询，支持行业"黑话"指标，能完成复杂数据分析任务，提供媲美专业分析师的分析能力

将AI与BI相结合，不仅能描述和诊断现状，还能预测未来趋势并提出优化建议。为企业带来数据驱动的智能化运营，提升分析效率和价值，赋能业务决策

![image.png](https://alidocs.oss-cn-zhangjiakou.aliyuncs.com/res/ybEnBBx98RdMnP13/img/46620995-5baf-4e5f-838c-f39470ff2f13.png)
:::

#### 方案价值

:::
**经营分析助理提供安全、灵活、专业的对话问数能力，实现自助式、零门槛数据分析，经营管理者可随时随地进行数据洞察，提升企业的运营效率和决策质量。**

**降低数据分析门槛，释放数据价值**

通过自然语言交互,用户无需掌握复杂的数据分析技能,即可高效利用数据进行分析和洞察,充分释放数据价值

**提升数据分析效率，助力企业敏捷经营**

AI自动完成数据处理和计算，秒级响应，大幅提高数据分析的效率

**个性化数据洞察**

可根据特定业务场景和需求，提供个性化的数据洞察结果，数据赋能决策

**降低IT运维成本**

通过自动化的SQL代码生成和数据处理流程，降低IT运维的工作量和成本
:::

#### 方案亮点

:::
**更安全、更准确、更自主，引领企业数智化转型**
:::

![image.png](https://alidocs.oss-cn-zhangjiakou.aliyuncs.com/res/NpQlKa1dMRA0qDvL/img/78ff5da6-f2b0-4761-94f9-c237b68d82a7.png)

**安全可控**

[进度: 已完成]混合云技术架构，核心数据资产存储在客户环境

[进度: 已完成]数据防泄、应用权限、模型安全三重安全体系

[进度: 已完成]精细化数据权限控制，分级分权

[进度: 已完成]提供AI一体机私有化落地解决方案

**准确可信**

[进度: 已完成]上文语境感知，多轮连贯对话深入分析

[进度: 已完成]推理流程定制调优，回答有依据

[进度: 已完成]学习专业领域业务经验，越用越准确

[进度: 已完成]多场景落地，综合准确率90%+

![image.png](https://alidocs.oss-cn-zhangjiakou.aliyuncs.com/res/oJGq76W44Qo6nAKe/img/81153aaa-45fe-4414-baa1-b3f83d7d93a3.png)

![image.png](https://alidocs.oss-cn-zhangjiakou.aliyuncs.com/res/ybEnBBx98RdMnP13/img/aed1682c-0ae9-4679-88b9-16f80a59496d.png)

**开放自主**

[进度: 已完成]多产品形态，钉内AI助理、机器人等，也支持钉外集成

[进度: 已完成]支持文字语音多类问答

[进度: 已完成]适配Mysql、GaussDB、PostgreSQL等多种数据源

[进度: 已完成]支持自选大模型接入

#### 落地案例

![image.png](https://alidocs.oss-cn-zhangjiakou.aliyuncs.com/res/mxPOG5z6LvgPKnKa/img/6c1d69e1-0e4c-4c32-9531-ad01a677d7c4.png)

![image.png](https://alidocs.oss-cn-zhangjiakou.aliyuncs.com/res/3BMqYaRJGpvAqwZL/img/348f6c63-8314-429c-849f-5e7285ff6c5d.png)

![image.png](https://alidocs.oss-cn-zhangjiakou.aliyuncs.com/res/3BMqYaRJGpvAqwZL/img/b1eddb54-baa1-4f0b-90ff-3e47d80fbdda.png)

![image.png](https://alidocs.oss-cn-zhangjiakou.aliyuncs.com/res/3BMqYaRJGpvAqwZL/img/3a9af12c-9de9-43be-a27a-5b8b8cd0328a.png)

![image.png](https://alidocs.oss-cn-zhangjiakou.aliyuncs.com/res/3BMqYaRJGpvAqwZL/img/319af772-8ea9-4e9f-81bd-a2bad00a615f.png)

[https://agent.dingtalk.com/copilot?code=5V2kbOFuWo: https://agent.dingtalk.com/copilot?code=5V2kbOFuWo](https://agent.dingtalk.com/copilot?code=5V2kbOFuWo)

### 售后智能客服

**BEFORE**

*   人工客服响应慢，用户排队久，高峰期体验差
    
*   服务标准不一，依赖员工经验，解答质量不稳定
    
*   人力成本高，重复问题占用大量精力，效率低下
    
*   服务数据难统计，问题无法系统性分析与改进
    

**AFTER**

*   7×24小时即时响应，秒级解答高频问题，用户等待消失
    
*   回复标准统一，知识库支持，服务质量稳定可控
    
*   人工坐席处理复杂问题，人效提升，运营成本降低
    
*   服务数据自动沉淀，问题分类统计，持续优化有据可依
    

[https://design.gemcoder.com/aiHtmlPreview.html?appuuid=2001232008105164800&uuid=2001232008134524928&version=2&appName=%E6%9C%AA%E5%91%BD%E5%90%8D: https://design.gemcoder.com/aiHtmlPreview.html?appuuid=2001232008105164800&uuid=2001232008134524928&version=2&appName=%E6%9C%AA%E5%91%BD%E5%90%8D](https://design.gemcoder.com/aiHtmlPreview.html?appuuid=2001232008105164800&uuid=2001232008134524928&version=2&appName=%E6%9C%AA%E5%91%BD%E5%90%8D)

## 五、基础能力建设

### （1）企业知识库构建

企业知识库利用AI技术实现企业内部知识的智能检索与问答，支持自然语言提问，快速准确地返回制度条款与操作指引。「知识库」是钉钉文档内专业高效的企业知识管理平台，可用于搭建企业知识管理库和企业内部的文档协同管理。操作简单便捷，管理员添加成员后即可多人共享，实时同步，知识库成员可以在其中记录内部协作产出的所有内容。

如何准确地将知识沉淀下来，成为企业当下极为重要的环节。但往往在日常工作中，就会遇到以下问题：

:::
:::
**创作**
:::

员工使用不同的平台或工具创建知识文档，导致知识碎片化。

不同部门或个人的知识文档格式、风格、深度不一，导致知识库混乱
:::
:::
:::
**沉淀**
:::

企业过往资料散落各地，缺乏统一管理，无法高效利用

核心资料掌握在个别员工手上，难以形成共识
:::
:::
:::
**流转**
:::

企业内跨团队分享难，对外传播物料混乱，把控难度高，高效和安全难平衡

知识文档的访问权限设置不当，可能导致敏感信息泄露或重要信息无法获取。
:::

钉钉知识库，帮助企业做好知识的管理，并让它在生产经营中发挥出价值。

#### 创作

*   可以使用文件夹对文档做归类。同时可以选择设置在一个目录树呈现所有的文档，还加入了 logo 和封面功能，让每一个空间都可以定义属于自己的调性。
    

![image.png](https://alidocs.oss-cn-zhangjiakou.aliyuncs.com/res/meonaA7mwY8JnXxj/img/dcd6fac7-d0e0-4586-b9fb-1e0f11e067c4.png)

*   为提升使用文档效率和规范，管理员可以将常用的会议、方案、汇报文档保存为「知识库模板」，这样知识库成员可以一键带入知识库模板，在知识库下写文档高效又规范。
    

![image.png](https://alidocs.oss-cn-zhangjiakou.aliyuncs.com/res/meonaA7mwY8JnXxj/img/3e8cbee3-337f-49d8-99c8-bed840344e03.png)

#### 沉淀

*   零散文件，统一沉淀，本地文件一键上传至知识库，整理方便，清晰呈现，用书本目录方式整理文档，一目了然。
    

![image.png](https://alidocs.oss-cn-zhangjiakou.aliyuncs.com/res/meonaA7mwY8JnXxj/img/a2cc1e68-109b-40ba-bb41-8d8f5fadb4a7.png)

#### 流转

*   针对整个知识库，知识库所有者、管理者可「添加」「修改」「移除」知识库成员权限。此权限设置针对整个知识库生效，添加/修改/移除成员后，将同步拥有/调整/移除对知识库内所有文档对应的权限。
    

![image.png](https://alidocs.oss-cn-zhangjiakou.aliyuncs.com/res/meonaA7mwY8JnXxj/img/563be200-a874-49b3-8357-675260957eb5.png)

*   对知识库及知识库中的文件夹、文档进行分层配置，精细管控，可设置如谁**可以评论、添加协作者等权限，此外还可以开启水印、防泄漏保护**等安全设置，保障知识库数据安全。
    

![image.png](https://alidocs.oss-cn-zhangjiakou.aliyuncs.com/res/meonaA7mwY8JnXxj/img/d67be3b1-3963-43e5-a9fb-7ace411bcae1.png)

### （2）统一AI开发平台底座

#### 企业AI落地面临的挑战

:::
**AI专业人才不足**

企业的场景和流程繁多，AI应用的需求层出不穷，但缺乏大量专业AI人员去构建应用

**担忧企业数据泄露**

AI应用强依赖企业内部的知识、经营数据等有较高隐私性的内容，智能体部署在云端有数据泄露的风险

**专属应用开发难**

专属企业级智能体需要调用内部的系统、流程等，企业需要结合业务特点定制复杂端对端流程和插件

**企业集成难度高**

多模型集成难，且缺乏丰富灵活的集成方式，让智能体嵌入到已有的业务系统中

**应用效果难以保障**

从头构建复杂应用的试错成本高，缺乏专业的评测体系保证应用效果
:::

#### 钉钉企业Agent平台，模型-知识-智能体，打造企业自己的AI

:::
**更低使用门槛：业务人员也能搭建出来一个助理**

角色级模板中心，每个业务角色都可以找到自己的助理

![image.png](https://alidocs.oss-cn-zhangjiakou.aliyuncs.com/res/XNkOM5jmRWQN3OY7/img/f0620f51-59b9-45b4-8efe-481b121ad2d7.png)

预置提示词模板，AI一键润色

![image.png](https://alidocs.oss-cn-zhangjiakou.aliyuncs.com/res/XNkOM5jmRWQN3OY7/img/72eb14d7-762a-4085-8df8-05d4f376472a.png)

无需编写代码，手动勾选即可创建出助理

![image.png](https://alidocs.oss-cn-zhangjiakou.aliyuncs.com/res/XNkOM5jmRWQN3OY7/img/1cfa3155-04f3-4a1c-a53f-0772ebdca70e.png)
:::
:::
**更强安全保障：像管理企业资产一样管理AI**

企业资产精细管理，智能体、知识、模型层层保障

![image.png](https://alidocs.oss-cn-zhangjiakou.aliyuncs.com/res/XNkOM5jmRWQN3OY7/img/bf226fc0-b002-4cbb-8160-c97b16d10aa6.png)![image.png](https://alidocs.oss-cn-zhangjiakou.aliyuncs.com/res/XNkOM5jmRWQN3OY7/img/0fa181f8-4708-42fd-8c61-921743c075a6.png)![image.png](https://alidocs.oss-cn-zhangjiakou.aliyuncs.com/res/XNkOM5jmRWQN3OY7/img/c7908eb0-9986-42bb-a3b4-4e61e23bcc48.png)

知识不越权，不光钉钉文档，本地知识同样无损继承权限

![image.png](https://alidocs.oss-cn-zhangjiakou.aliyuncs.com/res/XNkOM5jmRWQN3OY7/img/91047ef6-562c-4947-84ed-475685c7fb47.png)

敏感词管控，大模型的输入/输出内容有保障

![image.png](https://alidocs.oss-cn-zhangjiakou.aliyuncs.com/res/XNkOM5jmRWQN3OY7/img/98e92e21-3c86-4625-a557-c683255cedd5.png)
:::
:::
**更深企业适配：与客户业态真正融合**

一方集成：钉钉MCP全面接入，业务集成快人一步

![image.png](https://alidocs.oss-cn-zhangjiakou.aliyuncs.com/res/XNkOM5jmRWQN3OY7/img/ecc17504-eac3-41f4-a7b5-01b27a3b0e2c.png)

三方集成：支持企业自有系统接入，Agent无缝调用

![image.png](https://alidocs.oss-cn-zhangjiakou.aliyuncs.com/res/XNkOM5jmRWQN3OY7/img/453fc2bd-5051-45e2-b252-79a375e6de22.png)![image.png](https://alidocs.oss-cn-zhangjiakou.aliyuncs.com/res/XNkOM5jmRWQN3OY7/img/f6db81ba-a67b-4971-ac9e-865a6434cc9a.png)

业务开放：不止于钉钉，AI与企业业务深度集成

![image.png](https://alidocs.oss-cn-zhangjiakou.aliyuncs.com/res/XNkOM5jmRWQN3OY7/img/9060cbe8-7500-4e07-ac47-ac77ca2240b8.png)
:::
:::
**更强效果保障：真正为企业AI业务落地买单**

![image.png](https://alidocs.oss-cn-zhangjiakou.aliyuncs.com/res/XNkOM5jmRWQN3OY7/img/7d85041a-3829-4ffb-94f4-d305b8b2f348.png)

智能体评测，上线前即可保障效果达到生产级别

![image.png](https://alidocs.oss-cn-zhangjiakou.aliyuncs.com/res/XNkOM5jmRWQN3OY7/img/ff78236c-033d-476f-9cd9-01f636e6e5b3.png)![image.png](https://alidocs.oss-cn-zhangjiakou.aliyuncs.com/res/XNkOM5jmRWQN3OY7/img/3a51f002-6d98-4bcd-9c8c-1a9808198263.png)

智能体运营，智能体真实使用效果一目了然

![image.png](https://alidocs.oss-cn-zhangjiakou.aliyuncs.com/res/XNkOM5jmRWQN3OY7/img/27c7f4a7-2bf7-4c47-ac01-0925ee58336e.png)

智能体观测，给你的智能体做一次深度“体检”，链路级跟踪到每一个问题

![image.png](https://alidocs.oss-cn-zhangjiakou.aliyuncs.com/res/XNkOM5jmRWQN3OY7/img/f93c5ebb-2784-494c-998e-87aea160736c.png)

![image.png](https://alidocs.oss-cn-zhangjiakou.aliyuncs.com/res/XNkOM5jmRWQN3OY7/img/011540f8-5550-4ac8-8025-f3ed81527683.png)
:::