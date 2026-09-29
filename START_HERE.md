# Start Here / 从这里开始

## 5-minute no-code setup / 5 分钟零代码配置

You do **not** need:
- Codex CLI
- Skill installation
- Plugin installation
- Node.js
- Python
- API key

你**不需要**：
- Codex CLI
- 安装 Skill
- 安装 Plugin
- Node.js
- Python
- API Key

---

## 1. Create a new ChatGPT Project / 新建 ChatGPT Project

Create a fresh Project named:

新建一个 Project，名字可以叫：

**Dark Collage Editor — Beta**

Use a fresh Project so you can test the experience like a completely new user.

建议新建一个全新的 Project，这样可以模拟陌生用户第一次使用时的真实体验。

---

## 2. Add Project Instructions / 添加 Project Instructions

Open **PROJECT_INSTRUCTIONS.md**.

打开 **PROJECT_INSTRUCTIONS.md**。

Copy the complete contents into your Project's instruction field.

把全文复制到 ChatGPT Project 的 Instructions 中。

For the first test, do not shorten or rewrite it.

第一次测试建议不要删减，先直接使用完整版本。

---

## 3. Upload the Style Guide / 上传 Style Guide

Upload **STYLE_GUIDE.md** into the Project.

把 **STYLE_GUIDE.md** 上传到 Project 文件中。

This gives the Project a separate visual reference document.

这样模型除了 Instructions 之外，还能单独参考一份视觉规范。

---

## 4. Optional: add 3–6 reference images / 可选：加入 3–6 张参考效果图

You can test without reference images first.

建议第一轮先不上传参考图，先看纯 Instructions + Style Guide 能不能跑通。

For a stronger style lock, add 3–6 examples later:
- one Clean
- two Editorial
- one horizontal image
- one text example
- one no-text example

如果基础测试通过，再加入 3–6 张风格参考图，例如：
- 1 张 Clean
- 2 张 Editorial
- 1 张横图
- 1 张有文字
- 1 张无文字

Do not upload private CR2 originals to a public GitHub repository.

不要把私人 CR2 原图上传到公开 GitHub 仓库。

---

## 5. First test / 第一次测试

Start a new chat inside the Project.

在这个 Project 中新建聊天。

Upload one portrait and send:

上传一张照片，然后发送：

> Editorial. No text. Preserve my face, pose, clothes and original orientation.

或者中文：

> Editorial。不要文字。保留我的脸、动作、衣服和原始横竖构图。

Then compare the result with Test 01 in **TEST_CASES.md**.

然后按照 **TEST_CASES.md** 的 Test 01 检查结果。

---

## 6. Exact text test / 精确文字测试

Use another image and send:

换一张照片，发送：

> Editorial. Text: STAY IN THE NOISE. Use it once. Do not cover my face.

或者：

> Editorial。文字写：STAY IN THE NOISE。只出现一次，不要挡脸。

---

## 7. Batch test / 批量测试

Upload 4–9 photos and send:

上传 4–9 张照片，然后发送：

> Make these one consistent dark collage series. Editorial. No text. Keep the same palette and texture family, but make every layout different. Do not create chaos by repeating my face.

或者：

> 把这些照片做成同一个暗黑拼贴系列。Editorial，不要文字。统一配色和材质，但每张构图都不同。不要通过重复粘贴我的脸来制造混乱感。

---

## What counts as success? / 什么算测试通过？

A good first result should satisfy most of these:

第一次结果最好满足：

- same person / 人物还是本人
- same pose / 动作基本保持
- clothes and accessories preserved / 衣服和首饰没有乱改
- horizontal stays horizontal / 横图不被强行改成竖图
- vertical stays vertical / 竖图不被强行改成横图
- one dominant portrait / 主体人物仍然占主导
- no wall of repeated faces / 没有大量重复贴脸
- no invented readable text when "No text" is requested / “不要文字”时不出现乱写的英文
- exact custom text / 自定义文字拼写正确
- batch looks consistent but not copy-pasted / 批量照片统一但不套同一个模板

---

## If something fails / 如果测试失败

Do not rewrite everything immediately.

不要一失败就重写整个 Instructions。

Record the failure category:

记录失败类型，例如：
- identity drift / 脸变了
- pose drift / 动作变了
- orientation changed / 横竖方向变了
- too many portrait fragments / 人像碎片太多
- invented text / 乱加文字
- text misspelled / 文字拼错
- too cluttered / 太乱
- batch layouts too repetitive / 批量构图过于重复

Then change only the relevant rule and re-run the same test.

然后只改对应规则，再用同一张图和同一测试语句重新测试。
