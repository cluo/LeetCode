#第三十七题
##Sudoku Solver
解决一个必定有解的数独问题

###版本1
使用递归方式，每次找到一个空缺，根据数独的规则，找到空缺可以填的数字，然后递归填写空，直到所有的空缺被填满。
第一次做到时候，有一个下标的位置放错了，结果浪费了我半个小时调试。。
最后结果通过，但是速度不够快。

###版本2
看了别人写的高速版本，发现思路是完全一样的，不过他添加了4个数据结构，分别用来记录，每一行出现过的数字，每一列出现过的数字，和每个方块出现过的数字，再加上还未解决的空。
这样就避免了我的代码中，每次循环要重新寻找空格和可以填写数字的时间。速度快了非常多。