## 全局Filter过滤器  {docsify-ignore}


## 时间格式处理
**formatDatetime**
```
// 格式化date
// @param validDate 任何可以new Date()的有效日期
// @param fmt 形如 "yyyy-MM-dd hh:mm:ss", "MM月-dd日" 等字符串
Filters.formatDatetime = function(validDate, fmt) {
    if (typeof validDate === 'string'){
        validDate = validDate.replace('T',' ').replace(/-/g,'\/');
    } else if (validDate === undefined){
        return '';
    }
    let date = new Date(validDate);
    var o = {
        "M+": date.getMonth() + 1, //月份
        "d+": date.getDate(), //日
        "h+": date.getHours(), //小时
        "m+": date.getMinutes(), //分
        "s+": date.getSeconds(), //秒
        "q+": Math.floor((date.getMonth() + 3) / 3), //季度
        "S": date.getMilliseconds() //毫秒
    };
    if (/(y+)/.test(fmt)) fmt = fmt.replace(RegExp.$1, (date.getFullYear() + "").substr(4 - RegExp.$1.length));
    for (var k in o)
        if (new RegExp("(" + k + ")").test(fmt)) 
        	fmt = fmt.replace(RegExp.$1, (RegExp.$1.length == 1) ? (o[k]) : (("00" + o[k]).substr(("" + o[k]).length)));
    return fmt;
} 
```

参数说明:

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| validDate | 任何可以new Date()的有效日期 | Date | |
| fmt | 形如'yyyy-MM-dd' 日期格式 |  String  |  |


## 格式化数字
**formatNumber**

```
// 格式化数字
// @param number 必需，要格式化的数字
// @param decimals 可选，规定多少个小数位，默认两位。
// @param point 可选，规定用作小数点的字符串（默认为 . ）。
// @param thousands 可选，规定用作千位分隔符的字符串（默认为 , ），如果设置了该参数，那么所有其他参数都是必需的。
Filters.formatNumber = function(number, decimals, point, thousands) {
    //https://github.com/txgruppi/number_format
    //form http://phpjs.org/functions/number_format/
    number = (number + '').replace(/[^0-9+\-Ee.]/g, '');
    var n = !isFinite(+number) ? 0 : +number,
        prec = !isFinite(+decimals) ? 2 : Math.abs(decimals),
        sep = typeof thousands === 'string' ? thousands : ",",
        dec = point || ".",
        s = '';

    // Fix for IE parseFloat(0.55).toFixed(0) = 0;
    s = (prec ? toFixedFix(n, prec) : '' + Math.round(n)).split('.');
    if (s[0].length > 3) {
        s[0] = s[0].replace(/\B(?=(?:\d{3})+(?!\d))/g, sep);
    }
    return s.join(dec);
}

```

