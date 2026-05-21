# 常见Bug排查

## 1. 页面空白
- 按 F12 打开浏览器控制台，看红色报错
- 检查 `src/App.jsx` 有没有语法错误
- 确认所有标签都正确闭合
- 确认 `return` 后面只有一个根元素

## 2. 样式不生效
- 检查 Tailwind 类名有没有拼错
- 确认 `src/index.css` 里有 `@import "tailwindcss"`
- 重启开发服务器：`Ctrl+C` 然后 `npm run dev`

## 3. 组件不更新
- 确认文件已保存
- 检查控制台有没有报错
- 硬刷新：`Cmd+Shift+R` (Mac) 或 `Ctrl+Shift+R` (Windows)

## 4. 安装依赖后报错
- 删除 `node_modules` 和 `package-lock.json`
- 重新运行 `npm install`

## 5. 部署后页面404
- 检查 `vercel.json` 有没有配置重写规则
- 确认构建输出目录是 `dist`

## 6. 端口被占用
```bash
npm run dev -- --port 3000
```

## 排查步骤总结
1. 看控制台报错（最重要）
2. 检查最近改了什么文件
3. 告诉AI具体的报错信息
4. 重启开发服务器试试
