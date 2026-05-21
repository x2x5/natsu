# Vite 常用命令和配置

## 常用命令

| 命令 | 作用 |
|------|------|
| `npm run dev` | 启动开发服务器（http://localhost:5173） |
| `npm run build` | 打包成生产版本（生成 dist 目录） |
| `npm run preview` | 本地预览生产版本 |
| `npm run lint` | 代码检查 |

## vite.config.js 说明

```js
import { defineConfig } from 'vite'
import react from '@vitejs/plugin-react'
import tailwindcss from '@tailwindcss/vite'

export default defineConfig({
  plugins: [react(), tailwindcss()],
})
```

- `plugins` — 启用的插件
- 一般不需要修改此文件

## 环境变量

- 以 `VITE_` 开头的变量才能在代码中使用
- 放在 `.env.local` 文件中（不会提交到Git）
- 代码中通过 `import.meta.env.VITE_XXX` 访问
