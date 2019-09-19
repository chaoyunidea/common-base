## 示例 {docsify-ignore-all}
 
```
 <template>
     	<loading v-if='isloading' :bgType = '2'></loading>
 </template>

 <script>
   export default {
     data(){
       return {
         isloading:true
       }
     },
    
   }
 </script>
     
```


 
## 标签属性说明

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| isDefault | 是否默认全屏 | Boolean | true   |
| bgType | 全屏背景样式 | Number |  0  |
| showIcon | 是否显示icon图标 | Boolean | true |   


 
