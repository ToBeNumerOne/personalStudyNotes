# 个人学习笔记

## Webpack

webpack的相对路径是相对当前目录，绝对路径是相对webpack.config.js的入口文件。

webpack中babel的配置：

1、

```javascript
{
    test: /\.jsx?$/,
    exclude: /node_modules/,
    loader: 'babel',
    query: {
    	presets:[
        	'es2015', 'react'
    	]
    }
}
```

2、

```javascript
{
    test: /\.jsx?$/,
    exclude: /node_modules/,
    loaders: ["react-hot", "babel?presets[]=react,presets[]=es2015"]
}
```

3、 react-router
嵌套路由的时候，被嵌套路由的组件相当于上层组件的子组件。在子组件中可以通过{this.props.children}来展示子组件。无论嵌套中的路由使用相对路径还是绝对路径。

如果去掉{this.props.children}则不显示子组件，但是依然会进行路由跳转，无论嵌套的路由使用的是相对路径还是绝对路径。
