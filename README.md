# DocStudio

DocStudio 是一个基于 Docusaurus 的内容开发解决方案，提供：

- 📚 **文档系统** - 技术文档、API参考、用户手册
- ✍️ **博客平台** - 技术博客、公司动态、知识分享
- 🏢 **企业官网** - 产品展示、团队介绍、营销页面

开箱即用的预设配置，模块化插件系统，主题定制能力。

## 架构方案：主 Monorepo + 插件生态

```bash
📦 仓库结构建议：
├── **主仓库（monorepo）** - geekat/docstudio
│   ├── packages/
│   │   ├── core/                    # 核心引擎（必需）
│   │   ├── presets/                 # 官方预设（必需）
│   │   │   ├── blog/
│   │   │   ├── docs/
│   │   │   └── website/
│   │   └── starters/               # 启动模板（必需）
│   ├── examples/                   # 示例项目（文档用）
│   └── plugins/                    # **官方维护的核心插件**
│       ├── contact-form/
│       ├── analytics/
│       └── ...
│
├── **独立仓库** - 仅用于大型/独立组件
│   ├── geekat/docstudio-cli        # CLI工具（可选独立）
│   ├── geekat/docstudio-themes     # 主题包（可选独立）
│   └── geekat/docstudio-ui         # UI组件库（可选独立）
│
└── **社区插件** - 各自独立仓库
    ├── community/docstudio-plugin-x
    ├── community/docstudio-theme-y
    └── ...
```

