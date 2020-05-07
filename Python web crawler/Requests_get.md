r.requests.get(url):返回一个response对象
Response对象的属性：
	r.status_code:HTTP请求的返回状态，200表示连接成功，404表示失败
	r.text:HTTP响应内容的字符串形式，即url对应的页面内容
	r.encoding:从HTTP header中猜测的响应内容编码方式
	r.apparent_encoding:从内容中分析出响应内容的编码方式
	r.content:HTTP响应内容的二进制形式
	
	r.encoding和r.apparent_encoding区别：
		r.encoding:如果header中不存在charset，则认为编码为ISO-8859-1
		r.apparent_encoding:根据网页内容分析出的编码方式

Requests库的异常：
	requests.ConnectionError:网络连接异常，如DNS查询失败、拒绝连接等
	requests.HTTPError:HTTP错误异常
	requests.URLRequired:URL缺失
	requests.TooManyRddirects:超过最大重定向次数，产生重定向异常
	requests.ConnectTimeout:远程连接服务器超时异常
	requests.Timeout:请求url超时
	r.raise_for_status():如果不是200，产生异常requests.HTTPError



	
