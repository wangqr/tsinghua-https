此处为清华大学校内网中支持https的网站的列表。

# Firefox用户

文件采用 HTTPS Everywhere 规则的格式，可以配合[HTTPS Everywhere 插件](https://www.eff.org/https-everywhere)实现自动访问https。安装插件后，直接复制tsinghua.xml到`%AppData%\Mozilla\Firefox\Profiles\xxxxxxxx.default\HTTPSEverywhereUserRules`目录下即可生效。

注意：

* 启用后请依次访问一遍以下网站并添加永久例外：
  * https://announce.cic.tsinghua.edu.cn
  * https://bmxxfb.cic.tsinghua.edu.cn
  * https://fdcglc.cic.tsinghua.edu.cn
  * https://gjcbg.cic.tsinghua.edu.cn
  * https://grjycx.cic.tsinghua.edu.cn
  * https://jdbsc.cic.tsinghua.edu.cn
  * https://jwcbg.cic.tsinghua.edu.cn
  * https://kywjdc.cic.tsinghua.edu.cn
  * https://kyybgxx.cic.tsinghua.edu.cn
  * https://learn.cic.tsinghua.edu.cn
  * https://life.cic.tsinghua.edu.cn
  * https://meta.cic.tsinghua.edu.cn
  * https://sykxxfb.cic.tsinghua.edu.cn
  * https://xxbg.cic.tsinghua.edu.cn
  * https://xyybg.cic.tsinghua.edu.cn
  * https://yjsy.cic.tsinghua.edu.cn
  * https://zhjw.cic.tsinghua.edu.cn
  * https://zhxxfw.cic.tsinghua.edu.cn
  * https://www.dangjian.tsinghua.edu.cn
  * https://www.hall.tsinghua.edu.cn
  * https://shetuan.student.tsinghua.edu.cn
* 网络学堂和部分网站存在混合内容的问题，请先安装Greasemonkey插件，然后使用以下脚本：
  * [Upgrade Insecure Requests](https://github.com/wangqr/dummy/raw/master/csp.user.js)
  * [HTTPS fix for learn.cic@THU](https://github.com/wangqr/dummy/raw/master/learnfix.user.js)

# Chrome用户

对于Chrome（PC/Android）而言，实现自动https的更加推荐的方式是手动添加[HSTS](https://zh.wikipedia.org/wiki/HTTP%E4%B8%A5%E6%A0%BC%E4%BC%A0%E8%BE%93%E5%AE%89%E5%85%A8)规则。注意HSTS并不允许证书例外，因此应当只添加证书合法的域名。我并不熟悉Tampermonkey的机制，因此上述Greasemonkey脚本并不能解决Chrome中的混合内容问题（参见下方注意），因此不建议以https方式访问存在此问题的网站，如info。

具体操作方法为，打开[chrome://net-internals/#hsts](chrome://net-internals/#hsts)，依次添加以下域名：

```text
academic.tsinghua.edu.cn
hq.tsinghua.edu.cn
its.tsinghua.edu.cn
learn.tsinghua.edu.cn
m.tsinghua.edu.cn
mail.tsinghua.edu.cn
mails.tsinghua.edu.cn
net.tsinghua.edu.cn
news-quest.tsinghua.edu.cn
postinfo.tsinghua.edu.cn
rsc.tsinghua.edu.cn
tuna.tsinghua.edu.cn (可勾选"Include subdomains for STS")
usereg.tsinghua.edu.cn
```

注意：

* 因为混合内容问题，网络学堂的公告不能直接显示，而需要选择“在新标签页中打开链接”才能查看。如对此介意请在上述列表中排除`learn.tsinghua.edu.cn`.

# 其他浏览器用户

我相信你们并不会希望使用这种激进的安全策略。