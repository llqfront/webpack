# webpack-sass-sprite
webpack sass less 编译  如何使用背景图合并 sprite 使用jdf 配合使用
用 npm 安装 Webpack：（需要安装node与jdf所使用相同）
安装命令：npm install webpack -g

# 查看 webpack 版本信息
$ npm info webpack

# 进入项目目录
# 确定已经有 package.json，没有就通过 npm init 创建
# 安装 webpack 依赖
$ npm install webpack --save-dev

# 安装指定版本的 webpack
$ npm install webpack@1.12.x --save-dev


*如果需要使用 Webpack 开发工具，要单独安装：

$ npm install webpack-dev-server -g


打包：
webpack
启服务：
webpack-dev-server

如果做pc端需要背景图合并：
cd dev 
使用jdf 启服务
[jdf](https://github.com/putaoshu/jdf)

页面中引入 jdf 中的链接  比如：
http://localhost:8082/css/index.css

同时把dev/js/entry.js中的css引入注掉

如果不需要jdf 
样式引入 
<link rel="stylesheet" href="./bundle/css/index.css">
同时把dev/js/entry.js中的css引入放开


另起配置文件
package.json
"start_es6": "webpack --config webpack.es6.config.js",
"build_es6": "webpack-dev-server --hot --inline --config webpack.es6.config.js"

npm start start_es6
npm start build_es6
启另一个配置文件
webpack-dev-server --config webpack.es6.config.js
webpack --config webpack.es6.config.js
