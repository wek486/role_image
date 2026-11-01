---
name: draw_role_form_mingchao_acg
description: Generate Wuthering Waves (鸣潮) character design sheets from reference illustrations in the user's approved semi-realistic ACG/CG style. Use for reference-image requests such as “这个也生成”, character style conversion, or matching this established series, with a portrait plus front/side/back full-body layout.
---

# 鸣潮角色半写实 CG 设定图

用户已确认本技能的画风与排版满意。收到角色参考图和“生成”“这个也生成”等简短指令时，直接沿用本流程生成图片，无须再次询问风格、排版、性别或是否开始。名称按用户指定保留为 `draw_role_form_mingchao_acg`，包括下划线与 `form` 拼写。

## 固定视觉参照

- 女性画风与排版锚点：[assets/approved-female.png](assets/approved-female.png)，来自本次用户明确满意的爱弥斯版本。
- 男性画风与排版锚点：[assets/series-male.png](assets/series-male.png)，来自同系列男漂泊者版本。
- 根据新角色选择适合的一个锚点。生成时同时输入新角色参考与锚点图片；不能仅用文字代替可用的视觉锚点。
- 输入 1 决定人物身份、外貌与服装；输入 2 只决定渲染、光照与排版。禁止把锚点角色的发色、脸、服装、性别特征或装饰混进新角色。
- 用户最新提供的新画风、姿势或布局要求优先于这里的默认值。

## 画风要求

半写实、适度动漫化的精细幻想 CG 角色。真实面部结构结合美化五官，细腻鼻唇、柔和眼窝与面颊体积，眼睛适度风格化而不夸张。脸部精度对齐锚点；男性保留男性骨相、肩颈与体态，女性保留参考人物自身特征，避免所有人物套同一张脸。

皮肤采用细腻柔和明暗与自然血色，光泽克制。头发有清晰发束、细发丝、碎发及真实体积。区分棉布、缎面、薄纱、皮革、金属、宝石、绒毛等材质；金属有集中反射，衣料有厚度、接缝和褶皱。整体精致清晰，避免平涂赛璐璐、厚油画笔触、塑料皮肤、全身同样油亮和过度光晕。

使用柔和中性棚拍光、无缝中灰背景、脚底接触阴影。保留角色原有主配色与点缀色，不把所有角色改成灰色或锚点角色的粉色。参考中的雨夜蓝光、逆光染色等应与人物本色区分；除非用户要求，不复制原背景的强烈色偏。

## 默认画面

横向展示板：左侧大幅头肩特写；右侧正面、严格侧面、背面三张完整全身图。全身图等高、脚底对齐，站姿自然，手臂略离躯干，手指放松。保持各方向脸型、发型、身材、饰件和服装结构一致。全身人物头饰与鞋履完整入画。

长发、狐尾、披风和长飘带适度让开，以便看见背面衣服结构，仍保留角色特征。服装与角色辨识度优先于添加华丽装饰。参考有佩刀等身份道具时可保留在腰侧或入鞘，默认不做攻击动作。餐盘、饮料、蛋糕、泡泡等情境道具通常省略，手势恢复自然站姿。去掉手机界面、水印、签名、原画文字、背景人物、风景和遮挡衣服的魔法光效。

## 角色还原与未展示部分

先看参考图，提炼头发/眼睛颜色、发型、头饰、身体特征、服装剪裁、叠层、配饰位置、材质及鞋履。区分真实兽耳/尾巴与发箍装饰，数量不随意增加。

若原图只到半身或背面不可见，按已有剪裁与配色谨慎补全，并在简短说明中指出补全范围。不能把补全当作角色官方设定；无需为了补全去搜索角色百科。用户另给全身、鞋履或背面图时以新图为准。避免多加无依据的武器、纹身、首饰或繁复花纹。

## 执行与交付

1. 简短中文说明即将生成及需补全的部分，然后直接生成。不要再次完整分析画风或让用户复制提示词到别处。
2. 使用可用的内置 `image_gen` 工具；涉及工具通用操作时遵循可用的 `imagegen` 技能。无须 API key；内置工具不可用时如实说明，不能擅自转付费 API 或写脚本冒充出图。
3. 使用新角色与所选锚点的实际图片作为输入，显式说明每张图的角色。本地图片按工具要求先查看；没有可用本地路径时使用能涵盖全部目标图的最小近期图片数量，避免把无关的上一个角色当作本次目标。全程只选一种图片引用机制。
4. 先生成一版。检查人物身份、画风、服装主结构、三视图、完整入画与明显错误。只有严重遗漏、错角色或明显生成缺陷才定向修正；没有用户要求不批量试图、不为追求额外变体反复生成。
5. 工具等待按实际可用参数进行，及时告知生成仍在进行，不反复叙述无变化状态。
6. 默认将最终图片只复制一次到参考图所在角色目录，文件名 `半写实角色设定-v1.png`；若已存在则使用下一个未占用版本号，不覆盖。保留工具输出原件。若用户指定预览即可，不复制。
7. **用户明确嫌弃生成后多余文件编辑：默认不另存提示词、不写说明/日志、不做格式转换和无关项目编辑。** 用户明确要求提示词时再提供。首次创建本技能的参考图片复制属于技能安装，后续每次生成不重复复制锚点文件。
8. 工具已内联显示图片时不再重复显示。最终只用简短中文说明结果，给保存图片的绝对路径链接，必要时一句注明补全部分；不主动附上大段提示词。
9. 用户在上一张生成过程中追加角色时，保留两张任务：收取并保存上一张，然后生成新角色；不可丢失仍在运行的任务或漏存已完成图片。

## 提示词骨架（内部使用，不自动保存成文件）

按每张图的实际可见细节填充，勿把占位符原样发给工具：

```text
Use case: stylized-concept.
Create a polished wide landscape semi-realistic fantasy CG character design sheet.
Input 1 is the SOLE character identity and costume reference.
Input 2 is ONLY rendering style, materials, soft studio lighting and layout reference; do not copy its identity or outfit.
Subject: [actual face, hair, eyes, expression, build and distinctive anatomy from input 1].
Preserve costume: [specific visible garment construction, layers, colors, ornaments, footwear and their placement].
Conservatively infer: [only obscured or missing details that must be completed].
Style: refined semi-realistic stylized facial anatomy, fine hair strands, soft natural skin shading, distinct fabric/leather/metal/fur materials, precise seams and restrained highlights, matching input 2.
Composition: large head-and-shoulders portrait left; complete front, strict side and rear full-body views right, same character and costume in all views, equal height and aligned feet, neutral standing poses, relaxed hands and arms slightly apart. Show back costume details around long hair or cape. Entire full-body heads and footwear inside canvas.
Lighting/background: soft neutral studio lighting, seamless gray background, subtle floor contact shadows.
Palette: preserve input 1's actual character colors.
Avoid: unrelated reference character features, outfit redesign, source scene/UI/text/watermark, excessive glow, plastic skin and flat anime cel shading.
```
