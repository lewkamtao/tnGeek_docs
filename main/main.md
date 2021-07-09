#### Javascript判断Video视频播放、暂停、结束完成及获取长度事件监听处理

> 最近公司项目业务需求对视频播放器的个性化定制要求有点苛刻，所以在找了很多第三方视频框架都不太好，太臃肿了。所以决定重写一个播放器，这样一来也收获了很多知识。



##### 先引入HTML视频标签

```html
<video id="video" controls="controls">
    <source type="video/mp4" src="mi.mp4">
</video>
```



##### 视频加载后获取视频的长度

```js
<script>
    var elevideo = document.getElementById("video");
    elevideo.addEventListener('loadedmetadata', function () { //加载数据
        //视频的总长度
        console.log(elevideo.duration);
    });
</script>
```



##### 视频开始播放

``` js
<script>
	var elevideo = document.getElementById("video");
    elevideo.addEventListener('playing', function () { //播放中
       console.log("播放中");
    });
</script> ```
```



##### 视频加载中：

```js
<script>
    var elevideo = document.getElementById("video");
    elevideo.addEventListener('waiting', function () { //加载
        console.log("加载中");
    });
</script>
```



##### 视频暂停播放：

```js
<script>
    var elevideo = document.getElementById("video");
    elevideo.addEventListener('pause', function () { //暂停开始执行的函数
        console.log("暂停播放");
    });
</script>
```



##### 视频播放结束：

```js
<script>
    var elevideo = document.getElementById("video");
    elevideo.addEventListener('ended', function () { //结束
        console.log("播放结束");
    }, false);
</script>
```



常用的一些 video API

**"视频播放":video.play();**

***\*"视频暂停播放":video.pause();\****

**"视频地址":video.currentSrc;**

**"视频总时长":video.duration;**

**"视频播放速率":video.playbackRate;**

**"是否暂停":video.paused;**

**"是否结束":video.ended;**

**"是否静音":video.muted;** 

**"当前播放时间": video.currentTime;**

**"当前缓冲量":video.buffered.end(0);**

**"当前音量":video.volume**



> 原文：https://www.jinliniuan.com/archives/1299.html

