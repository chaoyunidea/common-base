## 分页组件 {docsify-ignore-all}
 
**标签名：fe-pagination**

* 参数:：
  * ``{ Object}  page ``
    * ``{Number}  recordcount``
    * ``{Number}  pagesize``
    * ``{Number}  pageindex``
    * ``{Number}  totalpage``

```
 <template>
     <fe-pagination :page="page" @change=""> </fe-pagination>
 </template>

 <script>
    export default{
      data(){
        return {
          page:{
            recordcount:1, //总条数
            pagesize:10, //每页条数
            pageindex:1,// 当前页
            totalpage:1 //总页数
          }
        }
      }
    }
 </script>
     
```

## 标签属性说明

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| page | 分页参数 | Object |  |

## 事件说明

| 事件名 | 说明 | 类型 | 传参 |
| --- | --- | --- | --- |
| change | 翻页触发事件 | Function | change(type,val) |

## 弹窗分页组件 {docsify-ignore-all}
 
**标签名：fe-pagination-popup**

```
 <template>
     <fe-pagination-popup :page="page" @change=""> </fe-pagination-popup>
 </template>

 <script>
    export default{
      data(){
        return {
          page:{
            recordcount:1, //总条数
            pagesize:10, //每页条数
            pageindex:1,// 当前页
            totalpage:1 //总页数
          }
        }
      }
    }
 </script>
     
```

## 标签属性说明

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| page | 分页参数 | Object |  |

## 事件说明

| 事件名 | 说明 | 类型 | 传参 |
| --- | --- | --- | --- |
| change | 翻页触发事件 | Function | change(type,val) |
