# Python Crawler Notes

### 爬虫的步骤
0. 获取数据
> 本质是通过URL向服务器发出请求，服务器再把相关内容封装成一个Response对象返回，这是通过requests.get()实现的
1. 解析数据
2. 提取数据
3. 储存数据

### Response对象的常用属性
|属性|作用|
|---|---|
|response.status_code|检查请求是否成功（状态码）|
|response.content|把response对象转换为二进制数据|
|response.text|把response对象转换为字符串数据|
|response.encoding|定义response对象的编码|

### 常见响应状态码

### 爬虫伦理
- Robots协议

