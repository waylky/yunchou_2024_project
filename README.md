问题描述：假设校园内有一些点位，点位之间有路线连接（即点位之间的行驶时间），每个点位有给定的巡逻时间，现在出现保安巡逻问题，给定一定的巡逻要求（比如每个点位的巡逻次数），给定车辆数目和起始点，需要寻得最优方案，保证满足要求
建模：
baby version
目标函数：总时间最短？（待定）
决策变量：路线选择
约束：
流平衡，每点进入=出=给定出入量
详细：
xijk：k车是否从i到j
首先，对于每辆车，考虑它进行一次循环（其实这是不符合实际的，因为可能一次巡逻许多地方，即反复）这样，对单一车辆有经典网络流限制
即对于给定k，sigma x_j=xj_,再规定起始点为1
其次，对于每个点位，总次数要求S
即给定i，sigma,sigma xi_ _ =Si
目标函数：所有车的总路程时间+总点位巡逻时间（感觉后者可以去了，因为似乎是定值）


strong version
区别，添加频率
考虑时间窗？
我觉得可以考虑添加时间标签，即每点的时间，但由于我们的出发点多，似乎有些复杂
或者，假设时间为1h，考虑对于一个需要巡逻三次的点位，其时间窗有三个，020，2040，4060？
