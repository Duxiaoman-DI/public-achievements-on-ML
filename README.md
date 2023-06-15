# public-achievements-on-ML
度小满有数千个模型，我们研发AutoML来助力建模，从特征管理、算法选择、模型的自动调优上线都使用 AutoML，一些简单模型完全实现了自动化。   

对于一些复杂的模型，通过AutoML也能达到往往比人工还好的效果。目前在度小满，所有模型上线之前必须要通过AutoML机制。    

我们研发的AutoML创新性地提出[集成贝叶斯优化策略](#highperformance)，通过对多个代理模型进行结果优化，在更早的迭代周期内就能找到全局最优解。相关成果获得NIPS 2020黑盒优化竞赛第四名（https://bbochallenge.com/leaderboard/）。    

## <span id='highperformance'>Higher Performance for AutoML</span>: The Benefit of Various Ensemble Bayesian Optimization Strategy
**文章链接**：https://valohaichirpprod.blob.core.windows.net/papers/duxiaoman.pdf  
**文章简介**：  
在AutoML任务中，基于贝叶斯优化(BO)的方法在超参数优化方面表现出了极大的有效性。这些方法大多只使用一个模式，但每个模型都存在共通的局限性:1)容易得到次优解;2)在满足高维特征时，优化模型耗时较长。为了使AutoML任务得到更好的结果，本文提出了不同的集成贝叶斯模型，并尝试对这些模型进行探索，这些模型采用了不同代理模型融合其优点，使这些模型相互补充，缓解单一模型上的局限性。  
**相关代码**：[bbo_challenge_4th](https://github.com/SupUnicorn/bbo_challenge_4th)
![主要算法](https://raw.githubusercontent.com/Duxiaoman-DI/public-achievements-on-ML/main/highperformance.PNG)

