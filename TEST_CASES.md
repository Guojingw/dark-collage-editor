# Dark Collage Editor — Smoke Tests  
# 暗黑拼贴编辑器 — 基础测试

Use these tests in a fresh ChatGPT Project.  
建议在全新的 ChatGPT Project 中运行这些测试。

---

## Test 01 — Single image, no text / 单张，无文字

### User message / 用户输入

> Editorial. No text. Preserve my face, pose, clothes and original orientation.

中文：

> Editorial。不要文字。保留我的脸、动作、衣服和原始横竖构图。

### Pass / 通过标准

- identity preserved / 人还是本人
- pose preserved / 动作保留
- clothes and accessories preserved / 衣服和饰品不乱改
- orientation preserved / 横竖方向保留
- one dominant portrait / 一个明确主体
- no invented readable text / 不出现随机可读文字
- no more than 2 portrait fragments / 不超过 2 个人像碎片
- visual complexity mainly from non-portrait elements / 复杂度主要来自非人物元素

---

## Test 02 — Exact custom text / 精确文字

### User message / 用户输入

> Editorial. Text: STAY IN THE NOISE. Use it once. Do not cover my face.

中文：

> Editorial。文字写：STAY IN THE NOISE。只出现一次，不要挡脸。

### Pass / 通过标准

- exact spelling / 拼写完全正确
- appears once as main readable phrase / 主文字只出现一次
- does not cover key facial features / 不挡关键五官
- identity and pose remain stable / 人物和动作保持

---

## Test 03 — Batch series / 批量系列

### User message / 用户输入

> Make these one consistent dark collage series. Editorial. No text. Keep the same palette and texture family, but make every layout different. Do not create chaos by repeating my face.

中文：

> 把这些照片做成同一个暗黑拼贴系列。Editorial，不要文字。统一配色和纹理，但每张构图都不同。不要通过重复贴我的脸来制造混乱感。

### Pass / 通过标准

- same palette family / 配色统一
- same grain / paper language / 颗粒和纸张语言统一
- different layouts / 每张版式不同
- repeated faces are not the main variation / 不靠重复人脸制造变化
- orientation preserved per image / 每张原始横竖方向保留
- no invented readable text / 不乱加文字
- feels like one editorial series / 看起来像同一个系列

---

## Test 04 — Chaotic without face spam / Chaotic 但不狂贴脸

### User message / 用户输入

> Chaotic. No text. Make it aggressive with torn paper, red paint, scratches and graffiti. Do not add extra repeated faces.

中文：

> Chaotic。不要文字。加强撕纸、红色油漆、划痕和涂鸦，但不要重复添加很多我的脸。

### Pass / 通过标准

- denser than Editorial / 比 Editorial 更密集
- no wall of faces / 没有大量贴脸
- main subject remains clear / 主体清晰
- chaos mainly from graphics and texture / 混乱主要来自图形和纹理

---

## Test 05 — Minimal request / 极简输入

### User message / 用户输入

> Make this dark collage style.

中文：

> 把这张修成暗黑拼贴风。

### Expected / 预期

Use defaults:
默认：
- Editorial
- No text / 不加文字
- preserve identity / 严格保留人物

or ask only the minimum questions defined in PROJECT_INSTRUCTIONS.md.  
或者只问 PROJECT_INSTRUCTIONS.md 中定义的最少问题。

Do not ask for technical settings.  
不要要求用户填写技术参数。

---

## Failure log / 失败记录

```text
Test / 测试：
Source / 输入图片：
Failure category / 失败类型：
- identity drift / 脸变了
- pose drift / 动作变了
- orientation changed / 横竖方向改变
- too many portrait fragments / 人像碎片太多
- invented text / 乱加文字
- text misspelled / 文字拼错
- too cluttered / 太乱
- batch layouts too repetitive / 批量构图太重复
- style too weak / 风格太弱
- other / 其他

Observed / 实际：
Expected / 预期：
Next rule to adjust / 下一步只调整哪条规则：
```

Use the same source and same prompt when comparing instruction revisions.  
比较不同版本 Instructions 时，尽量使用同一张图和同一条测试语句。
