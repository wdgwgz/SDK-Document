### 登录服务器验证说明
##### 1. 验证接口地址：
    @url:
        http://api.asm8.com/api/channel_login_verify
    
##### 2. 参数说明：
    @param: 
        game_id (int) 游戏标识
        uid (int) 登录成功后SDK返回的UID
        time 当前时间 10位时间戳
        sessionid 登录成功之后SDK返回的 sessionid
        sign 双方约定的加密串

##### 3. 加密串加密说明:
    sign = md5(game_id  +  uid  +  key  +  time);
    注：+ 不参与运算
    
##### 4. 返回参数：
    ```
        {'status':1, data:{'msg':'success'}}
        {'status':1, data:{'msg':'sign error'}}
    ```

