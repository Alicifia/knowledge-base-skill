# knowledge-base-skill

Copyright (c) 2026 Alicifia · MIT License

把任意本地文件夹变成可检索的知识库系统：文档导入、向量检索、SQLite 持久化、多文档关联、多知识库管理与跨库统一检索，完全离线、零第三方依赖。

## 功能

- 指定任意本地目录作为知识库，递归扫描
- 多知识库注册与跨库统一检索
- CJK 优化的 TF-IDF 向量检索（中文单字+二元组 / 英文按词）
- SQLite 持久化，索引自包含于知识库目录
- 多文档关联（[[wikilink]] + Markdown 链接 + 相似度推荐）
- 多格式支持：.md / .txt / .epub / .mobi / .azw3 / .azw，可选 .docx / .pdf
- 增量更新，按内容哈希识别变更
- 仅 Python 3.8+ 标准库，零网络请求

## 安装

把 `SKILL.md` 和 `scripts/kb.py` 放到你的 AI agent 技能目录下，保持目录结构：

```
skills/knowledge-base/
  ├── SKILL.md
  └── scripts/kb.py
```

## 使用

通过自然语言或直接调用 CLI：

```bash
python scripts/kb.py init --root /path/to/notes --name 我的笔记
python scripts/kb.py add /path/to/notes
python scripts/kb.py search "检索内容" --top 5
python scripts/kb.py libraries
python scripts/kb.py related "某篇文档"
```

## 版权

Copyright (c) 2026 Alicifia. Released under the MIT License.