## HTTP 请求报文
报文是什么? 报文其实就是具有特定格式的字符串
```
请求行        GET https://www.baidu.com/ HTTP/1.1
请求头
              Host: www.baidu.com                   主机名
              Connection: keep-alive                设置连接  keep-alive 保持连接  close 关闭
              Upgrade-Insecure-Requests: 1          升级不安全的请求.
              User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like   Gecko) Chrome/81.0.4044.92 Safari/537.36            用户代理 (客户端的字符串标识)
              Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/  *;q=0.8,application/signed-exchange;v=b3;q=0.9    接受数据类型 q 喜好系数.   吃饭0.5  睡觉0.7  玩游戏0.8  学习
              Purpose: prefetch
              Sec-Fetch-Site: none                  暴露网页与服务器之间关系
              Sec-Fetch-Mode: navigate              暴露请求的方式
              Sec-Fetch-User: ?1                    暴露是否为用户触发的请求
              Sec-Fetch-Dest: document              暴露目标资源的类型
              Accept-Encoding: gzip, deflate, br    接受的压缩方式
              Accept-Language: zh-CN,zh;q=0.9,en;q=0.8,la;q=0.7   接受的语言
              Cookie: BD_UPN=12314753; PSTM=1586223611; delPer=0; 小甜饼(每一次向服务器发送请求, 都会自动带着 cookie )
请求空行
请求体        a=100&b=200   {a:100,b:200}
```
## 请求报文的组成
1. 请求行
2. 请求头   
3. 空行
4. 请求体

### 请求行
GET https://www.baidu.com/ HTTP/1.1

* GET    请求方式 POST DELETE PATCH 
* https://www.baidu.com/     URL 地址
* HTTP/1.1       HTTP 协议版本

#### 关于 URL
* https://www.baidu.com/
* https://www.baidu.com/home/msg/data/personalcontent?num=8&indextype=manht#logo

完整 URL 的组成部分
* 协议        https
* 主机名      www.baidu.com
* 端口号      80  443
* 路径        /home/msg/data/personalcontent
* 查询字符串  num=8&indextype=manht
* 锚点        #logo

### 请求头
格式    **头的名字: 头的值**
请求头的名字可以是自定义的, 也可以使用协议规定的


### 请求体
请求体的内容格式是非常灵活的. 

## 响应
* 响应行
* 响应头
* 响应空行
* 响应体

```
响应行      HTTP/1.1 200 OK
响应头      Bdpagetype: 1                        百度自定义的响应头    
            Bdqid: 0xf403a5d7003d63ab
            Cache-Control: private              缓存控制 private 私有  public 公有
            Connection: keep-alive
            Content-Type: text/html;charset=utf-8 内容的类型. 设定响应体的格式(使用说明书)
            Date: Tue, 09 Jun 2020 01:21:15 GMT   时间
            Expires: Tue, 09 Jun 2020 01:20:41 GMT  过期时间
            Server: BWS/1.1                         服务使用的技术 nginx apache
            Set-Cookie: BDSVRTM=0; path=/           设置 cookie . 一个响应报文中可以设定多个 cookie
            Set-Cookie: BD_HOME=1; path=/
            Set-Cookie: H_PS_PSSID=31356_1469_31671_21126_31764_31321_30823_26350; path=/; domain=.baidu.com
            Strict-Transport-Security: max-age=172800    
                                                    Strict-Transport-Security与请求报文 Upgrade-insecure-Requres 对应的
            Traceid: 1591665675048351719417583079713025123243     跟踪 ID
            X-Ua-Compatible: IE=Edge,chrome=1       IE=Edge使用电脑上最新的IE解析器解析网页
            Content-Length: 241681                  响应体的长度 字节
响应空行
响应体
    <!DOCTYPE html><!--STATUS OK-->
    <html><head><meta http-equiv="Content-Type" content="text/html;charset=utf-8"><meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1"><meta content="always" name="referrer"><meta name="theme-color" content="#2932e1"><meta name="description" content="全球最大的中文搜索引擎、致力于让网民更便捷地获取信息，找到所求。百度超过千亿的中文网页数据库，可以瞬间找到相关的搜索结果。"><link rel="shortcut icon" href="/favicon.ico" type="image/x-icon" /><link rel="search" type="application/opensearchdescription+xml" href="/content-search.xml" title="百度搜索" /><link rel="icon" sizes="any" mask href="//www.baidu.com/img/baidu_85beaf5496f291521eb75ba38eacbd87.svg"><link rel="dns-prefetch" href="//dss0.bdstatic.com"/><link rel="dns-prefetch" href="//dss1.bdstatic.com"/><link rel="dns-prefetch" href="//ss1.bdstatic.com"/><link rel="dns-prefetch" href="//sp0.baidu.com"/><link rel="dns-prefetch" href="//sp1.baidu.com"/><link rel="dns-prefetch" href="//sp2.baidu.com"/><title>百度一下，你就知道</title><style index="newi" type="text/css">#form .bdsug{top:39px}.bdsug{display:none;position:absolute;width:535px;background:#fff;border:1px solid #ccc!important;_overflow:hidden;box-shadow:1px 1px 3px #ededed;-webkit-box-shadow:1px 1px 3px #ededed;-moz-box-shadow:1px 1px 3px #ededed;-o-box-shadow:1px 1px 3px #ededed}.bdsug li{width:519px;color:#000;font:14px arial;line-height:25px;padding:0 8px;position:relative;cursor:default}.bdsug li.bdsug-s{background:#f0f0f0}.bdsug-store span,.bdsug-store b{color:#7A77C8}.bdsug-store-del{font-size:12px;color:#666;text-decoration:underline;position:absolute;right:8px;top:0;cursor:pointer;display:none}.bdsug-s .bdsug-store-del{display:inline-block}.bdsug-ala{display:inline-block;border-bottom:1px solid #e6e6e6}.bdsug-ala h3{line-height:14px;background:url(//www.baidu.com/img/sug_bd.png?v=09816787.png) no-repeat left center;margin:6px 0 4px;font-size:12px;font-weight:400;color:#7B7B7B;padding-left:20px}.bdsug-ala p{font-size:14px;font-weight:700;padding-left:20px}#m .bdsug .bdsug-direct p{color:#00c;font-weight:700;line-height:34px;padding:0 8px;margin-top:0;cursor:pointer;white-space:nowrap;overflow:hidden}#m .bdsug .bdsug-direct p img{width:16px;height:16px} </style>
    </body>
        
	</html>
```
### 响应行
HTTP/1.1 200 OK
* HTTP 协议版本     HTTP/1.1
* 响应状态码        200
* 响应状态字符串     OK

### 响应头
格式:   头名字: 头值

### 响应体
格式灵活. HTML, CSS, JavaScript, 图片, 字体

### HTTP 协议 
不认识 CSS HTML JavaScript.  字符串






