# 错误码 Error Code Map

## 短信 SMS
| 序号     | 错误码   |  错误描述  |
| -------- | -----  | ----  |
| 1        | 12     | 空号 |
| 2        | 002    | 已欠费停机 |
| 3        | 006    | 黑名单 |
| 4        | -103   | 黑名单 |
| 5        | 024    | 用户关机或无法接通 |
| 6        | 059    | 关机 |
| 7        | -131   | 验证码发送频率过高 |
| 8        | 640    | 空号 |
| 9        | -1005  | 敏感词拦截 |
| 10       | DB:0141| 用户处于运营商黑名单 |
| 11       | DB:0142| 超过日最大发送下发短信数量 |
| 12       | mk:0010| 空号 |

### alibaba.aliqin.fc.sms.num.send (短信发送)
| 错误码 | 错误描述 | 解决方案 |
| --- | --- | --- |
| isv.OUT_OF_SERVICE | 业务停机 | 登陆www.alidayu.com充值 |
| isv.PRODUCT_UNSUBSCRIBE | 产品服务未开通 | 登陆www.alidayu.com开通相应的产品服务 |
| isv.ACCOUNT_NOT_EXISTS | 账户信息不存在 | 登陆www.alidayu.com完成入驻 |
| isv.ACCOUNT_ABNORMAL | 账户信息异常 | 联系技术支持 |
| isv.SMS_TEMPLATE_ILLEGAL | 模板不合法 | 登陆www.alidayu.com查询审核通过短信模板使用 |
| isv.SMS_SIGNATURE_ILLEGAL | 签名不合法 | 登陆www.alidayu.com查询审核通过的签名使用 |
| isv.MOBILE_NUMBER_ILLEGAL | 手机号码格式错误 | 使用合法的手机号码 |
| isv.MOBILE_COUNT_OVER_LIMIT | 手机号码数量超过限制 | 批量发送，手机号码以英文逗号分隔，不超过200个号码 |
| isv.TEMPLATE_MISSING_PARAMETERS | 短信模板变量缺少参数 | 确认短信模板中变量个数，变量名，检查传参是否遗漏 |
| isv.INVALID_PARAMETERS | 参数异常 | 检查参数是否合法 |
| isv.BUSINESS_LIMIT_CONTROL | 触发业务流控限制 | 短信验证码，使用同一个签名，对同一个手机号码发送短信验证码，允许每分钟1条，累计每小时7条。 短信通知，使用同一签名、同一模板，对同一手机号发送短信通知，允许每天50条（自然日）。 |
| isv.INVALID_JSON_PARAM | JSON参数不合法 | JSON参数接受字符串值。例如{"code":"123456"}，不接收{"code":123456} |

### alibaba.aliqin.fc.sms.num.query (短信发送记录查询)
| 错误码 | 错误描述 | 解决方案 |
| --- | --- | --- |
| isv.OUT_OF_SERVICE | 业务停机 | 登陆www.alidayu.com 进入管理中心充值 |
| isv.MOBILE_NUMBER_ILLEGAL | 手机号码格式非法 | 使用合法的手机号码 |
| isv.QUERY_DATE_ILLEGAL | 查询时间非法 | 支持近30天记录查询。 |
| isv.SPLIT_PAGE_ILLEGAL | 分页参数不合法 | 每页最大显示50条记录 |
| isv.INVALID_PARAMETERS | 参数异常 | 检查参数合法性 |
| isv.ACCOUNT_NOT_EXISTS | 账户信息不存在 | 入驻阿里大于 |

## 语音 Voice
| 状态值     | 状态含义   |  错误描述  |
| -------- | -----  | ----  |
| 200000 | 用户听完语音 | 单呼时用户听完语音  |
| 200001 | 用户提前挂机未完整收听 | 单呼时用户提前挂机，未完整收听语音  |
| 200002 | 用户占线 | 单呼时指用户占线，双呼时指主叫占线  |
| 200003 | 用户收到呼叫但未接听 | 单呼时指用户未接听，双呼时指主叫未接听  |
| 200004 | 用户号码不合法 | 单呼时指用户号码不合法，双呼时指主叫号码不合法  |
| 200005 | 用户无法接通（拒绝） | 单呼时指用户无法接通，双呼时指主叫号码无法接通  |
| 200006 | 语音播放失败铃声格式有误 | 单呼时，指语音格式错误  |
| 200007 | 用户无法接通（不在服务区） | 单呼时指用户无法接通，双呼时指主叫号码无法接通  |
| 200008 | 获取按键超时 |   |
| 200010 | 关机 |   |
| 200011 | 停机 |   |
| 200100 | 呼叫结束（双呼） | 主被叫通话结束  |
| 200101 | 正在接通主叫 | 正在接通主叫  |
| 200102 | 成功接通主叫，正在接通被叫  |
| 200103 | 呼叫建立，正在通话 | 主被叫通话中  |
| 200104 | 主叫号码受限 | 主叫号码受限  |
| 200105 | 被叫号码受限 | 双呼时被叫号码受限  |
| 200111 | 被叫无法接通（拒绝） | 双呼时被叫无法接通（拒绝）  |
| 200120 | 被叫无法接通（不在服务区） | 双呼时被叫无法接通（不在服务区）  |
| 200112 | 被叫占线 | 双呼时被叫占线  |
| 200105 | 被叫号码受限 | 双呼时被叫号码受限  |
| 200113 | 被叫收到呼叫但未接听 | 双呼时被叫收到呼叫但未接听  |
| 200116 | 被叫号码不合法 | 双呼时被叫号码不合法  |
| 200117 | 来电显示号码不合法 |   |
| 9996 | 呼叫未建立或者呼叫已结束（apus） | 查询或终止呼叫时可能返回呼叫未建立或者呼叫已结束（apus）  |
| 999999 | 系统错误 |   |
| 500 | 运营商错误 |   |
| 400 | 网元繁忙 | - |

## alibaba.aliqin.fc.voice.num.singlecall (语音通知)
| 错误码 | 错误描述 | 解决方案 |
| --- | --- | --- |
| isv.OUT_OF_SERVICE | 业务停机 | 登陆www.alidayu.com充值 |
| isv.PRODUCT_UNSUBSCRIBE | 产品服务未开通 | 登陆www.alidayu.com开通相应产品服务 |
| isv.ACCOUNT_NOT_EXISTS | 账户信息不存在 | 登陆www.alidayu.com完成入驻 |
| isv.ACCOUNT_ABNORMAL | 账户信息异常 | 联系技术支持 |
| isv.VOICE_FILE_ILLEGAL | 语音文件不合法 | 登陆www.alidayu.com查询审核通过的合法语音文件使用 |
| isv.DISPLAY_NUMBER_ILLEGAL | 号显不合法 | 登陆www.alidayu.com查看合法的号显使用 |
| isv.MOBILE_NUMBER_ILLEGAL | 手机号码格式错误 | 使用合法的手机号 |
| isv.INVALID_PARAMETERS | 参数异常 | 检查参数合法性 |

## alibaba.aliqin.fc.tts.num.singlecall (文本转语音通知)
| 错误码 | 错误描述 | 解决方案 |
| --- | --- | --- |
| isv.OUT_OF_SERVICE | 业务停机 | 请登录阿里大于充值 |
| isv.PRODUCT_UNSUBSCRIBE | 未开通产品服务 | 请登录阿里大于开通相应产品服务 |
| isv.ACCOUNT_NOT_EXISTS | 账户信息不存在 | 请登录阿里大于完成入驻 |
| isv.ACCOUNT_ABNORMAL | 账户信息异常 | 请联系技术支持 |
| isv.MOBILE_NUMBER_ILLEGAL | 手机号码格式不合法 | 请使用合法的手机号码 |
| isv.TTS_TEMPLATE_ILLEGAL | 文本转语音模板不合法 | 请使用合法的文本转语音模板。登录www.alidayu.com查看已审核通过的文本转语音模板。 |
| isv.DISPLAY_NUMBER_ILLEGAL | 号显不合法 | 请使用合法的号显。登录www.alidayu.com查询已审核通过的号码 |
| isv.TEMPLATE_MISSING_PARAMETERS | 文本转语音模板参数缺失 | 登录www.alidayu.com查询文本转语音模板，检查模板参数是否漏传。 |
| isv.INVALID_PARAMETERS | 参数异常 | 请检查入参是否合法 |

## alibaba.aliqin.fc.voice.num.doublecall (多方通话)
| 错误码 | 错误描述 | 解决方案 |
| --- | --- | --- |
| isv.OUT_OF_SERVICE | 业务停机 | 登陆www.alidayu.com充值 |
| isv.PRODUCT_UNSUBSCRIBE | 产品服务未开通 | 登陆www.alidayu.com开通相应的产品服务 |
| isv.ACCOUNT_NOT_EXISTS | 账户信息不存在 | 登陆www.alidayu.com完成入驻 |
| isv.ACCOUNT_ABNORMAL | 账户信息异常 | 联系技术支持 |
| isv.MOBILE_NUMBER_ILLEGAL | 手机号码不合法 | 使用合法的手机号码 |
| isv.DISPLAY_NUMBER_ILLEGAL | 号显不合法 | 使用合法的号显 |
| isv.INVALID_PARAMETERS | 参数异常 | 检查参数是否合法 |




