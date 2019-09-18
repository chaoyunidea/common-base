## 时间组件示例 {docsify-ignore-all}
 
**综合单个选择与快速选择时间的功能组件**

```
  <template>
    <date-bar :sdate="dataObj.sdate" :edate="dataObj.edate" :index='dataObj.index' :shortcuts='arr' @changeDate='handlechange'></date-bar>
  </template>

  <script>
    export default{
      data(){
        return {
          arr:['今天','昨天','本周','最近7天','最近30天','本月','上月'],
          dataObj:{
            sdate:'',
            edate:'',
            index:1
          }
        }
      },
      method:{
        handlechange(dataObj){
          this.dataObj = dataObj
        }
      }
    }
  </script>
 
```


 
## 标签属性说明

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| sdate | 开始日期 | String |    |
| edate | 结束日期 | String |    |
| index | 快速选择日期的下标 | Number | -1 |   
| shortcuts | 快速选择日期的数组 | Array | ['今天','昨天','本周','最近7天','最近30天','本月','上月']  |
| changeDate | 选择回调事件 | Function | |
 
