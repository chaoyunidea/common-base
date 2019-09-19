## 拖拽指令 
**指令名称：v-drag，对绑定的元素进行拖拽**

```
<template>
  <div  style="height:84px;width:100%;" v-drag></div>
</template>

```


## 输入框规则限制

**指令名称：v-reg**

```
  <template>
      <input  type="text" v-reg:3.number/>
      <input  type="text" v-reg.floatPlus/>
      //自定义规则 v-reg传入正则 会根据规则限制输入
      <input  type="text" v-reg="/^[0-9a-zA-Z]{0,4}$/">
  </template>
```
| 类型 | 说明 | 
| --- | --- | 
| number | 数字，可传参限制位数 |
| float | 小数，可传参限制位数 |
| mobile | 手机号，0到11位数字 |
| floatPlus | 默认最多两位小数，可传参限制位数 |
| numberPlus | 默认最多999位数字，可传参限制位数 |

## 图片预览 

**指令名称：v-viewer**  
```
  <template>
      <div v-viewer>
        <img src=""/>
      </div>
  </template>  
```
