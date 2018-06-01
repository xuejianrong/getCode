# getCode
getWeixinCode and getQQCode 获取微信授权和qq授权的中转页

> 假设域名是 www.Jrrr.com

## 微信授权地址
```
https://www.Jrrr.com/get-weixin-code.html?appid=appid&scope=snsapi_userinfo&state=state&redirect_uri=uri
```
> 使用http或者https都可以，公众号需要配置“网页授权域名”

| 参数 | 说明 |
| :--- | :--- |
| appid | 公众号appid |
| scope | snsapi_userinfo 需要用户授权，能拿到用户头像和昵称等信息，snsapi_base 只能拿到openid（unionID不能） |
| state | 填写state就行，重定向后会带上state参数，可以填写a-zA-Z0-9的参数值，最多128字节 |
| redirect_uri | 回调的url，会带上code，和from（自己加上去的区分微信（weixin）还是qq(qq)） |


## qq授权地址
```
https://www.Jrrr.com/get-qq-code.html?client_id=client_id&redirect_uri=redirect_uri&state=state&display=mobile
```
> 使用http或者https都可以，腾讯开放平台或者qq互联需要配置“网页授权域名”
| 参数 | 说明 |
| :--- | :--- |
| client_id | 网页应用的appid（需要在 腾讯开放平台或者qq互联 创建） |
| state | 填写state就行，重定向后会带上state参数，可以填写a-zA-Z0-9的参数值，最多128字节 |
| display | 填写mobile就行，默认为PC端样式，mobile为手机端样式 |
| redirect_uri | 回调的url，会带上code，和from（自己加上去的区分微信（weixin）还是qq(qq)） |
