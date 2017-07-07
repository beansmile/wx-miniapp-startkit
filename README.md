# wx-miniapp-startkit
微信小程序的初始配置，开箱即用

## Getting Started
###  Installation

```
# 克隆仓库到指定的文件夹
$ git clone git@github.com:xifengzhu/wx-miniapp-startkit.git

$ cd wx-miniapp-startkit

$ yarn install
```

### Develop

* 在项目根目录运行 `NODE_ENV=development gulp dev`
* 如果想使用 `production`的 `config` 文件 `NODE_ENV=production`即可
* 打开微信Web开放者工具，将下载的项目添加的 `/dist` 目录导入进去，填写或选择相应信息
* 创建新页面运行 `gulp generate --page '${page-name}'`
* 支持sass语法，gulp自动检测 `src/pages` 目录下的 `scss` 文件，自动编译成 `wxss` 放在对应的 `/dist`目录下
* 启动构建脚本之后，只会针对修改的文件进行替换与`eslint`检查

### Structure

```
├── .eslintrc.json ------------- eslint rule
├── README.md ------------------ readme
├── dist ----------------------- 构建目录
├── gulpfile.js ---------------- gulp构建脚本
├── node_modules --------------- 第三方库
├── package.json
├── src ------------------------ 源码目录
│   ├── app.js
│   ├── app.json
│   ├── app.wxss
│   ├── configs ---------------- 配置目录(如：api host)
│   ├── images
│   ├── pages
│   └── utils
│       └── wechat.js  --------- 微信发起方法请求promise封装
│       └── request.js  -------- 微信内置方法请求promise封装
└── yarn.lock
```
