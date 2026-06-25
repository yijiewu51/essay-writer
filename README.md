# 留学文书生成器

解决两个核心问题：Turnitin AI 检测 + 人眼识别。

## 功能

- **文书类型**：SOP、Personal Statement、Common App Essay、推荐信
- **三阶段流水线**
  1. 生成初稿（内置禁词、句式规则，从源头减少 AI 特征）
  2. 去AI优化（识别并修复 30+ 种 AI 写作模式，二次自审）
  3. Turnitin 优化（EN → 中文 → 法语 → EN 翻译链，打散统计指纹）
- **流式输出**，实时看到生成过程
- **API Key 本地存储**，不经过任何服务器

## 部署（GitHub Pages）

```bash
cd essay-writer
git init
git add index.html README.md
git commit -m "init"
gh repo create essay-writer --public --source=. --push
```

然后在 GitHub 仓库页面：Settings → Pages → Branch: main → Save

几分钟后访问：`https://<你的用户名>.github.io/essay-writer/`

## 使用

1. 点右上角「API Key 设置」，输入 Anthropic API Key 并保存
2. 选择文书类型，填写信息（核心故事 / 具体事例是最关键的部分）
3. 点「开始生成」，等待三个阶段完成
4. 复制「Turnitin优化」标签页的最终结果
