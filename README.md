# BookSourceRepository

The repository is based on GitHub to provide an open book source repository for the Deepink, and welcomes the introduction of new book sources.

仓库地址：https://raw.githubusercontent.com/chimisgo/BookSourceRepository/master/repository.json

##### 目前已收录

| 书源 | API | 类型 | 排行榜 | 账号 | 版本 |
| :----: | ------------- | :--: | :----: | :----: | :---: |
| My716 | http://api.zhuishushenqi.com | 网文 | 4 | 否 | 1.0.4 |
| 作品集 | http://zuopinj.com | 出版 | 4 | 否 | 1.0.0 |
| 稻草人书屋 | https://www.daocaorenshuwu.com | 综合 | 0 | 否 | 1.0.0 |
| 笔趣阁 | https://www.biqubao.com | 网文 | 0 | 否 | 1.0.0 |
| 亲小说 | https://www.qinxiaoshuo.com | 轻小说 | 6 | 否 | 1.0.0 |
| 轻之文库 | https://www.linovel.net | 轻小说 | 24 | 否 | 1.0.0 |
| 斋书苑 | https://www.zhaishuyuan.com | 网文 | 0 | 否 | 1.0.0 |

---

##### 书源属性讲解

- name ：书源名字
- version ：版本号，100即1.0.0
- category : 类别，0（出版）、1（网文）、2（轻小说）、3（综合）
- url ：来源链接（真实有效）
- charset ：字符集 utf-8 gbk gbk2312
- metadata： 元数据（每个子属性支持多个匹配，适应不同场景，比如排行榜或搜索）
    - name： 书名
    - author： 作者
    - cover：封面
    - summary： 摘要
    - category： 分类，例如：玄幻，武侠，连载等
    - status：状态（选填），完结 或 连载
    - update：更新时间（选填）（不填将无法检查更新）
    - link： 书籍详情地址
    - catalog：目录地址（不填视为目录与详情同一个地址）
- catalog： 目录
    - list：章节列表
    - orderBy：排序方式 0（分卷正序章节正序）1（分卷倒序章节倒序）2（分卷正序章节倒序）3（分卷倒序章节正序）
    - booklet：分卷（选填）
        - name：分卷名
        - list：章节列表
    - chapter： 章节
        - name：章节名
        - link：章节链接
- content：内容
    - text： 文本
    - filter：内容过滤（数组）
- search：搜索
    - link：链接
    - list：列表
- rank：排行榜（可选）
    - link：链接（数组）
        - name：名字
        - link：链接
    - list：列表
    - page：分页
        - index：起始索引
        - limit：单页数量
        - begin：起始页面拼接字符
        - next：下一页拼接字符
