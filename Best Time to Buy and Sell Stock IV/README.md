#第一百八十八题
##Best Time to Buy and Sell Stock IV
最多进行k次股票交易，求能赚取的最大利润

###版本1
使用dp加上dfs求解，结果正确，但是超时，看来这样的效率不够高。需要找更简单的办法。

###版本2
非常神奇的解法，看别人的答案了解了此解法，原理与最大子序和相似，维护一个第j次买入，和第j次卖出的数组，每次求取从j=1..k的买入，卖出最大最大值。递推关系如下：   
cur = prices[i]; hold[j] = max(hold[j],sell[j-1] - cur); sell[j] = max(sell[j],hold[j] + cur);

看起来似乎不太理解到底怎么运作的，需要自己手动尝试一遍。原解法见地址：http://www.07net01.com/2015/08/903505.html