# Uoload 上传文件

## 代码演示

```jsx
import { Upload, Button } from 'lpf-ui';
import React from 'react';
const APP = () => {
  return (
    <>
      <Upload action="www.baidu.com" Children={<Button>点击上传</Button>}></Upload>
    </>
  );
};
export default APP;
```

## 上传限制

```jsx
import { Upload, Button } from 'lpf-ui';
import React from 'react';
const APP = () => {
  const checkFileSize = (file) => {
    if (Math.round(file.size / 1024) > 50) {
      alert('file too big');
      return false;
    }
    return true;
  };
  return (
    <>
      <Upload
        action="www.baidu.com"
        beforeUpload={checkFileSize}
        Children={<Button>不能传大于50kb</Button>}
      ></Upload>
    </>
  );
};
export default APP;
```

## 拖动上传

```jsx
import { Upload, Button } from 'lpf-ui';
import React from 'react';
const APP = () => {
  return (
    <>
      <Upload action="www.baidu.com" drag Children={'点击或拖动到此处上传'}></Upload>
    </>
  );
};
export default APP;
```

## API

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| action\* | 必选参数, 上传的地址 | string |  |
| defaultFileList | 上传的文件列表 | [] |  |
| beforeUpload | 上传文件之前的钩子，参数为上传的文件，若返回 false 则停止上传。 |  |  |
| onProgress | 文件上传时的钩子 | ((percentage: number, file: UploadFile) => void) |  |
| onSuccess | 文件上传成功时的钩子 | ((data: any, file: UploadFile) => void) |  |
| onError | 文件上传失败时的钩子 | ((err: any, file: UploadFile) => void) |  |
| onChange | 文件状态改变时的钩子，上传成功或者失败时都会被调用 | ((file: UploadFile) => void) |  |
| onRemove | 文件列表移除文件时的钩子 | ((file: UploadFile) => void) |  |
| headers | 设置上传的请求头部 | { [key: string]: any; } |  |
| name | 上传的文件字段名 | string | 'file' |
| data | 上传时附带的额外参数 | { [key: string]: any; } |  |
| withCredentials | 支持发送 cookie 凭证信息 | boolean |  |
| accept | 可选参数, 接受上传的文件类型 | string |  |
| multiple | 是否支持多选文件 | boolean | false |
| drag | 是否支持拖拽上传 | boolean | false |
