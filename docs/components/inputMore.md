## 输入框定制 {docsify-ignore-all}
**标签名：fe-input-more** 
```
 <template>
     	 <fe-input-more defaut-rule="" :max="" :min="" valid-rule="" autoFormat> </fe-input-more>
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
| default-rule | 内置规则，如default-rule="number(3)" 则最多可输3位数字，有number,float,mobile,numberPlus,floatPlus(不允许输入负) | String |   |
| max | 可输入的最大数 | Number |  |
| min | 可输入的最小数 | Number |  |   
| valid-rule | 验证规则，input的时回调该函数，参数为经内置规则处理的当前值，返回值作为最终的v-model的值 | Function |  |
| autoFormat | 自动保留两位小数 | Bool | false |

 
