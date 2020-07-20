# lty-lv2d-v3
使用方法：
https://www.cnblogs.com/x66ccff/p/luotianyi-live2d-v3-in-cnblogs.html

### 给你的博客园添加一只萌萌的洛天依吧！
如上一篇文章提到，本来打算用@unsignzhang 的方法和模型把洛天依添加到博客园
（博文链接：http://unsignedzhang.cn/luotianyi-live2d/ ）
但是因为live2d的v2版本模型（unsignedzhang的模型）在博客园上存在跨域引用的问题，所以导致模型无法显示在博客园里。
于是我寻找别的方法，在@麻辣猪仔 的文章里找到了解决方法：
（博文链接：https://www.cnblogs.com/wstong/p/12874732.html ）

首先，从 @麻辣猪仔 的博文这里，得到两个文件
1.bundle.js（https://cdn.jsdelivr.net/gh/wangstong/live2dm3/live2d/js/live2dcubismcore.js ）
2.live2dcubismcore.js （https://cdn.jsdelivr.net/gh/wangstong/live2dm3/live2d/js/bundle.js ）
（我也不知道具体是什么原理（因为之前完全不懂html,js,css这些，太菜了……）），这两个文件应该是对所有moc3（live2d-v3版本的）模型通用的配置文件
然后把以下代码放到你的博客园html框里，并上传上面两个文件到博客园后台就可以使用了！

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

关于洛天依模型的制作：
如果你访问上述cdn链接会发现，模型的名称是Hiyori（live2d的一个官方模型）而不是天依，这是因为模型的大部分文件（包括动作、表情）都是使用Hiyori的（来自@麻辣猪仔 的github），直接拿来主义了，如果要亲手做的话可能要很久；贴图来自 @unsignedzhang 的v2版本模型；而模型其他部分如各个参数的运动是我自己做的。

项目github链接：https://github.com/x66ccff/lty-lv2d-v3
本文作者：https://www.cnblogs.com/x66ccff/

ps:本人目前无论在github还是博客、前端这方面都是小白，有什么地方做的不好请多多指教，如果这个模型有什么可以改进的可以在github上（pull request???）