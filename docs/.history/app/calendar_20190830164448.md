## 日历日期选择弹窗 

**app.calendar(option)**   

 
* 参数:：
  * ``{ Object}  option ``
    * ``{String}  value``
    * ``{String}  autoClosed``



* 返回值：``{String} valaue``


* 用法：

  无参数时默认当天高亮， 通过参数value可控制。autoClosed选择后自动关闭
  

* 示例：

```
   app.calendar({value:'2019-08-29'}).then(res => {
    // 选中2019-08-08
    
     console.log(res) //  '2019-08-08'
     
   })

```
 


***



## 时间区域选择 

**app.quickDate(option)**  

* 参数:：
  * ``{ Object}  option ``
    * ``{Number}  type``
    * ``{Number}  quickDateIndex``
    * ``{Array}  quickDateArr``

* 返回值：
    * ``{Object} options``
      * ``{Number} index``
      * ``{Date} sdate``
      * ``{Date} edate``
 
* 示例：
```
  let shortcuts = ['不限','今天','昨天','最近7天','最近30天','近90天']
  let quickDateIndex = -99; //默认不限
  app.quickDate({type:1,shortcuts,quickDateIndex}).then(res => console.log(res))
  
  //返回 {index: "2", sdate: "2019-08-26", edate: "2019-09-01"}
```
* 配置
   * ``{Number} type``
     * 1 选择框
     * 2 滑动选择
   * `{Array} quickDateArr`


   | name | value |
        | --- | --- |
        | 不限 | -99 |
        | 今天 | 0 |
        | 昨天 | 1 |
        | 本周 | 2 |
        | 最近7天 | 3 |
        | 最近30天 | 4 |
        | 本月 | 5 |
        | 上月 | 6 | 
        | 近15天 | 7|
        | 近30天 | 8|
        | 近90天 | 9 |
 



*** 


 
 ##  滑动日期选择 

**app.datetimePicker(option)**


* 参数:：
   
| options参数 |  类型 |  默认值 | 备注 |
| --- | --- | ---| |
| title | String |  | |
| format | String | ' YYYY-MM-DD' | YYYY-MM-DD HH:mm只能选 |
| maxYear | Number | 25年后 ||
| minYear | Number | 25年前 ||
| date | Date | 今天 | 初始化日期 |
 

* 返回值：
    * ``{String} value``
 
* 示例：

```
  app.datetimePicker().then(res => {

      console.log(res)// 2019-08-30

  })
  
``````