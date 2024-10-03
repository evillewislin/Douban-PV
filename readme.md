豆瓣数据可视化处理
1.课题分析
    1.1问题描述
    本项目旨在通过数据分析与可视化手段，深入探索豆瓣上电影数据的一些有趣现象，如热门电影特征、用户观影偏好、演员影响力等。你将运用Python中的Pandas库进行数据预处理、数据合并、数据统计分析，并借助Matplotlib库进行数据可视化呈现，完成一次从原始数据到洞察输出的全过程实践。

2.开发环境介绍与部署
    2.1Python
    2.2Jupyter Notebook
    2.3Pandas和Matplotlib库
    2.4环境部署过程

  1.1问题描述
  本项目旨在通过数据分析与可视化手段，深入探索豆瓣上电影数据的一些有趣现象，如热门电影特征、用户观影偏好、演员影响力等。你将运用Python中的Pandas库进行数据预处理、数据合并、数据统计分析，并借助Matplotlib库进行数据可视化呈现，完成一次从原始数据到洞察输出的全过程实践。

2.开发环境介绍与部署
  2.1Python
  2.2Jupyter Notebook
  2.3Pandas和Matplotlib库
  2.4环境部署过程


下载安装Anaconda软件，勾选自动设定python的path，然后运行jupyterLab，使用pip安装Pandas和Matplotlib库

3.数据预处理流程
<<<<<<< HEAD
    3.1缺失值处理
    3.2重复值处理
    3.3异常值处理
    3.4数据变换与格式统一

4.项目设计与代码实现
    4.1数据介绍
    4.2数据预处理
    4.2.1数据合并
    4.2.2缺失值、重复值、异常值处理
    4.2.3数据变换
    4.3数据统计
    4.4数据分析

  3.1缺失值处理
  3.2重复值处理
  3.3异常值处理
  3.4数据变换与格式统一

4.项目设计与代码实现
  4.1数据介绍
  4.2数据预处理
  4.2.1数据合并
  4.2.2缺失值、重复值、异常值处理
  4.2.3数据变换
  4.3数据统计
  4.4数据分析

5.结果展示
    一、数据内容
    movies.csv: 电影数据。
    - MOVIE_ID: 电影ID，对应豆瓣的DOUBAN_ID
    - NAME: 电影名称
    - ALIAS: 别名
    - ACTORS: 主演
    - COVER: 封面图片地址
    - DIRECTORS: 导演
    - GENRES: 类型
    - OFFICIAL_SITE: 地址
    - REGIONS: 制片国家/地区
    - LANGUAGES: 语言
    - RELEASE_DATE: 上映日期
    - MINS: 片长
    - IMDB_ID: IMDbID
    - TAGS: 标签
    - STORYLINE: 电影描述
    - SLUG: 加密的url，可忽略
    - YEAR: 年份
    - ACTOR_IDS: 演员与PERSON_ID的对应关系,多个演员采用“\|”符号分割，格式“演员A:ID\|演员B:ID”；
    - DIRECTOR_IDS: 导演与PERSON_ID的对应关系,多个导演采用“\|”符号分割，格式“导演A:ID\|导演B:ID”；
    - rating.csv: 豆瓣用户对电影的评分数据。
    - RATING_ID: 评分ID
    - USER_ID：豆瓣用户ID
    - MOVIE_ID: 电影ID，对应豆瓣的DOUBAN_ID
    - RATING: 评分
    - RATING_TIME: 评分时间
    二、数据预处理
        读取数据
        ![image1](https://s2.loli.net/2024/10/03/oHuMbcfKzaJhGwN.png)
        查看缺失值
        ![image2](https://s2.loli.net/2024/10/03/l8s1TvKeBiC3o6x.png)
        将上映日期的缺失值用1970填充。
        ![image3](https://s2.loli.net/2024/10/03/eOcpRn7gyPhYIGF.png)
        没有重复值，无需处理
        ![image4](https://s2.loli.net/2024/10/03/7zJLmMOA9GHtxED.png)
        将上映日期统一为年份显示
        ![image5](https://s2.loli.net/2024/10/03/7zJLmMOA9GHtxED.png)
        三、数据分析
        给电影数据增加一列评分
        ![image6](https://s2.loli.net/2024/10/03/zC7URSa4jlBnfOF.png)
        给电影数据添加新的一列评分人数
        ![image7](https://s2.loli.net/2024/10/03/hD1cbNSsmEJqTFr.png)
        没有用户评分的电影，评分使用均值替代。
        ![image8](https://s2.loli.net/2024/10/03/l8s1TvKeBiC3o6x.png)
        看评分低于2个标准差的电影信息和评分数据高于2个标准差的电影信息
        ![image9](https://s2.loli.net/2024/10/03/DEpOLZrlCRKftjF.png)
        查看异常值
        ![image10](https://s2.loli.net/2024/10/03/9O2rVGKgctYqmxQ.png)
    三、数据呈现
        展示不同类型电影的平均评分
        ![image11](https://s2.loli.net/2024/10/03/GK82oMSVF1Cd5Oq.png)
        ![image12](https://s2.loli.net/2024/10/03/oXMD4bW12CpyKFV.png)
        惊悚恐怖的电影评分较低
        展示不同国家电影大于50部的平均评分
        ![image13](https://s2.loli.net/2024/10/03/RWVXB8sefb2km73.png)
        展示不同年份的电影的平均评分
        ![image14](https://s2.loli.net/2024/10/03/H6dUYTlXPbCwGR8.png)
        ![image15](https://s2.loli.net/2024/10/03/NAWX8mDnFVcbOjY.png)
        平均评分逐年递减，1910年平均评分为5.0可能是由于数据较少导致
        展示不同国家/地区电影的数量
        ![image16](https://s2.loli.net/2024/10/03/hR6QYWkZ5VEp4xB.png)
        ![image17](https://s2.loli.net/2024/10/03/kOYxAdIZjavrLbC.png)
        大部分国家电影数量为1，而电影数量多的国家的经济都比较发达
        展示不同年份电影的数量
        ![image18](https://s2.loli.net/2024/10/03/6QvuBpSzU41FEng.png)
        ![image19](https://s2.loli.net/2024/10/03/My1ZKGh6YkiFzlx.png)
        1970电影数量遥遥领先，总体来说呈逐年递增趋势
        展示不同类型电影的占比
        ![image20](https://s2.loli.net/2024/10/03/MQDl6wdAjaYp3N5.png)
        ![image21](https://s2.loli.net/2024/10/03/eEIQSOTMhsvkH4f.png)
        ![image22](https://s2.loli.net/2024/10/03/BRawm6SPYVcevEf.png)
        电影多数为剧情、喜剧，说明观众多数喜爱这些类型的电影

6.学习体会
在这个项目中，我通过数据分析和可视化手段，深入探索了豆瓣电影数据的一些有趣现象，通过使用 Python 中的 Pandas 库和 Matplotlib 库，我完成了一次从原始数据到洞察输出的全过程实践。
在这个项目中，我首先使用 Pandas 读取并加载了豆瓣电影数据，并对数据进行了清洗，包括删除重复行和处理缺失值。这一过程让我体会到数据清洗的重要性，干净的数据能够更好地为后续分析提供可靠的基础。通过数据合并，我将电影数据与其他数据集（如演员数据）进行了关联。这个过程让我学会了如何通过合并数据集来提取更多的信息，并从不同的角度分析数据。同时，我还对数据进行了转换，如创建新的列和调整数据类型。这让我对数据操作有了更深入的理解。在数据分析阶段，我计算了各种基础统计量，如平均评分、最高评分、最低评分等。通过对不同电影类型和年份的数据进行统计，我发现了一些有趣的现象。例如，不同类型的电影在评分上的差异，以及电影评分与上映年份之间的关系。在项目的最后阶段，我使用 Matplotlib 库对数据进行了可视化呈现。通过绘制柱状图和散点图，我成功展示了数据中的趋势和相关性。这个过程让我体会到数据可视化的重要性，它可以将复杂的数据以直观的形式呈现出来，让人们更容易理解数据中的含义。
通过这个项目，我对数据分析和可视化的整个流程有了更全面的了解。从数据预处理到数据合并，再到统计分析和可视化呈现，我学会了如何从原始数据中提取有价值的信息。这次实践不仅提高了我的数据分析技能，也加深了我对豆瓣电影数据的认识




