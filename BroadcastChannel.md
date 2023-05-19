# BroadcastChannel

## BroadcastChannel

BroadcastChannel 接口代理了一个命名频道，可以让指定 origin 下的任意 browsing context 来订阅它。它允许同源的不同浏览器窗口，Tab 页，frame 或者 iframe 下的不同文档之间相互通信。通过触发一个 message 事件，消息可以广播到所有监听了该频道的 BroadcastChannel 对象

## 使用过程

```js
// 创建或加入频道
const channel = new BroadcastChannel('channel name');


// 发送消息
channel.postMessage(message: any)


// 监听消息
channel.addEventListener('message', ({data: any}) => {
    console.log(data);
})
// 或者
channel.onmessage = ({data: any}) => {
    console.log(data);
}


// 异常处理
channel.addEventListener('messageerror', e) => {
    console.error(e);
})
// 或者
channel.onmessagerror = (e) => {
    console.error(e);
}


// 关闭 channel
channel.close()
```

## 参考链接

- [MDN](https://developer.mozilla.org/zh-CN/docs/Web/API/BroadcastChannel)
- [codesandbox example](https://codesandbox.io/p/sandbox/broadcastchannel-3rdjf6)
- [单开网页应用利器-BroadcastChannel](https://mp.weixin.qq.com/s/VJk6zS1YYmSSYmr6UiQuyQ)

## 时间

2023-05-19
