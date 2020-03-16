## aiPool-DataHub
 
> We are committed to building an open data center，just like github.

- 在线：[http://www.datashub.cn](http://www.datashub.cn)  
注意(未发布，内网穿透中，不稳定)
- 项目地址：[https://github.com/AiPoolll/DatahubOpen.git](https://github.com/AiPoolll/DatahubOpen.git)
- 网站源码地址：[https://github.com/luoaijun/Datahub](https://github.com/luoaijun/Datahub)
- 日志：

```
    - 2020.03.10-前端 update 更新了UI
    - 2020.02.16-数据后端 add 通过sparkstreaming增加实时IP黑名单屏蔽
    - 2020.02.06-后端 fix pdf全文检索，增加hashcode标记
    - 2020.02.05-后端 fix pdf全文检索
    - 2020.01.28-后端 add pdf全文检索
    - 2020.01.25-后端 add 新增pdf解析+elastic文档库
    - 2020.01.16-前端+后端 update 更新了person界面的overview ，star，fork 界面的UI，并修复了部分bug
    - 2020.01.15-前端+后端 add    在个人界面增加了star和fork的项目
    - 2020.01.15-后端 fix    解决了多用户并发上传失败的bug
    - 2020.01.15-后端 update 调整了上传策率，由简单上传更新为分片上传，
                             并采用zip压缩算法进一步提高上传速度
    - 2020.01.15-后端 fix 修复了link的历史回溯
    - 2020.01.15-前端+后端 add 新增 个人界面—Overview，修复了star，fork的显示bug
    - 2020.01.14-前端 update 调整了详情界面 UI
    - 2020.01.13-前端 add 新增PDF是否存在提示
    - 2020.01.13-前端+后端 add 新增PDF文件下载，调整了UI
    - 2020.01.13-前端+后端 add 新增PDF文件上传
    - 2020.01.10-前端+后端 add 新增自定义标签
    - 2020.01.09-前端+后端 fix 修复了star和fork的显示bug
    - 2020.01.06-前端 update ui,修正了logo
    - 2020.01.06-前端+后端 add star and ref ,并为此构建了新的link模型
    - 2020.01.03-数据后端 add sparksql 离线 IP黑名单处理写入mysql
    - 2020.01.03-数据后端 cancel 撤销sqoop: mysql-hive 
    - 2020.01.03-数据后端 add 新增定时增量更新，sqoop: mysql-hive 
    - 2020.01.03-数据后端 cancel 撤销Datax: mysql to hvie
    - 2020.01.03-数据后端 add 新增数据集成，Datax: mysql to hvie
    - 2020.01.02-后端 add 新增IP黑名单，拉黑恶意访问
    - 2019.12.31-后端 update hibernate to mybatis 
    - 2019.12.31-后端 fix searhWorch inseart
    - 2019.12.26-前端+后端 add 在搜索中嵌入了中文诗词对话系统
    - 2019.12.26-前端 delete 取消了即时搜索
    - 2019.12.26-前端 add 更新了即时搜索
    - 2019.12.26-后端 update 使用jieba构建分词接口，更新了中文分词搜索 
    - 2019.12.26-后端 Fix Search word 
    - 2019.12.25-前端+后端 update UI界面，并增加热搜词检索
    - 2019.12.25-前端 Solve了当前路由跳转不刷新界面的问题
    - 2019.12.25-前端 add 个人中心界面（持续修正中）
    - 2019.12.25-前端+后端 add search界面 （持续修正中）
    - 2019.12.24-前端 update 提议界面 （持续修正中）
    - 2019.12.23-前端 add 用自建远程图床作为本站图片来源
    - 2019.12.20-前端+后端 init 使用springboot+vue初步构建了本站
```

- 主页面  
![image](http://192.144.186.150/images/datahub/2.PNG)
- 嵌入诗词对话系统搜索页面
![image](http://192.144.186.150/images/datahub/9.PNG)
- 中文分词搜索  
![image](http://192.144.186.150/images/datahub/8.PNG)
- 自定义标签发布
![image](http://192.144.186.150/images/datahub/12.PNG)
- PDF文件上传
![image](http://192.144.186.150/images/datahub/13.PNG)
- PDF文件下载
![image](http://192.144.186.150/images/datahub/14.PNG)
- PDF存在提示
![image](http://192.144.186.150/images/datahub/15.PNG)
![image](http://192.144.186.150/images/datahub/16.PNG)
![image](http://192.144.186.150/images/datahub/17.PNG)

- 分类页面
![image](http://192.144.186.150/images/datahub/3.PNG)
- 标签页面
![image](http://192.144.186.150/images/datahub/4.PNG)
- 归档页面
![image](http://192.144.186.150/images/datahub/5.PNG)
- search页面
![image](http://192.144.186.150/images/datahub/6.PNG)
- 详细信息页面
![image](http://192.144.186.150/images/datahub/10.PNG) 
![image](http://192.144.186.150/images/datahub/11.PNG)
- 个人中心页面
![image](http://192.144.186.150/images/datahub/7.PNG)
![image](http://192.144.186.150/images/datahub/18.PNG)
![image](http://192.144.186.150/images/datahub/19.PNG)



## Datahub-thinking
### 1. star+fork 绑定page_id+user_id
1. 创建视图记录最新的user对于page的状态（star+fork）变更
2. mybatis通过user_id+page_id读取视图中type,返回给前端
 



## Datahub-idea
1. 热搜词检索
2. vue store.state 记录搜索历史
3. pdf+数据集外链
4. pdf分为原著和转载，原著需提交资料申请证明
5. 有原著证明的用户，直接提升为星级用户
6. 所有资源增加引用和点赞功能
7. 查看资源需要点赞或引用
8. 原著类型资源才能被引用
9. 追加排行榜，分为资源引用排行，资源点赞排行，用户获赞排行，用户获引用排行
10. pdf检索功能，OCR+es检索
11. 中文拼音搜索
12. 分词搜索
13. 英文搜索
14. 标签与分类检索
15. 新增ES搜索引擎
16. ip黑名单
17. fork + star 绑定user_id 和 page_id
18. 添加用户行为记录（埋点）
19. 增加自定义标签 
20. 

## Problem Record
1. 2020.3.6  luoaijun  Check  Processing  BUG: API模块打Jar运行之后，PDF上传失败
2. 2020.3.6  luoaijun  Check  Processing  BUG: 系统标签不美观，是否需要存在系统标签
3. 2020.3.6  luoaijun  Check  Processing  BUG: PDF上传进度条存在bug
4. 2020.3.6  luoaijun  Check  Processing  BUG: 提议(Proposal)板块需要继续改进
5. 2020.3.6  luoaijun  Check  Processing  BUG: 个人界面和设置界面需要继续编写
6. 2020.3.6  luoaijun  Check  Processing  BUG: 搜索词语义分析需要继续开发
7. 2020.3.6  luoaijun  Check  Processing  BUG: 点击热搜词之后没有找到该词的搜索内容
8. 2020.3.6  luoaijun  Check  Processing  BUG: 手机端适配问题
9. 2020.3.6  luoaijun  Check  Processing  BUG: 自定义标签强制写
10. 2020.3.6  luoaijun  Check  Processing  BUG: 删除方式待改进
