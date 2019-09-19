##  默认吐司  

*  API
  * ` $xgj.toast(message) `
  * ` $xgj.toast( message, type) `
  * ` $xgj.toast( message, type,times) `
  * ` $xgj.toast( {message, type,times,icon}) `

参数说明:

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| message | 提示内容 | String | |
| type | 提示类 |  success,error,info,warning  | warning |
| times | 持续时间 | Number |  |
| icon | 单色图标的类 | String |  |

* 示例：
  
```
   $xgj.toast('评论修改成功', 'success')
```


## alert提示

*  API
  * ` $xgj.alert(option) `

参数说明:

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| title | 标题 | String | 提示 |
| msgtype | 弹窗类型 | success,error,info,warning | 'warning' |
| content | 内容 | String |   |


* 示例：
  
```
   $xgj.alert({content:'您的假期余额不足，请及时充值',msgtype:'warning'}).then(res => {
       if(res){
           console.log('点击了确定')
       }
   })

```


## confirm警告提示

*  API
  * ` $xgj.confirm(options) `
  
参数说明:

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| title | 标题 | String | 提示 |
| msgtype | 弹窗类型 | success,error,info,warning | 'warning' |
| content | 内容 | String |   |


* 示例：
  
```
   $xgj.confirm({content:'您的假期余额不足，请及时充值',msgtype:'warning'}).then(res => {
       if(res){
           console.log('点击了确定')
       }
   })

```
