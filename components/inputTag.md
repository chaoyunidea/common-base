## 标签容器 {docsify-ignore-all}
 
**标签名：fe-input-tag**

```
 <template>
     <fe-input-tag list="" field="" placeholder="" btnName="" delIcon="" isline @del=""> </fe-input-tag>
 </template>

 <script>
   
 </script>
     
```


 
## 标签属性说明

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| list | 展示数据的数组 | Array |  |
| field | 显示字段名称 | String | name |
| placeholder | 占位符 | String | '' |   
| delIcon | 删除图标的class 默认为单色图标 | String |  |
| isLine | 是否单行显示 | Bool | false |

## 事件说明

| 事件名 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| del | 删除当前项 传出被点击删除元素的index | Function | del(index) |
| choose | 点击后面的选择按钮触发  | Function |  |

## 插槽
| 类型 | name |
| --- | --- |
| 前置插槽 | pre | 
| 内容插槽 | content |
| 按钮插槽 | btn |