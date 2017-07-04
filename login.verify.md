## 登录验证说明

##### 1、登录验证地址

```
@url:
    http://api.asm8.com/api/channel_login_verify
```

##### 2、参数说明

```
@param:
    game_id (int) 游戏标识
    uid (int) 登录成功后SDK返回的UID
    time 当前时间 10位时间戳
    sessionid 登录成功之后SDK返回的 sessionid
    sign 双方约定的加密串
```

##### 3、加密串加密说明

```
sign = md5(game_id + uid + key + time)
注： + 不参与运算
```

**4、返回参数**

```
{'status':1, data:{'msg': 'success'}}
{'status':1, data:{'msg': 'sign error'}}
```



##### 5、实例

```
@ SDK返回参数
$uid = "*****";
$sessionid = "*******";

@平台方获取参数
$gameID = '****';
$key = "*****";


$time = time();
$sign = md5($gameID . $uid . $key . $time);
$url = "http://api.asm8.com/api/channel_login_verify";

$url = $url . "?game_id={$gameID}&uid={$uid}&time={$time}&sign={$sign}&sessionid={$sessionid}";

$res = file_get_contents($url);
var_dump($res);
```



