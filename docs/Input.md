# Input 输入框

通过鼠标或键盘输入内容，是最基础的表单域的包装。

## 代码演示

```jsx
import React from 'react';
import { Input } from 'lpf-ui';
const APP = () => (
  <>
    <Input placeholder="username" />
  </>
);
export default APP;
```

## 被禁用的 input

```jsx
import React from 'react';
import { Input } from 'lpf-ui';
const APP = () => (
  <>
    <Input disabled />
  </>
);
export default APP;
```

## 带图标的 input

```jsx
import React from 'react';
import { Input } from 'lpf-ui';
const APP = () => (
  <>
    <Input icon="search" />
  </>
);
export default APP;
```

## 带前后缀的 Input

```jsx
import React from 'react';
import { Input } from 'lpf-ui';
const APP = () => (
  <>
    <Input prepand="www." append=".com" />
  </>
);
export default APP;
```

## API

| 属性        | 说明                                       | 类型                      | 默认值 |
| ----------- | ------------------------------------------ | ------------------------- | ------ |
| placeholder | 提示内容                                   |                           |        |
| disabled    | 是否禁用 input                             | boolean                   | false  |
| icon        | 添加图标，在右侧悬浮添加一个图标，用于提示 | {}                        |        |
| prepend     | 添加前缀 用于配置一些固定组合              | string 或 ReactElement    |        |
| append      | 添加后缀 用于配置一些固定组合              | string 或 ReactElement    |        |
| onChange    |                                            | ((e: ChangeEvent => void) |        |
