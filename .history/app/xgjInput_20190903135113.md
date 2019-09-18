##  文本域弹窗 {docsify-ignore}

*  API
  * ` app.xgjInput(options) `
  

options参数说明:

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| content | 内容 | String | 1000  |
| max | 字符最大长度 | Num |   |
| check | 验证内容是否合理函数 | Function |   |
 


* 示例：
  
```
   app.xgjInput({
       content:123,
       max:5,
       check:function(v){
           if(v < 1000){
             return '数字不能大于1000'   //return 返回错误提示  
           } 
       }
   }).then(res => {
           //res :  {Object} String
           console.log(res)
        })

```
