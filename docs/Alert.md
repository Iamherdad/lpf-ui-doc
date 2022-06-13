# Alert 警告提示框

## 代码演示

```jsx
import { Alert } from 'lpf-ui';
import React from 'react';

const App = () => <Alert message="Success Text" type="success" />;

export default App;
```

## 四种样式

```jsx
import { Alert } from 'lpf-ui';
import React from 'react';

const App = () => (
  <>
    <Alert message="Success Text" type="success" />
    <Alert message="Info Text" type="info" />
    <Alert message="Warning Text" type="warning" />
    <Alert message="Error Text" type="error" />
  </>
);

export default App;
```

## 含有辅助性文字介绍

```jsx
import { Alert } from 'lpf-ui';
import React from 'react';
const App = () => (
  <>
    <Alert
      message="Success Text"
      description="Success Description Success Description Success Description"
      type="success"
    />
    <Alert
      message="Info Text"
      description="Info Description Info Description Info Description Info Description"
      type="info"
    />
    <Alert
      message="Warning Text"
      description="Warning Description Warning Description Warning Description Warning Description"
      type="warning"
    />
    <Alert
      message="Error Text"
      description="Error Description Error Description Error Description Error Description"
      type="error"
    />
  </>
);

export default App;
```

## 可关闭的警告提示

```jsx
import { Alert } from 'lpf-ui';
import React from 'react';

const App = () => (
  <>
    <Alert message="error Text" type="error" />
    <Alert message="点击右上关闭 Text" type="success" closable />
    <Alert message="Success info" type="info" />
  </>
);

export default App;
```

## 关闭回调函数

```jsx
import { Alert } from 'lpf-ui';
import React from 'react';

const App = () => (
  <>
    <Alert message="error Text" type="error" />
    <Alert
      message="点击右上关闭并弹框 Text"
      type="success"
      closable
      onClose={() => alert('我是关闭的回调')}
    />
    <Alert message="Success info" type="info" />
  </>
);

export default App;
```

## API

| 属性        | 说明                           | 类型                          | 默认值 |
| ----------- | ------------------------------ | ----------------------------- | ------ |
| type        | 指定警告提示的样式，有四种选择 | success、info、warning、error | info   |
| description | 警告提示的辅助性文字介绍       | string                        |        |
| closable    | 是否可关闭                     | boolean                       | false  |
| onClose     | 关闭的回调                     | (e: MouseEvent) => void       |        |
