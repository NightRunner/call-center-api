# call-center-api doc

# 写在前面:接口返回格式:
```
	{    
		code : 0,                 //错误码,0为成功,其他都为错误
		message : "信息",         //信息
		data : {...}              //数据
	}
    
参数默认为必填,使用"[]"包含的为选填
```
# 坐席状态码:
```
	900 离线    座席不在线
	700 空闲
	600 置忙    包括普通置忙，休息等
	400 整理  客服接打完电话后用于其他操作的时间
	300 呼叫中
	200 响铃
	100 通话
```

测试地址: http://192.168.51.14:8092

## 通过用户ID获取坐席号(ok)
```
	URL: v1/get-seat-no

	参数：   
		String userId 用户id

	返回值：{
		String seatNo 坐席号
	}
```
## 获取坐席状态
```
	URL: v1/get-seat-status

	参数：   
		String seatNo 坐席号
		
	返回值：{
		Integer status 参见坐席状态码说明
	}
```
## 坐席上线(ok)
```
	URL: v1/login

	参数：   
		String seatNo 坐席号
		[String telephone 电话号码]
		
	返回值： 无
``` 

## 坐席下线(?)
```
	URL: v1/logout

	参数：   
		String seatNo 坐席号
		
	返回值： 无
``` 
## 外呼(?)
```
	URL: v1/call

	参数：   
		String seatNo 坐席号
		String telephone 被叫号码
		
	返回值： 无
``` 
## 挂断(?)
```
	URL: v1/hang-up

	参数：   
		String seatNo 坐席号
		
	返回值： 无
``` 
## 置闲(?)
```
	URL: v1/to-idle

	参数：   
		String seatNo 坐席号
		
	返回值： 无
``` 
## 置忙(?)
```
	URL: v1/to-busy

	参数：   
		String seatNo 坐席号
		
	返回值： 无
``` 
