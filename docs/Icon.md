# Icon 图标

Icon 组件基于 fortawesome 二次封装,安装 lpf-ui 时已自动安装相关依赖您无需再次安装支持 react-fontawesome 的所有属性 可以在这里查询 https://github.com/FortAwesome/react-fontawesome#basic

支持 fontawesome 所有 free-solid-icons，可以在这里查看所有图标 https://fontawesome.com/icons?d=gallery&s=solid&m=free

## 代码演示

```jsx
import React from 'react';
import { Icon } from 'lpf-ui';
const APP = () => (
  <>
    <Icon icon="search" />
  </>
);
export default APP;
```

## 多色图标

```jsx
import React from 'react';
import { Icon } from 'lpf-ui';
const APP = () => (
  <>
    <Icon icon="spinner" theme="danger" spin />
    <Icon icon="spinner" theme="dark" spin />
    <Icon icon="spinner" theme="info" spin />
    <Icon icon="spinner" theme="light" spin />
    <Icon icon="spinner" theme="primary" spin />
    <Icon icon="spinner" theme="secondary" spin />
    <Icon icon="spinner" theme="success" spin />
    <Icon icon="spinner" theme="warning" spin />
  </>
);
export default APP;
```

## API

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| theme | 支持框架主题 根据主题显示不同的颜色 | "success""danger" "warning" "info" "primary" "secondary" "light" "dark" |  |
