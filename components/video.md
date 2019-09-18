## 视频 {docsify-ignore-all}
 
**展示视频的组件**

* 参数:：
  * ``{ Object}  data对象 ``
    * ``{String}  FilePath`` 视频路径
    * ``{String}  ThumbPath`` 语音时长
    * ``{String}  Duration`` 视频时间长度，单位毫秒

```
 <template>
   	<fe-video-grid  
        showDelete
        :data="list"
        @del="">
    </fe-video-grid>
 </template>

 <script>
   export default {
     data(){
       return {
         data:{},//展示时的视频文件
       }
     }
   }
 </script>   
```


 
## 标签属性说明

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| data | 视频对象 | Object |  |
| showDelete | 显示删除按钮 | Bool | true |

## 事件说明

| 事件名 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| del | 删除当前项 | Function |    |
 
 


 
