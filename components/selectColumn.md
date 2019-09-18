## 选择列 {docsify-ignore-all}
 
**标签名：fe-select-column**


```
 <template>
      <fe-select-column :columns="" cacheid="" @change=""> </fe-select-column>
 </template>

 <script>
    export default{
      data(){
        return {          
        }
      }
    }
 </script>
     
```

## 标签属性说明

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| columns | 列选择项列表 | Array |  |
| cacheid | 本地存储id 一般用模块名开头 | String |  |

## 事件说明

| 事件名 | 说明 | 类型 | 传参 |
| --- | --- | --- | --- |
| change | 触发事件 | Function |  |
