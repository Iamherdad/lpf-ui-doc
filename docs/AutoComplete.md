# AutoComplete 组件

输入框自动完成功能。当输入值需要自动完成时使用，支持方向键选择

## 代码演示

```jsx
import { AutoComplete } from 'lpf-ui';
import React from 'react';
const APP = () => {
  const lakers = [
    'bradley',
    'pope',
    'caruso',
    'cook',
    'cousins',
    'james',
    'AD',
    'green',
    'howard',
    'kuzma',
    'McGee',
    'rando',
  ];
  const handleFetch = (query) => {
    return lakers.filter((name) => name.includes(query));
  };
  return <AutoComplete fetchSuggestions={handleFetch} />;
};
export default APP;
```

## API

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| fetchSuggestions\* | 返回输入建议的方法，可以拿到当前的输入，然后返回数组 |  |  |
| onSelect | 点击选中建议项时触发的回调 |  |  |
| onChange | 文本框发生改变的时候触发的事件 |  |  |
| renderOption | 支持自定义渲染下拉项，返回 ReactElement | (item: DataSourceObject) => ReactElement |  |
