# webpack-noWebpack.config.js
webpack默认零配置：webpack新建生成，无配置文件打包分析

## 安装：
webpack可以本地安装以及全局安装【一般使用本地webpack，保证版本一致】
yarn init -y
yarn add webpack webpack-cli -D

## webpack可以进行0配置：(无配置文件)可以实现以下功能
### 打包工具 - 输出后的结果（js模块）：
  在项目根目录下创建src/index.js文件
  运行npx webpack，打包后会新生成的文件：dist目录，其中包含文件main.js
  执行npx webpack后：默认在node_modules下寻找bin/webpack.cmd进行判断：
  如果当前文件夹下有node.exe文件则执行node.exe，否则node执行webpack/bin文件夹下的webpack.js
  其中就需要依赖webpack-cli【webpack4中安装webpack需要安装webpack-cli】
npx webpack打包后会默认生成dist文件其中包含main.js

### 打包 - 支持js模块化
  对于符合commomjs以及es6模块化的代码，webpack打包后可以直接在浏览器运行：新建一个html文件，引入打包后dist下的main.js运行即可看到打包引入的结果
