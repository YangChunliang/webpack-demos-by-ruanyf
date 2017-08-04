这篇文章整理了一下webpack的简单示例。
这些示例使用简单、清晰的风格书写。跟着下面的示例来学习这个强大的工具将会变得非常简单。
### 如何使用
首先，全局安装webpack和webpack-dev-server。
```
$ npm i -g webpack@1.x webpack-dev-server@1.x
```
然后，克隆仓库、安装依赖
```
# Linux & Mac
$ git clone git@github.com:ruanyf/webpack-demos.git

# Windows
$ git clone https://github.com/ruanyf/webpack-demos.git
:
$ cd webpack-demos
$ npm install
```
现在，运行一下demo目录下的源文件
```
$ cd demo01
$ webpack-dev-server
```
在浏览器里输入[http://127.0.0.1:8080]( http://127.0.0.1:8080)
### 前言：webpack是什么
webpack和Grunt与Gulp一样的前端构建工具。
它被用作和Browserify相似，功能强大的模块打包工具。
```
$ browserify main.js > bundle.js
# be equivalent to
$ webpack main.js bundle.js
```
它的配置文件是`webpack.js`
```
// webpack.config.js
module.exports = {
  entry: './main.js',
  output: {
    filename: 'bundle.js'
  }
};
```
创建好webpack.config.js之后，你就可以不带任何参数直接使用webpack
```
$ webpack
```
你应该知道的一些常用命令行选项
* `webpack`——
* `webpack -p`——
* `webpack -watch`——
* `webpack -d`——
* `webpack --colors`——
在开始程序之前，你应该在你的package.json中加入如下scripts域。
```
// package.json
{
  // ...
  "scripts": {
    "dev": "webpack-dev-server --devtool eval --progress --colors",
    "deploy": "NODE_ENV=production webpack -p"
  },
  // ...
}
```
### 目录
 1. [Entry file](Entry-file)
 2. [Multiple entry files](Multiple-entry-files)
 3. [Babel-loader](Babel-loader)
 4. [CSS-loader](CSS-loader)
 5. [Image loader](Image-loader)
 6. [CSS Module](CSS-Module)
 7. [UglifyJs Plugin](UglifyJs-Plugin)
 8. [HTML Webpack Plugin and Open Browser Webpack Plugin](HTML-Webpack-Plugin-and-Open-Browser-Webpack-Plugin)
 9. [Environment-flags](Environment-flags)
