# npm_cnpm_yarn_tyarn
npm\cnpm\yarn\tyarn 关于源和代理的问题
npm 是一个包管理器。Node.js 自带。
cnpm 是 npm 的阿里版，用的阿里源。
yarn 是另一个包管理器，不自带，需要另外装。可以单独装，也可以用 npm 装。
tyarn 是 yarn 的阿里版，用的阿里源。

安装 yarn
$ npm install -g yarn

安装 cnpm
$ npm install -g cnpm --registry=https://registry.npm.taobao.org
npm 怎么用，cnpm就怎么用。
 
安装 tyarn
npm i yarn tyarn -g
yarn 怎么用，tyarn就怎么用。
 
npm 换淘宝源。
npm config set registry https://registry.npm.taobao.org
换回来。
npm config set registry https://registry.npmjs.org
看一下现在是什么源。
npm config get registry
 
 
yarn 同理。
yarn config set registry https://registry.npmjs.org
yarn config set registry https://registry.npm.taobao.org
yarn config get registry
 
npm 设置代理
npm config set proxy=http://127.0.0.1:8087
npm config set https-proxy=http://127.0.0.1:8087
npm 取消代理
npm config delete proxy
npm config delete https-proxy
 
yarn 设置代理
yarn config set proxy http://XXX
yarn config set https-proxy http://XXX
yarn 取消代理
yarn config delete proxy
yarn config delete https-proxy
 
还有一个指定目录换源的方法。
    新建一个.npmrc 到需要 yarn 的目录
registry=https://registry.npm.taobao.org
    内容如上。
对于个别很难下载的库，还可以通过设置 SASS_BINARY_SITE 解决。
参考：https://segmentfault.com/a/1190000005921721
 
综上所述，装依赖遇到困难时，至少有4种方法。
•	使用 cnpm / tyarn
•	更换淘宝源 / .npmrc 设置源
•	设置代理
•	设置 SASS_BINARY_SITE

