# React 基础

## 1. 组件

组件就是一个函数，返回一段 JSX（长得像HTML）。

```jsx
function Welcome() {
  return <h1>你好，世界！</h1>
}

export default Welcome
```

## 2. State（状态）

State 是组件内部的变量，变了页面会自动更新。

```jsx
import { useState } from 'react'

function Counter() {
  const [count, setCount] = useState(0)
  
  return (
    <button onClick={() => setCount(count + 1)}>
      点击了 {count} 次
    </button>
  )
}
```

## 3. Props（属性）

Props 是父组件传给子组件的数据。

```jsx
// 子组件
function Greeting({ name }) {
  return <h1>你好，{name}！</h1>
}

// 父组件使用
<Greeting name="小明" />
```

## 4. JSX 规则
- 只能返回**一个**根元素（用 `<div>` 或 `<>` 包裹）
- 类名用 `className` 而不是 `class`
- 标签必须闭合，如 `<br />`
- JavaScript 表达式用 `{}` 包裹

## 5. 条件渲染

```jsx
function Login({ isLoggedIn }) {
  return isLoggedIn ? <button>退出</button> : <button>登录</button>
}
```

## 6. 列表渲染

```jsx
function List({ items }) {
  return (
    <ul>
      {items.map((item) => (
        <li key={item.id}>{item.name}</li>
      ))}
    </ul>
  )
}
```
