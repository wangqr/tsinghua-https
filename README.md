此处为清华大学校内网中支持https的网站的列表。

文件采用 HTTPS Everywhere 规则的格式，直接复制到`%AppData%\Mozilla\Firefox\Profiles\xxxxxxxx.default\HTTPSEverywhereUserRules`目录下即可生效（其他浏览器同理）。

注意1：有大量\*.cic.tsinghua.edu.cn的网站使用\*.tsinghua.edu.cn的证书造成证书警告，需手动添加例外。

注意2：新版网络学堂(learn.cic.tsinghua.edu.cn)目前支持https但存在功能缺失，故暂时将其排除在该表外。

网络学堂和部分网站存在混合内容的问题，可以配合使用以下油猴脚本解决：
[Upgrade Insecure Requests](https://gist.github.com/wangqr/1dd12bdb798369d50bb93adcd2f1c964)
