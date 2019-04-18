# push-huawei

> 华为推送Node服务

根据华为提供的推送服务实现的 Node 版SDK。支持华为通知栏推送功能，欢迎大家使用。

## 安装
```
npm install push-huawei --save-dev
```

## 实例
```javascript
const Huawei = require('push-huawei');
const huawei = new Huawei({
  client_id: 'appId',
  client_secret: 'appSecret',
  appPkgName: '应用包名'
});

huawei.push({
  title: '标题',
  content: '内容',
  list: ['pushId'],
  extras: {
    // ... 额外信息
  },
  success(res){}, // 成功回调
  error(err){} // 失败回调
});
```
## 参数

| key | value |
|:----|:----|
|client_id|appID|
|$client_secret|appSecret|
|appPkgName|应用包名|
|getTokenUrl|获取token URL 默认 https://login.cloud.huawei.com/oauth2/v2/token|
|pushUrl|推送URL 默认 https://api.push.hicloud.com/pushsend.do|
|grant_type|华为接口参数 默认 'grant_type'|
|nsp_svc|华为接口参数 默认 'openpush.message.api.send'|
|maxLength|华为推送限制长度 默认100|


[华为官方文档](https://developer.huawei.com/consumer/cn/service/hms/catalog/huaweipush_agent.html?page=hmssdk_huaweipush_api_reference_agent_s1)