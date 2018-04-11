# call-center-api

# 写在前面:接口返回格式:
```
    {    
        code : 0,                 //错误码,0为成功,其他都为错误
        message : "信息",         //信息
        data : {...}              //数据
    }
    
    参数默认为必填,使用"[]"包含的为选填
```

测试地址: http://192.168.51.14:8092

## 通过用户ID获取坐席号
```
    URL: v1/get-seat-no

    参数：   
		String userId 用户id
		
    返回值：{
		String seatNo 坐席号
	}
```
