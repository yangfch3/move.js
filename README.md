# move.js
一个轻量型 DOM 动画框架

## 主函数：move(element, props[, duration][, fx][, complete])

### element
Type：`HTMLElement`

需要添加动画的 DOM 元素

### props
Type：`Object`

样式配置对象，支持大部分动画属性（自动补全、纠正单位），例如：
```javascript
move(document.body, {
    width: 500,
    // 单位 'px' 会自动补全，推荐直接使用数值
    borderTopWidth: '100px',
    opacity: 0.5,
    // backgroundSize 可以使用百分数字符串（'110%'）也可以使用数值（1.1）表示
    backgroundSize: 1.1
});
```
> CSS3 属性动画请直接使用 CSS3 实现；backgroundSize 可以使用百分数字符串也可以使用数值表示（1 == 100%）。
> 
> 查看支持哪些属性，请去往 [Demo](http://yangfch3.com/move.js/)。

### duration
Type：`Number`

动画耗时，默认为 400ms

### fx
Type：String

缓动函数名，默认为匀速线性变化，所有支持的缓动函数名称见：[http://easings.net/zh-cn](http://easings.net/zh-cn)
> 注：缓动函数全部存储在 Math.TWEEN 属性对象上，打开控制台打印 Math.TWEEN 查看详情。

### complete
Type：`Fcuntion`

动画完毕时的回调函数

## TODO
- [x] 兼容至 ~~IE8~~ IE9（天猫和淘宝近期宣布放弃对 IE8 的支持，腾讯企业号和企业微信近期也决定放弃对 IE8 的支持）
- [x] 支持 `backgroundSize` 百分字符串与数值两种值类型
- [x] Demo 完善，功能展示补全