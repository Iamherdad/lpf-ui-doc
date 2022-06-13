# Progress

进度条组件

## 代码演示

```jsx
import { Progress } from 'lpf-ui';
import React from 'react';
const APP = () => {
  return <Progress percent={30} />;
};
export default APP;
```

## API

| 属性         | 说明         | 类型                | 默认值 |
| ------------ | ------------ | ------------------- | ------ |
| percent      | 进度         | number              |        |
| strokeHeight | 进度条高度   | number              | 15     |
| showText     | 是否显示文字 | boolean             | false  |
| style        | 自定义样式   | React.CSSProperties |        |
