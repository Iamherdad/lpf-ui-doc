# Button 按钮

## 代码演示

```jsx
import React from 'react';
import { Button } from 'lpf-ui';
import 'lpf-ui/dist/index.css';
const APP = () => (
  <>
    <Button btnType="primary">primary</Button>
  </>
);
export default APP;
```

## 不同类型的 Button

```jsx
import React from 'react';
import { Button } from 'lpf-ui';

const APP = () => (
  <>
    <Button btnType="primary">primary</Button>
    <Button btnType="danger">danger</Button>
    <Button btnType="link" href="www.baidu.com" target="_blank">
      link
    </Button>
    <Button btnType="text">text</Button>
    <Button btnType="dashed">dashed</Button>
    <Button btnType="primary" disable>
      primary
    </Button>
    <Button>default</Button>
  </>
);
export default APP;
```

## 不同尺寸的 Button

```jsx
import React, { useState } from 'react';
import { Button } from 'lpf-ui';
const APP = () => {
  const [size, setSize] = useState('large');
  return (
    <>
      <Button onClick={() => setSize('large')}>large</Button>
      <Button onClick={() => setSize('small')}>small</Button>
      <br />
      <br />
      <Button size={size} btnType="primary">
        primary
      </Button>
      <Button size={size} btnType="danger">
        danger
      </Button>
    </>
  );
};
export default APP;
```

## API

通过设置 Button 的属性来产生不同的按钮样式。按钮的属性说明如下：

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| btnType | 设置按钮类型 | primary，ghost，link，text，dashed，default，danger | default |
| onClick | 点击按钮时的回调 | (event) => void |  |
| target | 相当于 a 链接的 target 属性，href 存在时生效 | string |  |
| href | 点击跳转的地址，指定此属性 button 的行为和 a 链接一致 | string |  |
| size | 设置按钮大小 | large， small | large |
| disabled | 按钮失效状态 | boolean | false |
