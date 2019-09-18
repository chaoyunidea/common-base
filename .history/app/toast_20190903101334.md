##  默认吐司  

*  API
  * ` app.toast(text) `
  * ` app.toast( type, text) `
  * ` app.toast( text, duration)   //text不为参数type中的值时 为此效果 `
  * ` app.toast( type, text, duration) `
  * ` app.toast( {type, text, duration}) `

参数说明:

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| text | 提示内容 | String | |
| type | 提示类 |  success  ,  error  ,  info  ,  default  | default |
| duration | 持续时间 | Number | 2000 |

* 示例：
  
```
   app.toast('自爆装置已启动', 3000 )

```


## alert提示

*  API
  * ` app.alert(text) `
  * ` app.alert(options) `
  

参数说明:

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| title | 标题 | String |   |
| titleStyle | 标题样式 | Object |   |
| text | 内容 | String |   |
| textStyle | 内容样式 | Object |   |
| html | 标签内容,出现在text上 | String\|Element |   |
| btn | 按钮配置 | Object |   |
| btn.text | 按钮文字 | String |   |
| btn.style | 按钮样式 | Object |   |
| btn.action | 按钮点击返回值 | Boolean | true |
| cancelAction | 路由变化引起的取消事件 | Boolean | false |
| clickMask2close | 遮罩层点击事件 | Function | false  |

* 示例：
  
```
   app.alert('鸡你太美').then(res => {
       if(res){
           console.log('点击了确定')
       }
   })

```


## confirm警告提示

*  API
  * ` app.confirm(text) `
  * ` app.confirm(options) `
  

参数说明:

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| title | 标题 | String |   |
| titleStyle | 标题样式 | Object |   |
| text | 内容 | String |   |
| textStyle | 内容样式 | Object |   |
| html | 标签内容,出现在text上 | String\|Element |   |
| cancelAction | 路由变化引起的取消事件 | Boolean | false |
| clickMask2close | 遮罩层点击事件 | Boolean | false  |
| btns | 按钮配置 | Array |   |
| btn.text | 按钮文字 | String |   |
| btn.style | 按钮样式 | Object |   |
| btn.action | 按钮点击返回值 | Boolean | true |


* 示例：
  
```
   app.confirm({
        text:'你是不是我最疼爱的人?',
        btns:[{
            text:'是',
            action:true,
            style:{color:'pink'}
        },{
            text:'嗯咯',
            action:true,
            style:{color:'green'}
        }]}).then(res => {
            if(res){
                //因为action都是true  点击都会进入这里
                console.log('点击了确定')
            }
        })

```


## dialog  

**命令模式弹窗**

*  API
  * ` app.dialog('alert',options) `
  * ` app.dialog('confirm',options) `

参数说明:
  同上