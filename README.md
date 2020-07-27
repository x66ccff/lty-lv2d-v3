# 博客园live2d洛天依看板娘
## 给你的博客园添加一只萌萌的洛天依看板娘吧！
使用方法：
https://www.cnblogs.com/x66ccff/p/luotianyi-live2d-v3-in-cnblogs.html

## 文件说明
### bundle.js
### live2dcubismcore.js 
这两个是moc3(live2d-v3版本模型)的关键配置文件，在html中引入

### Hiyori文件夹
存放洛天依模型
（虽然命名是Hiyori(live2d的一个官方模型名称)，但是模型是天依，借用了Hiyori的动作和表情，为了防止可能的bug，就不改模型名称了）

### html部分关键代码
```
<!-- Live2DCubismCore script -->
<script src="https://blog-static.cnblogs.com/files/【这里写你的cnblogs域名】/live2dcubismcore.js"></script>
<!-- Build script -->
<script src="https://blog-static.cnblogs.com/files/【这里写你的cnblogs域名】/bundle.js"></script>
<canvas id="live2d" width="500" height="500" class="live2d" style="position: fixed; opacity: 1; left: -110px; bottom: -125px; z-index: 99999; pointer-events: none;"></canvas>

<script type="text/javascript">
  var resourcesPath = 'https://cdn.jsdelivr.net/gh/x66ccff/lty-lv2d-v3@v1.2/'; // 指定资源文件（模型）保存的路径
  var backImageName = ''; // 指定背景图片
  var modelDir = ['Hiyori']; // 指定需要加载的模型
  initDefine(resourcesPath, backImageName, modelDir); // 初始化模型
</script>
```

## 关于洛天依模型的制作：
模型的名称是Hiyori（live2d的一个官方模型）而不是天依，这是因为模型的大部分文件（包括动作、表情）都是使用Hiyori的（来自@麻辣猪仔 的github），直接拿来主义了，如果要亲手做的话可能要很久；贴图来自 @unsignedzhang 的v2版本模型；而模型其他部分如各个参数的运动是我自己做的。

## 效果展示：
可以到我的博客看天依！
https://www.cnblogs.com/x66ccff/p/luotianyi-live2d-v3-in-cnblogs.html

## 致谢
(@unsignedzhang)[http://unsignedzhang.cn/luotianyi-live2d/]
(@麻辣猪仔)[https://www.cnblogs.com/wstong/p/12874732.html]
(@weixin_44128558)[https://blog.csdn.net/weixin_44128558/article/details/104792345]


ps:本人目前无论在github还是博客、前端这方面都是小白，有什么地方做的不好请多多指教，如果这个模型有什么可以改进的欢迎在github上pull request（???）
