# Menu

为网站提供导航功能的菜单。支持横向纵向两种模式，支持下拉菜单。

## 代码演示

```jsx
import { Menu } from 'lpf-ui';
import React from 'react';
const APP = () => {
  return (
    <Menu>
      <Menu.Item>one</Menu.Item>
      <Menu.Item>two</Menu.Item>
      <Menu.Item>three</Menu.Item>
    </Menu>
  );
};
export default APP;
```

## 默认 Menu

```jsx
import { Menu } from 'lpf-ui';
import React from 'react';
const APP = () => {
  return (
    <Menu>
      <Menu.Item>1</Menu.Item>
      <Menu.Item>2</Menu.Item>
      <Menu.Item>3</Menu.Item>
    </Menu>
  );
};
export default APP;
```

## 禁用的 Menu

```jsx
import { Menu } from 'lpf-ui';
import React from 'react';
const APP = () => {
  return (
    <Menu>
      <Menu.Item>1</Menu.Item>
      <Menu.Item>2</Menu.Item>
      <Menu.Item disabled>disabled</Menu.Item>
    </Menu>
  );
};
export default APP;
```

## SubMenu

```jsx
import { Menu } from 'lpf-ui';
import React from 'react';
const APP = () => {
  return (
    <Menu>
      <Menu.Item>1</Menu.Item>
      <Menu.Item>2</Menu.Item>
      <Menu.SubMenu title="下拉选项">
        <Menu.Item>option1</Menu.Item>
        <Menu.Item>option2</Menu.Item>
      </Menu.SubMenu>
    </Menu>
  );
};
export default APP;
```

## 纵向 Menu

```jsx
import { Menu } from 'lpf-ui';
import React from 'react';
const APP = () => {
  return (
    <Menu mode="vertical">
      <Menu.Item>1</Menu.Item>
      <Menu.Item>2</Menu.Item>
      <Menu.SubMenu title="下拉选项">
        <Menu.Item>option1</Menu.Item>
        <Menu.Item>option2</Menu.Item>
      </Menu.SubMenu>
    </Menu>
  );
};
export default APP;
```

## 默认展开的纵向 Menu

```jsx
import { Menu } from 'lpf-ui';
import React from 'react';
const APP = () => {
  return (
    <Menu mode="vertical" defaultOpenSubMenu={['2']}>
      <Menu.Item>1</Menu.Item>
      <Menu.Item>2</Menu.Item>
      <Menu.SubMenu title="下拉选项">
        <Menu.Item>option1</Menu.Item>
        <Menu.Item>option2</Menu.Item>
      </Menu.SubMenu>
    </Menu>
  );
};
export default APP;
```

## API

### Menu

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| defaultIndex | 默认 active 的菜单项的索引值 | string | "0" |
| className | 类名 | string |  |
| mode | 菜单类型 横向或者纵向 | "horizontal","vertical" | "horizontal" |
| style |  | CSSProperties |  |
| onSelect | 点击菜单项触发的回掉函数 | ((selectedIndex: string) => void) |  |
| defaultOpenSubMenus | 设置子菜单的默认打开 只在纵向模式下生效 | string[] | [] |

### MenuItem

| 属性      | 说明           | 类型    | 默认值 |
| --------- | -------------- | ------- | ------ |
| index     |                | string  |        |
| disabled  | 选项是否被禁用 | boolean | false  |
| className | 类名           | string  |        |
| style     | 自定义样式     |         |        |

### SubMenu

| 属性      | 说明               | 类型   | 默认值 |
| --------- | ------------------ | ------ | ------ |
| title\*   | 下拉菜单选项的文字 | string |        |
| className | 类名               | string |        |
| style     | 自定义样式         |        |        |
