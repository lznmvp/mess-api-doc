!>  `api.bzqll.com` 此域名由于不知名网友在微信使用API,导致微信认为诱导分享 :angry: 目前在微信已经被封禁，仅做保留，5月底将停止该域名访问，如果使用此域名请尽快更换新的域名 `api.itooi.cn`

## 新版特性

1. 相对更加稳定,服务器不再过滤参数内容,用户自行解析参数,减少参数解析出错几率
2. 网易云音乐,酷我音乐可获取收费资源内容和获取更高音质的音乐（支持无损）
3. 接口更加丰富,增加部分接口和平台
4. 降低门槛,参数简单统一,支持GET,POST等请求,支持跨域调用

!>  由于空闲时间较少，文档中的实例纯属复制粘贴出来的，很多都不能用，可能有很多错误的信息，请求直接在文档项目提[issue](https://github.com/mrdong916/mess-api-doc/issues)

## 请求说明

以下所有接口请求域名为 `v1.itooi.cn`,为了降低使用门槛，所有请求为`GET`请求,你也可以试用其他请求方式

注意: 请求头中 `Content-type` 为 `application/x-www-form-urlencoded`

请求地址 = 域名 + 接口地址 + 参数

域名：`https://v1.itooi.cn`

接口地址：`netease/song`

参数：`id=526307800`

示例： `https://v1.itooi.cn/netease/song?id=526307800`

## 支持平台
    
- 网易云音乐 http://music.163.com
- QQ音乐 http://y.qq.com
- 酷狗音乐 http://www.kugou.com
- 酷我音乐 http://www.kuwo.cn

## 联系方式

- QQ群①：579621905（技术探讨）
- QQ群②：261097396（群友交流）
- 邮箱： mrdong916@163.com
- Github： http://github.com/mrdong916

## 关于项目

目前没有打算开源的想法，不过有个旧版的开源项目，右上角项目地址可以访问到 [MessMusic](http://github.com/MessMusic)，如果真的想要源码，带着你的诚意来找群主讨论价格！

## 捐赠
 
[![pay.png](https://i.loli.net/2019/04/26/5cc2a151aebe2.png)](https://i.loli.net/2019/04/26/5cc2a151aebe2.png)

## 更新日志

由于日志太多，请前往 [更新日志](changeLog.md) 查看


## 免责声明

1. 以上开发接口仅限于技术研究和项目开发练习使用，禁止商业用途，如有发现直接禁IP和域名
2. 版权归各音乐平台所有，若有侵犯版权，请联系我删除

