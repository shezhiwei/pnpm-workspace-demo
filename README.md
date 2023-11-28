一个简单的pnpm + workspace的demo工程

首先需要在根目录下建pnpm-workspace.yaml文件

在这里写入workspace的范围

然后在需要的项目中的package.json文件中添加需要共同使用的依赖,例如下面使用的就是project1,这里的project1的名字是根据package.json中的name属性

./project2/package.json  ./project3/package.json
```js
"dependencies": {
    "project1":"workspace:^1.0.0"
  },
```

现在你在project1中修改文件,就会实时以第三方包的形式导入project2和project3
