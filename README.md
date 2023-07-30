> 项目地址：https://github.com/mute2000/draw-and-guess
## 下载&运行

```
npm install express ws //后端所需依赖项

npm install -g @vue/cli
vue create client
cd client               //前端所需依赖项

node server.js // 运行服务端

npm run serve  // 运行客户端程序

然后浏览器打开localhost:8080即可
```

## 技术栈

- 前端框架使用`vue`
- 后端框架使用`Express`,实时通信使用`ws`
- 数据库使用`Mysql`

## 基本

- 用WebSocket提供数据同步，内容分发功能。
- 用绘图位点坐标，每隔一段时间向服务器发送坐标，再通过`.send()`方法把坐标分发出去，在猜图中获取坐标，实现绘图数据的同步。
- 同步绘画数据后，输入框能够提交关键词，检测答案是否正确。

## 游戏逻辑

1.用户加入游戏房间。

1.游戏开始，随机选择一个玩家作为画画者，其他玩家为猜画者。

3.画画者收到一个随机的词语，开始画画。

4.猜画者根据画画者的画猜词语。

5.猜对的玩家得分，游戏继续。

6.游戏结束，显示得分排名。

## 前端设计
1.登录/注册界面：用户输入用户名和密码进行登录或注册。

2.游戏大厅：显示可加入的游戏房间列表，用户可以创建新房间或加入已有房间。

3.游戏房间：显示当前房间内的玩家列表、聊天窗口、画板。

4.画板：画画者在此绘制图像，猜画者可以看到实时的画面。

5.得分榜：显示游戏结束后的得分排名。

