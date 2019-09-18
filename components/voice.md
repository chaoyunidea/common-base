## 音频 {docsify-ignore-all}
 
**展示音频的组件**
**标签名：fe-voice**

* 参数:：
  * ``{ Object}  list元素 ``
    * ``{String}  filepath`` 语音的路径
    * ``{String}  filelength`` 语音时长

```
 <template>
   	<fe-voice  
        showDelete
        :list="list"
        @del="">
    </fe-voice>
 </template>

 <script>
   export default {
     data(){
       return {
         list:[],//展示时的录音文件
       }
     }
   }
 </script>   
```


 
## 标签属性说明

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| list | 语音列表 | Array |  |
| showDelete | 显示删除按钮 | Bool | true |

## 事件说明

| 事件名 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| del | 删除当前项 | Function |    |
 


 
