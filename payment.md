### 服务器端对接文档

##### 1、充值回调地址

```
@url: 
    cp 提供
```

##### 2、充值回调参数说明

```
 @param: 
    game_id     (int)       游戏ID
    order_id    (string)    订单号
    uid         (int)       用户ID
    sid         (string)    服务器标识
    cp_order_id (string)    cp唯一订单
    roleid      (string)    角色ID
    rolename    (string)    角色名称
    order_money (int)       订单金额  `单位：元`
    productid   (string)    商品ID
    pay_type    (int)       支付类型 目前只有苹果内购
    ext         (string)    附属信息（cp自定义）
    time        (int)       发送时间
    sign        (string)    验证串
```

##### 2、 加密串加密说明

```
sign = md5(game_id + time + key + uid + pay_money + cp_order_id);
```

##### 3、返回参数

```
充值成功直接返回 字符串 success
如果没有成功返回 success  我服务器会判定次订单没有充值成功，每隔 5分钟会在次发送订单信息

注意：同一个订单信息有可能多次发送，如果订单已经成功 请忽略
```



