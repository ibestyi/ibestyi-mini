# ibestyi-mini

> author xu.xiangke

## 初始化ibestyi-mini

``` bash
# 1. 先检查下 Node.js 是否安装成功
$ node -v
v8.9.0

$ npm -v
5.6.0

# 2. 由于众所周知的原因，可以考虑切换源为 taobao 源
$ npm set registry https://registry.npm.taobao.org/

# 3. 全局安装 vue-cli
# 一般是要 sudo 权限的
$ npm install --global vue-cli@2.9

# 4. 创建一个基于 mpvue-quickstart 模板的新项目
# 新手一路回车选择默认就可以了
$ vue init mpvue/mpvue-quickstart ibestyi-mini

# 5. 安装依赖，走你
$ cd ibestyi-mini
$ npm install
$ npm run dev
```

## 搭建ibestyi-mini开发环境
``` bash
# 1.使用微信小程序开发者工具导入ibestyi-mini项目，点击“确定”按钮后会跳到正式的开发页面，点击“编辑器”按钮，关闭自带的小程序编辑器。然后如图

```
![微信小程序开发者工具](http://mpvue.com/assets/quick-start/2.png "微信小程序开发者工具")

