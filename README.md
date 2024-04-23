
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
