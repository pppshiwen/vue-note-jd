

## 安装

已安装MySQL数据库，然后导入migou.sql文件

然后通过`npm`安装本地服务第三方依赖模块(需要已安装[Node.js](https://nodejs.org/))

```
cd vue-jd
```

```
npm install 或 cnpm install(个人比较喜欢使用后者，下载依赖模块速度较快)
```

```
npm run dev
```

最后开启后台服务

```
node server.js
```

## 目录结构
<pre>
.
├── README.md           
├── libs               		// 后台常用工具模块的封装，比如格式化事件、MD5加密等
├── route              		// 后台接口的编写目录
├── server.js          		// 后台服务的配置文件
├── webpack.config.js  		// webpack配置文件
├── index.html         		// 项目入口文件
├── package.json       		// 项目配置文件
├── src                		// 生产目录
│   ├── assets         		// css js 和图片资源
│   ├── components     		// 各种Vue组件
│   ├── store          		// vuex状态管理器
│   ├── App.vue        		// 项目中全局Vue
│   ├── main.js        		// Webpack 预编译入口
│   └── router.config.js    // vue路由配置文件
</pre>

##截图
<p align="center">
    <img src="https://raw.githubusercontent.com/pppshiwen/img/master/%E6%88%AA%E5%9B%BE%202018-11-08%2020.03.05.png" alt="Sample"  width="250">
    <p align="center">
        <em>注册</em>
    </p>
</p>
<p align="center">
    <img src="https://raw.githubusercontent.com/pppshiwen/img/master/%E6%88%AA%E5%9B%BE%202018-11-08%2020.02.59.png" alt="Sample"  width="250">
    <p align="center">
        <em>登录</em>
    </p>
</p>

<p align="center">
    <img src="https://raw.githubusercontent.com/pppshiwen/img/master/%E6%88%AA%E5%9B%BE%202018-10-26%2016.29.15.png" alt="Sample"  width="250">
    <p align="center">
        <em>个人中心</em>
    </p>
</p>
<p align="center">
    <img src="https://raw.githubusercontent.com/pppshiwen/img/master/%E6%88%AA%E5%9B%BE%202018-11-08%2020.02.02.png" alt="Sample"  width="250">
    <p align="center">
        <em>笔记页面</em>
    </p>
</p>
<p align="center">
    <img src="https://raw.githubusercontent.com/pppshiwen/img/master/%E6%88%AA%E5%9B%BE%202018-11-08%2020.02.23.png" alt="Sample"  width="250">
    <p align="center">
        <em>笔记详情</em>
    </p>
</p>
<p align="center">
    <img src="https://raw.githubusercontent.com/pppshiwen/img/master/%E6%88%AA%E5%9B%BE%202018-11-08%2020.02.35.png" alt="Sample"  width="250">
    <p align="center">
        <em>发布笔记</em>
    </p>
</p>
<p align="center">
    <img src="https://raw.githubusercontent.com/pppshiwen/img/master/%E6%88%AA%E5%9B%BE%202018-11-08%2020.02.48.png" alt="Sample"  width="250">
    <p align="center">
        <em>商城</em>
    </p>
</p>
<p align="center">
    <img src="https://raw.githubusercontent.com/pppshiwen/img/master/%E6%88%AA%E5%9B%BE%202018-11-08%2020.02.54.png" alt="Sample"  width="250">
    <p align="center">
        <em>购物车</em>
    </p>
</p>
<p align="center">
    <img src="https://raw.githubusercontent.com/pppshiwen/img/master/%E6%88%AA%E5%9B%BE%202018-11-08%2020.02.48.png" alt="Sample"  width="250">
    <p align="center">
        <em>商城</em>
    </p>
</p>

      

