# 工具方法

## isObject(target)
 ``判断目标是否为Object`` 

## isNumber(target)
 ``判断目标是否为Number``

## isFunction(target)
``判断目标是否为Function`` 

## isString(target)
``判断目标是否为String``

## isUndefined(target)
``判断目标是否为undefined``

## isNull(target)
``判断目标是否为Null``

## isBoolean(target)
``判断目标是否为布尔类型``

## isFloat(val, p)
``是否浮点数``

## isInt(target)
``是否整数``

## isTel(target)
``是否电话号码``

## isWords(target)
``是否数字字母组合``

## replaceRoundAngleNumber(target)
``替换圆角输入的数值``

## unFormartMoney(target)
``撤销金额的格式化``

## hasEmoji(target)
``是否含有表情``

## clone(obj)
``深拷贝``

## 数组方法（$xgj.tool.array）
```
/**
 * 数组中的值的存取
 * @param {Array} arr 数组
 * @param {*} item 添加或者移除的值
 * @returns {Array} arr 传入的数组
 */
export const toggle = function (arr, item) {
    var index = arr.indexOf(item);
    if (index == -1) {
        arr.push(item);
    }
    else {
        arr.splice(index, 1);
    }
    return arr;
};

/**
 * 移除数组中的某一项
 * @param {Array} arr 数组
 * @param {*} item 数组中的某一项
 * @returns {Array} arr 传入的数组
 */
export const remove = function (arr, item) {
    var index = arr.indexOf(item);
    arr.splice(index, 1);
    return arr;
};
/**
 * 按指定的长度拆分数组
 * @param {Array} arr 要拆分的数组
 * @param {Number} len 拆分的长度
 */
export const  chunk =function (arr, len) {

    var chunks = [],
        i = 0,
        n = arr.length;
  
    while (i < n) {
      chunks.push(arr.slice(i, i += len));
    }
  
    return chunks;
  }

/**
 * 不重复添加元素
 * @param {Array} arr 数组
 * @param {*} item 要添加的元素
 */
export const ensure =function (arr,item){
    var index = arr.indexOf(item);
    if (index == -1) {
       return arr.push(item);
    }
}

```

## 日期方法($xgj.tool.date)

```
-format(date,fmt);日期时间格式化，date为所需转换的时间，fmt为要转化的格式，类似于'yyyy-MM-dd'
- `getMonthDays(date,opt={fmt:'yyyy-MM-dd',weekType:0,weekPrefix:'星期'})`,获取date所在的日历月份,返回长度为42的数组,放了每一天的数据;weekType为0表示从星期一到星期日,weekPrefix切换星期一或周一;  
- `getMonthRange(date,fmt,type=0)`,同上,获取date所在的日历月份的开始日期和结束日期  
- `getWeekRange(date,fmt,type=0)`,同上,获取date所在周的开始日期和结束日期  
- `getWeekArr(date,fmt,type=0)`,同上,获取date所在周的一周日期(7天数组)  
- `getYearRange(opt={before:-5,after:10,thisYear})`,opt可选,默认返回今年为准,前5年后10年的年份数组.  
```

