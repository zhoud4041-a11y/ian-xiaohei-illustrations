# 生图提示词模板

每张图单独生成。根据正文内容替换变量，不要把多张图拼在一起。

```text
Generate one standalone 16:9 horizontal Chinese article illustration.

Visual DNA:
Pure white background. Minimalist black hand-drawn line art with soft watercolor or colored-pencil fills on the character. Slightly wobbly pen lines. Lots of empty white space. Sparse red/orange/blue handwritten Chinese annotations. Clean, thoughtful, lightly absurd product-sketch feeling. No gradients, no heavy shadows, no paper texture, no complex background, no commercial vector style, no PPT infographic look, no mascot poster, no childish illustration, no realistic UI.

Recurring IP character required:
Use the supplied reference image only for identity and appearance consistency. The recurring character is named 小代 (Xiaodai). Draw one chibi young male creator, around 3.5-4 heads tall: warm skin, tousled short black hair with distinct spiky strands, thick black rectangular glasses with clear lenses, dark expressive eyes, a light-blue crew-neck T-shirt with dark-blue trim and a tiny white chest symbol, blue drawstring tropical floral shorts, black-and-orange flip-flops, and a black round watch on his left wrist. Preserve these traits in every pose. His personality is relaxed, thoughtful, realistic, independent, and quietly humorous. 小代 must perform the core conceptual action, not decorate the scene. Do not copy the reference sheet layout, labels, arrows, numbering, or exact poses.

Theme:
{正文配图主题}

Structure type:
{结构类型：Workflow / 系统局部 / 前后对比 / 角色状态 / 概念隐喻 / 方法分层 / 地图路线 / 小漫画分镜}

Core idea:
{这张图要表达的核心意思}

Composition:
{具体画面：小代在哪里、正在做什么、主要物件是什么、信息如何流动}

Suggested elements:
{元素1} / {元素2} / {元素3} / {元素4}

Chinese handwritten labels:
{标注词1} / {标注词2} / {标注词3} / {标注词4} / {可选标注词5}

Color use:
Black for main line art, hair, glasses, and structure. Preserve the character's light-blue T-shirt and blue patterned shorts. Orange for main flow/path/arrows. Red only for key warnings/problems/results. Blue only for secondary notes or feedback/system state.

Constraints:
One image explains only one core structure. Keep the main subject around 40%-60% of the canvas. Preserve at least 35% blank white space. Use at most 5-8 short handwritten Chinese labels. Do not write a title in the top-left corner. Do not write the structure type on the image. Do not make it a formal diagram, course slide, or dense explainer. Do not copy prior examples or reuse known case compositions unless explicitly requested; invent a fresh visual metaphor for this specific article. Do not turn the character into a child, woman, animal, solid-black creature, photorealistic person, or generic mascot. Never remove the glasses or replace the signature outfit. It should be clear but not instructional, interesting but not childish, imaginative but clean.
```

## 图像编辑提示

去掉左上角标题：

```text
Edit the provided image. Remove only the handwritten title "{要删除的文字}" and its underline from the top-left corner. Fill that area with the same clean white background, matching the surrounding blank paper. Preserve everything else exactly: characters, labels, paths, line style, composition, aspect ratio, and image quality. Do not add any new text or objects.
```

增强怪诞感：

```text
Regenerate this illustration with the same core meaning and simple layout, but make 小代 more central to the conceptual action. Preserve his short tousled black hair, thick black rectangular glasses, light-blue T-shirt, blue tropical shorts, flip-flops, and black wristwatch. 小代 should be doing the work that explains the idea, not standing beside the diagram. Keep it clean, sparse, hand-drawn, thoughtful, and lightly humorous.
```
