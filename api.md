###.API



####.根路径: http://www.66rui.com/api/qwq


    1. /word  文字
    2. /picture 图片
    3  /video 视频
    4. /recommend 推荐
    
    
    5. /qiwen  奇闻
    6. /qushi 趣事
    7. /qutu  趣图
    8. /quwei 趣图
    
    9. /xiaohua
        1.+-- /nannv 男女
        2.+-- /qushi 糗事
        3.+-- /shenhuifu 神回复
        4.+-- /leng 冷笑话
        5.+-- /jingdian 经典
        6.+-- /jipin   极品
        7.+-- /baoxiao 爆笑
        8.+-- /neihan  内涵
        9.+-- /duanzi 段子
        10.+-- /fuqi   夫妻


	10. /face 表情
	11. /like GET
	    ?id=

	
	
        
    


##.数据据格式


1.经过分页的格式针对: 1, 2, 3, 5, 6, 7, 8, 9.*
    

    {
        'total' : 总条数
        'per_page': 每页条数
        'current_page': 当前页数
        'last_page': '最后一页'
        'next_page_url': 下一页的url
        'prev_page_url': 上一页的url
        'data': [    数据正文部分
                {
                    'xtype': 0.文字类型 1.图片类型 2.视频类型 3.混合类型 4.表情包
                    'is_gif': 是否为gif 0.不是 1.是
                    'title': 标题
                    'content': 内容，文字，混合类型为内容，图片和视频为: src: 'http://*'
                    'like': 点赞条数
                    'cover': 封面
                }
        ]
    }
    
2. 混合类型文章 格式

a.图片 b.链接 c.文字