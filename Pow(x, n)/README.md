#第五十题
##Pow(x,n)
计算次方
###版本1
最开始编写的代码使用累加，发现超时，改成累乘。还是在极大极小值超时。再次修改，在运行时判断是否已经超出范围，即可。
该题同样考验各种边界条件，第一次难以想到这些问题。

###版本2
查看别人的代码，发现只要把x的n次方分解，即可。当n为奇数时，结果乘以现在的x，当n是偶数时，x变成自己的平方，同时，n变成一半。