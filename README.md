# monit_sdk
用户操作数据采集
M2
============

## Monit中文文档
*一个简单的数据收集SDK*

### M2嵌入文档

 `M2_PNAME` 和 `M2_URL`参数为项目id为必填

```js

 (function () {
        var M2_PNAME = '项目ID'
        var M2_URL = '发送数据地址'
        window['M2_PNAME'] = M2_PNAME;
        window['M2_URL'] = M2_URL;
        var s = document.createElement('script');
        s.type = 'text/javascript';
        s.async = true;
        s.src = '埋点sdk地址?t=' + new Date().getTime();
        var x = document.getElementsByTagName('script')[0];
        x.parentNode.insertBefore(s, x);
  })();

```

### M2 常用方法

```js

        M2.getQuest('e||null','{b:111}自定义参数','埋点id')；
        M2.setMoint('e||null','{b:111}自定义参数','埋点id')；
        M2.getAttr(key); //key为自定义参数键值 不传参为获取所有自已参数
        M2.setAttrs(object); //object为必填 示例 {b:'1111'}
        M2.removeAttr(key); // key 为自定义参数键值 必填 删除所设置的自定义属性
        M2.setUserInfo(object); //{uid:'用户id',hid:'酒店id'

```