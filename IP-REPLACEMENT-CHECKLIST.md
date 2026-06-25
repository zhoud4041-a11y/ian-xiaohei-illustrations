# 将“小黑”替换为自有卡通 IP：需要改的清单

## 结论

真正控制生成结果的是 `ian-xiaohei-illustrations/` 技能子目录中的 6 个文本文件。

其中：

- IP 形象主要由 `references/xiaohei-ip.md` 定义。
- 画风主要由 `references/style-dna.md` 定义。
- 生图 Prompt 主要由 `references/prompt-template.md` 定义。
- `SKILL.md`、`composition-patterns.md`、`qa-checklist.md` 会在工作流、构图和质检阶段反复强化旧的小黑设定，也必须一起修改。

只改 `xiaohei-ip.md` 不够。旧角色会被其他文件里的“小黑、黑色实心、白点眼、细腿、空表情、not cute”等规则重新带回来。

## 第一组：必须修改

### 1. `ian-xiaohei-illustrations/references/xiaohei-ip.md`

这是角色设定的核心文件，建议改名为你的 IP 名称，例如：

```text
references/<your-ip-name>-ip.md
```

需要重写：

- IP 名称和角色定位
- 外形轮廓
- 头身比例
- 脸型、发型、眼睛、嘴巴
- 标志性服装和配饰
- 主色、辅色和固定色值
- 表情范围
- 性格与气质
- 常见动作
- 禁止画错的特征
- 多角度或不同动作下必须保持不变的识别点

建议新增：

- `角色固定特征`
- `允许变化的部分`
- `绝对不能变化的部分`
- `负面提示词`
- `参考图使用规则`

### 2. `ian-xiaohei-illustrations/references/prompt-template.md`

这是最终交给图像模型的 Prompt 模板，是影响成图最直接的文件。

必须替换：

- `Recurring IP character required` 下的小黑英文描述
- `solid-black`
- `white dot eyes`
- `tiny thin legs`
- `blank serious expression`
- `deadpan`
- `not cute`
- Composition 变量中的“小黑在哪里、正在做什么”
- Color use 中的 `Black for ... 小黑`
- “增强怪诞感”编辑 Prompt 中的小黑描述

建议把角色描述拆成固定字段：

```text
Character identity:
Character appearance:
Signature outfit/accessories:
Required colors:
Personality and expression:
Core action:
Character consistency constraints:
Negative constraints:
```

### 3. `ian-xiaohei-illustrations/SKILL.md`

这是技能入口和总工作流，会决定何时调用技能、如何规划图片、生成时必须包含什么。

必须修改：

- YAML 中的 `name` 和 `description`（如果要变成你的个人技能）
- 标题中的 `Ian`、`小黑`
- 核心定位里的默认视觉 IP 描述
- `xiaohei-ip.md` 的文件引用
- shot list 中的“小黑在图里做什么”
- 单张生成要求中的“小黑作为核心动作主体”
- 检查与迭代中的“小黑只是装饰”
- 所有旧角色外形和气质描述

可保留：

- 16:9
- 正文配图工作流
- 一图一个核心结构
- 大量留白
- 非 PPT、非商业插画
- 从文章重新发明隐喻

### 4. `ian-xiaohei-illustrations/references/composition-patterns.md`

这个文件控制角色如何进入构图和执行动作。

必须修改：

- 所有“小黑参与、搬砖、拉线、牵线、走路”等表述
- “小黑动作池”的标题和动作
- 原创隐喻生成法中的角色动作规则
- 反复刻规则中的旧小黑案例

需要根据新 IP 调整动作能力。例如角色是否有手、是否能拿工具、是否适合夸张变形、是否允许变成机器的一部分。

### 5. `ian-xiaohei-illustrations/references/qa-checklist.md`

这个文件会在生成后判断图片是否合格。

必须修改：

- “有小黑”
- “小黑承担核心动作”
- “小黑像吉祥物、表情包或可爱卡通”
- `deadpan / blank serious expression / not cute / not mascot`
- “换掉小黑动作”等迭代规则

建议新增角色一致性检查：

- 发型是否一致
- 服装和配饰是否一致
- 主色是否正确
- 脸部特征是否一致
- 是否多出手指、配饰或身体部件
- 是否错误改变年龄、性别感或体型
- 是否保持参考图中的核心识别特征

### 6. `ian-xiaohei-illustrations/references/style-dna.md`

这个文件定义整体画风，不完全等于角色设定，但会限制角色怎么被画出来。

至少检查：

- “黑色手绘线稿为主”是否适合你的角色
- 黑、红、橙、蓝配色是否与新 IP 冲突
- “不允许可爱、儿童卡通、复杂服装”等规则是否会误伤你的角色
- “怪诞、产品草图感”是否仍是你想保留的方向

如果你的卡通形象本身是彩色、可爱、服装复杂或偏精致，这个文件必须重写，不能只改角色名。

## 第二组：建议修改

### 7. `ian-xiaohei-illustrations/agents/openai.yaml`

这是 Codex 中显示的技能名称、简介和默认调用语。

需要替换：

- `display_name`
- `short_description`
- `default_prompt`

### 8. `examples/prompts.md`

这里的示例全部围绕小黑。虽然不直接控制核心生成，但会影响以后复制使用。

需要替换：

- 技能调用名称
- 小黑名称
- 小黑参与动作的描述
- “增强小黑参与感”示例

### 9. `README.md`

这是 GitHub 首页说明，不直接控制技能运行，但公开仓库必须同步修改。

需要替换：

- 项目名和简介
- Ian、小黑相关介绍
- 使用示例
- 工作流程
- 目录结构
- 作者信息和二维码（如果准备公开为自己的项目）

## 第三组：视觉资产必须处理

### 10. `ian-xiaohei-illustrations/assets/examples/`

这里有 14 张旧小黑样例。技能会把它们当作风格校准参考。

处理方式二选一：

1. 用你的角色重新制作 6-14 张样例并替换。
2. 在新样例完成前暂时移除旧样例，避免图像模型继续模仿小黑。

不建议保留旧小黑样例同时只修改文字 Prompt，视觉参考通常比文字约束更容易影响结果。

### 11. `examples/images/`

这是 GitHub README 展示用的 8 张图片。

它们不属于安装后的核心技能，但如果仓库要公开成你的版本，应替换为你的 IP 样例。

### 12. 建议新增角色参考图目录

建议增加：

```text
ian-xiaohei-illustrations/assets/character-reference/
├── character-front.png
├── character-side.png
├── character-expression-sheet.png
└── character-action-sheet.png
```

最低配置是一张干净的正面全身参考图。更稳定的配置是正面、侧面、表情和动作各一张。

## 推荐修改顺序

1. 确定新 IP 名称。
2. 准备角色参考图。
3. 重写 IP 角色档案。
4. 修改生图 Prompt 模板。
5. 修改 `SKILL.md` 的工作流与触发描述。
6. 修改构图动作规则。
7. 修改 QA 检查标准。
8. 决定保留还是重写现有画风 DNA。
9. 替换旧样例图。
10. 更新 `openai.yaml`、README 和示例 Prompt。
11. 用 3 个不同主题试生成，检查角色一致性。
12. 将修改后的技能重新安装到 Codex。

## 重新安装提醒

GitHub fork 和本机已安装技能是两份独立文件：

```text
GitHub 工作副本：
C:\Users\HP\Documents\Codex\2026-06-09\github\ian-xiaohei-illustrations

Codex 当前使用的已安装副本：
C:\Users\HP\.codex\skills\ian-xiaohei-illustrations
```

只修改 GitHub 工作副本不会自动更新 Codex。修改完成后，需要重新安装或同步技能目录，并重启 Codex。

## 下一步需要你提供

- 卡通 IP 的图片
- IP 名称
- 是否保留现在的白底手绘怪诞画风
- 是否保留红、橙、蓝批注配色
- 角色能否夸张变形
- 角色必须保留的外形、服装和配饰
- 绝对不能出现的画法
