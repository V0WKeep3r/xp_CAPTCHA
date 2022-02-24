# xp_CAPTCHA
## 简介
* xp_CAPTCHA burp验证码识别插件，中文名：瞎跑验证码
* 调用 http://www.kuaishibie.cn 网站的验证码识别接口
* 如果github图片加载不出来，请去博客看使用教程：http://www.nmd5.com/posts/2021-01-25-25/

********

## 使用教程

* 导入插件

![file](http://www.nmd5.com/wp-content/uploads/2021/01/600edb3d8331e.png)

![file](http://www.nmd5.com/wp-content/uploads/2021/01/600efaa4375be.png)

* Attack type处选择 Pitchfork,在http头部位置插入配置信息,选中需要跑字段和验证码。

#### 配置详情如下

```
http://www.kuaishibie.cn 处注册账号，用这个平台的原因是因为注册方便。
在http头部填入以下格式
xiapao:验证码url,验证码类型
验证码类型：纯数字=1，纯英文=2，数字英文混合=3
如：
xiapao:test,123456,http://www.xxx.coom/get-validate-code,3

账号密码，通过修改python文件中的username和password参数进行修改。避免原本header头修改导致账号密码泄漏。
```
*****

![python文件写入配置](https://image.v0w.top/2022/02/16456680715233.jpg)

![file](http://www.nmd5.com/wp-content/uploads/2021/01/600ee04b44979.png?time=111)

*****

![](https://image.v0w.top/2022/02/16456679807293.jpg)

* 导入字典

![file](http://www.nmd5.com/wp-content/uploads/2021/01/600edf10c571c.png)

![file](http://www.nmd5.com/wp-content/uploads/2021/01/600edf2b2ce28.png)

![file](http://www.nmd5.com/wp-content/uploads/2021/01/600edf49e0684.png)

******

* 开始跑他

![file](http://www.nmd5.com/wp-content/uploads/2021/01/600efc8944640.png)

![file](http://www.nmd5.com/wp-content/uploads/2021/01/600efc9a0a69d.png)

### 就是钱烧的有点快

![file](http://www.nmd5.com/wp-content/uploads/2021/01/600edff956db7.png)

*****

### 注意事项

* 我使用默认线程跑是正常的，但是如果出现验证码失效或者不对的问题，可以调成单线程试试
* 数据包一定要带cookie

*******

### 更新

* 2021-1-25 添加指定验证码类型
* 2021-1-26 修复部分ssl证书错误问题

*********

### 其他

* 博客：http://www.nmd5.com/
* 干货集中营：http://www.nmd5.com/test/index.php
