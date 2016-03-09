# SDK

> 持续更新中

## java sdk常见问题

### 短信发送接口：无法在创建`TaobaoClient`对象的时候设置返回参数格式？
- 缺少`common-logging`工具包

```
TaobaoClient client = new DefaultTaobaoClient(url, appkey, secret,"xml");
```

### 短信查询接口：因为page_size值过大报错？
- `page_size`可设置最大值为`50`

## php sdk常见问题
### Fatal error: Class 'TopClient' not found
- 设置文件和TopSdk.php必须同目录
- `php5.3`版本以下的，需要手动设置 `__DIR__` 变量为全路径

### 短信发送接口：请求返回`http status code 500`
- 需设置php文件编码为`utf-8`


## nodejs sdk常见问题
- 暂无