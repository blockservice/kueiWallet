# ecoinWallet
基于React-Native开发的离线HD钱包, 当前版本仅支持以太系.

![ecoinWallet](https://raw.githubusercontent.com/ChungkueiBlock/ecoinWallet/docs/docs/images/ewsdiagram.png)

### Description
ecoinWallet是一款离线钱包, 支持
+ 助记词导入
+ 私钥导入
+ keystore导入
+ 资产发送(eth/erc20)
+ Token列表查询
+ 交易历史查询

```
├── android
├── app.json
├── application
│   ├── actions
│   ├── components   //可复用的组件
│   ├── config.js    //配置文件
│   ├── core         //异步api;本地存储/api调用等
│   ├── index.js    
│   ├── models       
│   ├── reducers
│   ├── router.js    //路由
│   ├── screens      //对应每屏的视图
│   ├── stores
│   ├── theme        //主题css
│   └── utils        //工具函数
├── assets           //资源文件,图片等
├── global.js        //覆盖全局缺失的Buffer/process变量,详情参考node-libs-browser;初始化一些全局工具
├── index.js
├── ios
├── package.json
├── Readme.md
├── rn-cli.config.js //详情参考node-libs-browser
├── wallet_libs      //以太工具集,含离线签名,HD地址管理,公私钥转换,rpc调用等
│   ├── core
│   ├── ethereum
│   ├── fast-crypto
│   ├── mnemonic
│   ├── thirdparty
│   ├── timeused
│   └── utils
└── yarn.lock
```

### ecoinWallet基于React-Native开发
+ 简洁的UI设计
+ 安全,关键数据使用用户密码加密存储
+ 私密,用户数据仅存在于设备本地,不上传服务器
+ 分布式,设备直接与节点通信,并可自定义节点配置
+ 跨平台,android/IOS共用一套代码
+ 代码开源

### Requirements
ecoinWallet基于React-Native,开发套件的版本有严格要求
+ react-native: 0.55.4
+ react-native-cli: 2.0.1
+ android-sdk
详细版本请参考package.json文件

### Develop
```bash
git clone xxxxxxxxxxxxxxxxxxxxxxx
cd xxxxx
yarn install
react-native link
react-native run-android
```

如遇问题,可尝试:
```bash
rm -rf android ios
react-native eject
git reset --soft
react-native link
react-native run-android
```
