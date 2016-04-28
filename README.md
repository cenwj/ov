#老虎外汇对接API文档
编写目的
本文档旨在规范第三方对接的数据通信方式,数据格式等描述,目的是:

规范第三方系统与老虎外汇的系统对接

为第三方对接老虎外汇提供系统标准

1.数据类型定义
1.1 术语约定

MD5 一种不可逆加密算法

signature 数字签名

partner_key 老虎外汇分配给第三方的合作伙伴Key

private_key 老虎外汇分配给第三方的合作伙伴私有Key

partner_secret 老虎外汇分配给第三方的合作伙伴Secret

ThirdParty 第三方

1.2 加密方式

传递的所有字段拼接字符串排序后使用sha1加密,PHP加密函数如下:
在生成API请求中的签名(signature)时，需要提供账户中的public_key,partner_key和partner_secret，本例中假设

private_key  =  'juyoulicai'
partner_key  =  'partner_key'
partner_secret  =  'partner_secret'
signature =  '46f09bb9fab4f12dfc160dae12273d5332b5debe'
