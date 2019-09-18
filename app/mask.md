##  弹窗 {docsify-ignore}
$xgj.Mask(option)


* 参数:：
  * ``{ Object}  option ``
    * ``{String}  store``仓储
    * ``{String}  popups``弹窗路径映射
    * ``{String}  router``路由    
 

 
* 示例：
```
  //import popups store router
  $xgj._popup = new $xgj.Mask({
      popups,
      store,
      router
  }).show;
  $xgj.popup = function(name, params) {      
      return new Promise((resolve,reject) => {
          $xgj._popup(name, params).then(function(res) {
              resolve(res)
          }).catch(function(error) {
              reject(error)
          })
      })
  }
``````
**弹窗构造函数$xgj.Mask,项目里创建，弹窗调用方法进行传参：name ：弹窗名，params: 特性配置项，跟弹窗组件的props相对应**
