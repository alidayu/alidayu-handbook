# 发送第一条测试短信

## 阿里大鱼SDK短信API调用代码示例

### 请求参数
- 详细请参见[阿里大鱼短信API-请求参数](http://open.taobao.com/doc2/apiDetail?apiId=25450#s1)

### 开发者请求示例

- java

```java
//引入阿里大鱼SDK
import com.taobao.api.DefaultTaobaoClient;
import com.taobao.api.request.AlibabaAliqinFcSmsNumSendRequest;
import com.taobao.api.request.AlibabaAliqinFcSmsNumSendResponse;

//请填写自己的app key,app secret
TaobaoClient client = new DefaultTaobaoClient(url, "your_app_key", "your_app_secret");
AlibabaAliqinFcSmsNumSendRequest req = new AlibabaAliqinFcSmsNumSendRequest();

req.setExtend("123456");
req.setSmsType("normal");
req.setSmsFreeSignName("阿里大鱼");
req.setSmsParamString("{\"code\":\"888888\",\"product\":\"阿里大鱼(http://www.alidayu.com)\",\"item\":\"阿里大鱼\"}");
//请填写需要接收的手机号码
req.setRecNum("13000000000");
//短信模板id
req.setSmsTemplateCode("SMS_585014");

AlibabaAliqinFcSmsNumSendResponse rsp = client.execute(req);

System.out.println(rsp.getBody());
```

- php

```php
//引入阿里大鱼SDK
include "alidayu-openapi-php-sdk/TopSdk.php";

$c = new TopClient;
//请填写自己的app key
$c->appkey = "your_app_key";
//请填写自己的app secret
$c->secretKey = "your_app_secret";

$req = new AlibabaAliqinFcSmsNumSendRequest;
$req->setExtend("123456");
$req->setSmsType("normal");
$req->setSmsFreeSignName("阿里大鱼");
$req->setSmsParam("{\"code\": \"888888\", \"product\": \"阿里大鱼(http://www.alidayu.com)\"}");
//请填写需要接收的手机号码
$req->setRecNum("your_phone_number");
//短信模板id
$req->setSmsTemplateCode("SMS_645006");

$resp = $c->execute($req);

```

- nodejs
  - 待补充


### 阿里大鱼服务端返回示例

- 成功

```js
{
    "alibaba_aliqin_fc_sms_num_send_response":{
        "result":{
            "err_code":"0",
            "model":"134523^4351232",
            "success":false,
            "msg":"成功"
        }
    }
}
```

- 失败

```js
{
    "error_response":{
        "code":50,
        "msg":"Remote service error",
        "sub_code":"isv.invalid-parameter",
        "sub_msg":"非法参数"
    }
}
```

- 详细请参见[阿里大鱼短信API-响应参数](http://open.taobao.com/doc2/apiDetail?apiId=25450#s2)

### 错误码解释
- 详细请参见[阿里大鱼短信API-错误码解释](http://open.taobao.com/doc2/apiDetail?apiId=25450#s6)

### 常用开发工具
- [API测试工具](http://open.taobao.com/apitools/apiTools.htm?catId=20711&apiId=25450&apiName=alibaba.aliqin.fc.sms.num.send&scopeId=)
- [错误code查询](http://open.taobao.com/apitools/errorCodeSearch)