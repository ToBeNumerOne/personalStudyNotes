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