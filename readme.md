豆瓣数据可视化处理<br>
1.课题分析<br>
    1.1问题描述<br>
    本项目旨在通过数据分析与可视化手段，深入探索豆瓣上电影数据的一些有趣现象，如热门电影特征、用户观影偏好、演员影响力等。你将运用Python中的Pandas库进行数据预处理、数据合并、数据统计分析，并借助Matplotlib库进行数据可视化呈现，完成一次从原始数据到洞察输出的全过程实践。

2.开发环境介绍与部署<br>
    2.1Python<br>
    2.2Jupyter Notebook<br>
    2.3Pandas和Matplotlib库<br>
    2.4环境部署过程<br>

  1.1问题描述<br>
  本项目旨在通过数据分析与可视化手段，深入探索豆瓣上电影数据的一些有趣现象，如热门电影特征、用户观影偏好、演员影响力等。你将运用Python中的Pandas库进行数据预处理、数据合并、数据统计分析，并借助Matplotlib库进行数据可视化呈现，完成一次从原始数据到洞察输出的全过程实践。

2.开发环境介绍与部署<br>
  2.1Python<br>
  2.2Jupyter Notebook<br>
  2.3Pandas和Matplotlib库<br>
  2.4环境部署过程<br>


下载安装Anaconda软件，勾选自动设定python的path，然后运行jupyterLab，使用pip安装Pandas和Matplotlib库

3.数据预处理流程<br>
    3.1缺失值处理<br>
    3.2重复值处理<br>
    3.3异常值处理<br>
    3.4数据变换与格式统一<br>

4.项目设计与代码实现<br>
    4.1数据介绍<br>
    4.2数据预处理<br>
    4.2.1数据合并<br>
    4.2.2缺失值、重复值、异常值处理<br>
    4.2.3数据变换<br>
    4.3数据统计<br>
    4.4数据分析<br>

4.项目设计与代码实现<br>
  4.1数据介绍<br>
  4.2数据预处理<br>
  4.2.1数据合并<br>
  4.2.2缺失值、重复值、异常值处理<br>
  4.2.3数据变换<br>
  4.3数据统计<br>
  4.4数据分析<br>

5.结果展示<br>
    一、数据内容<br>
    movies.csv: 电影数据。<br>
    - MOVIE_ID: 电影ID，对应豆瓣的DOUBAN_ID<br>
    - NAME: 电影名称<br>
    - ALIAS: 别名<br>
    - ACTORS: 主演<br>
    - COVER: 封面图片地址<br>
    - DIRECTORS: 导演<br>
    - GENRES: 类型<br>
    - OFFICIAL_SITE: 地址<br>
    - REGIONS: 制片国家/地区<br>
    - LANGUAGES: 语言<br>
    - RELEASE_DATE: 上映日期<br>
    - MINS: 片长<br>
    - IMDB_ID: IMDbID<br>
    - TAGS: 标签<br>
    - STORYLINE: 电影描述<br>
    - SLUG: 加密的url，可忽略<br>
    - YEAR: 年份<br>
    - ACTOR_IDS: 演员与PERSON_ID的对应关系,多个演员采用“\|”符号分割，格式“演员A:ID\|演员B:ID”；<br>
    - DIRECTOR_IDS: 导演与PERSON_ID的对应关系,多个导演采用“\|”符号分割，格式“导演A:ID\|导演B:ID”；<br>
    - rating.csv: 豆瓣用户对电影的评分数据。<br>
    - RATING_ID: 评分ID<br>
    - USER_ID：豆瓣用户ID<br>
    - MOVIE_ID: 电影ID，对应豆瓣的DOUBAN_ID<br>
    - RATING: 评分<br>
    - RATING_TIME: 评分时间<br>
    二、数据预处理<br>
        读取数据<br>
        ![image1](https://s2.loli.net/2024/10/03/oHuMbcfKzaJhGwN.png)<br>
        查看缺失值<br>
        ![image2](https://s2.loli.net/2024/10/03/l8s1TvKeBiC3o6x.png)<br>
        将上映日期的缺失值用1970填充。<br>
        ![image3](https://s2.loli.net/2024/10/03/eOcpRn7gyPhYIGF.png)<br>
        没有重复值，无需处理<br>
        ![image4](https://s2.loli.net/2024/10/03/7zJLmMOA9GHtxED.png)<br>
        将上映日期统一为年份显示<br>
        ![image5](https://s2.loli.net/2024/10/03/7zJLmMOA9GHtxED.png)<br>
        三、数据分析<br>
        给电影数据增加一列评分<br>
        ![image6](https://s2.loli.net/2024/10/03/zC7URSa4jlBnfOF.png)<br>
        给电影数据添加新的一列评分人数<br>
        ![image7](https://s2.loli.net/2024/10/03/hD1cbNSsmEJqTFr.png)<br>
        没有用户评分的电影，评分使用均值替代。<br>
        ![image8](https://s2.loli.net/2024/10/03/l8s1TvKeBiC3o6x.png)<br>
        看评分低于2个标准差的电影信息和评分数据高于2个标准差的电影信息<br>
        ![image9](https://s2.loli.net/2024/10/03/DEpOLZrlCRKftjF.png)<br>
        查看异常值<br>
        ![image10](https://s2.loli.net/2024/10/03/9O2rVGKgctYqmxQ.png)<br>
    三、数据呈现<br>
        展示不同类型电影的平均评分<br>
        ![image11](https://s2.loli.net/2024/10/03/GK82oMSVF1Cd5Oq.png)<br>
        ![image12](https://s2.loli.net/2024/10/03/oXMD4bW12CpyKFV.png)<br>
        惊悚恐怖的电影评分较低<br>
        展示不同国家电影大于50部的平均评分<br>
        ![image13](https://s2.loli.net/2024/10/03/RWVXB8sefb2km73.png)<br>
        ![image14](https://s2.loli.net/2024/10/03/H6dUYTlXPbCwGR8.png)<br>
        展示不同年份的电影的平均评分<br>
        ![image15](https://s2.loli.net/2024/10/03/NAWX8mDnFVcbOjY.png)<br>
        ![image16](https://s2.loli.net/2024/10/03/hR6QYWkZ5VEp4xB.png)<br>
        平均评分逐年递减，1910年平均评分为5.0可能是由于数据较少导致<br>
        展示不同国家/地区电影的数量<br>     
        ![image17](https://s2.loli.net/2024/10/03/kOYxAdIZjavrLbC.png)<br>
         ![image18](https://s2.loli.net/2024/10/03/6QvuBpSzU41FEng.png)<br>
        大部分国家电影数量为1，而电影数量多的国家的经济都比较发达<br>
        展示不同年份电影的数量<br>
        ![image19](https://s2.loli.net/2024/10/03/My1ZKGh6YkiFzlx.png)<br>
        ![image20](https://s2.loli.net/2024/10/03/MQDl6wdAjaYp3N5.png)<br>
        1970电影数量遥遥领先，总体来说呈逐年递增趋势<br>
        展示不同类型电影的占比<br>
        ![image21](https://s2.loli.net/2024/10/03/eEIQSOTMhsvkH4f.png)<br>
        ![image22](https://s2.loli.net/2024/10/03/BRawm6SPYVcevEf.png)<br>
        电影多数为剧情、喜剧，说明观众多数喜爱这些类型的电影<br>

6.学习体会<br>
在这个项目中，我通过数据分析和可视化手段，深入探索了豆瓣电影数据的一些有趣现象，通过使用 Python 中的 Pandas 库和 Matplotlib 库，我完成了一次从原始数据到洞察输出的全过程实践。
在这个项目中，我首先使用 Pandas 读取并加载了豆瓣电影数据，并对数据进行了清洗，包括删除重复行和处理缺失值。这一过程让我体会到数据清洗的重要性，干净的数据能够更好地为后续分析提供可靠的基础。通过数据合并，我将电影数据与其他数据集（如演员数据）进行了关联。这个过程让我学会了如何通过合并数据集来提取更多的信息，并从不同的角度分析数据。同时，我还对数据进行了转换，如创建新的列和调整数据类型。这让我对数据操作有了更深入的理解。在数据分析阶段，我计算了各种基础统计量，如平均评分、最高评分、最低评分等。通过对不同电影类型和年份的数据进行统计，我发现了一些有趣的现象。例如，不同类型的电影在评分上的差异，以及电影评分与上映年份之间的关系。在项目的最后阶段，我使用 Matplotlib 库对数据进行了可视化呈现。通过绘制柱状图和散点图，我成功展示了数据中的趋势和相关性。这个过程让我体会到数据可视化的重要性，它可以将复杂的数据以直观的形式呈现出来，让人们更容易理解数据中的含义。
通过这个项目，我对数据分析和可视化的整个流程有了更全面的了解。从数据预处理到数据合并，再到统计分析和可视化呈现，我学会了如何从原始数据中提取有价值的信息。这次实践不仅提高了我的数据分析技能，也加深了我对豆瓣电影数据的认识



