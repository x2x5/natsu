# 文件结构

```
natsu/
├── src/                    # 源代码（最重要）
│   ├── main.jsx            # 入口：把React应用挂载到HTML
│   ├── App.jsx             # 主组件：页面内容在这里写
│   ├── App.css             # App样式（用Tailwind后可删）
│   ├── index.css           # 全局样式（已引入Tailwind）
│   └── assets/             # 图片等静态资源
│
├── public/                 # 公共资源（不经过构建处理）
│   ├── favicon.svg         # 浏览器标签图标
│   └── icons.svg           # 图标文件
│
├── index.html              # 唯一HTML文件，React挂载到 <div id="root">
├── package.json            # 项目配置：依赖包、运行命令
├── vite.config.js          # Vite配置：启用React和Tailwind插件
├── vercel.json             # Vercel部署配置（SPA路由重写）
├── .gitignore              # Git忽略文件
├── docs/                   # 本目录：AI记忆文档
└── dist/                   # 构建输出（自动生成，不用管）
```

## 核心文件说明

| 文件 | 作用 | 什么时候改 |
|------|------|------------|
| `src/App.jsx` | 页面内容 | 改页面布局、加新功能 |
| `src/index.css` | 全局样式 | 改全局颜色、字体 |
| `package.json` | 项目配置 | 安装新依赖时自动更新 |
| `vite.config.js` | 构建配置 | 一般不用改 |
