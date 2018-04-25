---
title: hexo使用笔记
tags: hexo
abbrlink: d6ed9cc7
date: 2018-04-25 09:56:14
---



### 添加阅读次数统计

> 参考next主题文档，使用leanCloud来统计

1.注册[leancloud](https://leancloud.cn/)账号，获取`appId`和`appKey`,具体细节可以参考[这里](https://notes.wanghao.work/2015-10-21-%E4%B8%BANexT%E4%B8%BB%E9%A2%98%E6%B7%BB%E5%8A%A0%E6%96%87%E7%AB%A0%E9%98%85%E8%AF%BB%E9%87%8F%E7%BB%9F%E8%AE%A1%E5%8A%9F%E8%83%BD.html#%E9%85%8D%E7%BD%AELeanCloud)

2.编辑`主题配置文件`，修改配项`leancloud_visitors`

```shell
leancloud_visitors:
  enable: true
  app_id: <your_app_id>
  app_key: <your_app_key>
  security: true
  betterPerformance: false
```

然后重新部署hexo博客，列表页已经有了阅读次数，但是详情页报错：`阅读次数： Counter not initialized! See more at console err msg.`
查看控制台报错，有两种方式解决：

- 使用`hexo-leancloud-counter-security`插件
- 设置`leancloud_visitors.security = false`

我这里选择第二种。设置以后重新部署hexo，即可看到阅读次数的统计。 



参考：

- [为NexT主题添加文章阅读量统计功能](https://notes.wanghao.work/2015-10-21-%E4%B8%BANexT%E4%B8%BB%E9%A2%98%E6%B7%BB%E5%8A%A0%E6%96%87%E7%AB%A0%E9%98%85%E8%AF%BB%E9%87%8F%E7%BB%9F%E8%AE%A1%E5%8A%9F%E8%83%BD.html#%E9%85%8D%E7%BD%AELeanCloud)
- [NexT官方文档](http://theme-next.iissnan.com/getting-started.html)

