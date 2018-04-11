# call-center-api
## 收藏的线上商品列表
```
    URL: api/v1/member/favorite/spu/list

    参数：   
		[Integer page 页码,]
		[Integer size 页大小]
		
    必须登录：是

    返回值：Page {
		String id,
		Integer convertToPointPercent 让利比,
		String name 名称,
		String sn 编码,
		String introduction 商品介绍,
		Long weight 重量,
		Long volume 体积,
		String shopId 线上店铺ID,
		String mainImageUrl 主图,
		String price 价格,
		String point 积分,
		Integer recentSales 最近销量,
		Boolean freightFree 是否包邮
		Integer status  -1:下架,0:审核中,1:上架,
		Integer stock 库存量
	}
```
