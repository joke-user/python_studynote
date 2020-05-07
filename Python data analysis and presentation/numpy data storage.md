csv file:
np.savetxt(fname,array,fmt='%.18e',delimiter=None)
		fname:文件、字符串或产生器，可以是.gz或.bz2的压缩文件。
		array:存入文件的数组。
		fmt:写入文件的格式，例如：%d %.2f %.18e。
		delimiter:分割字符串，默认是任何空格。
	eg:a=np.arange(100）.reshape(5,20)
	   np.savetxt('a.csv',a,fmt='%d',delimiter=',')

	np.loadtxt(fname,dtype=np.float,delimiter=None,unpack=Flase)
		fname:文件、字符串或产生器，可以是.gz或.bz2的压缩文件。
		dtype:数据类型，可选
		delimiter:分割字符串，默认空格
		unpack:如果true,读入属性将分别写入不同变量。
    多维数据存取：
	a.tofile(fname,sep='',format='%s')
		fname:文件、字符串
		sep:数据分割字符串，如果是空串，写入文件为二进制。
		format:写入数据的格式。
		Note:不包含维度信息
 
	np.fromfile(fname,dtype=float,count=-1,sep='')
		fname:文件、字符串
		dtype:读取的数据类型
		count:读入的元素个数，-1表示读取整个文件
		sep:数据分割字符串

	np.save(fname,array) or np.savez(fname,array)

numpy的random中的随机数：
	rand():创建随机数数组，浮点数，[0,1),均匀分布
	randn():创建随机数组，标准正态分布
	randint(low,high,shaoe):创建随机整数或整数数组，范围是[low,high)
	shuffle(a):根据数组a的第一轴进行随机排列，改变数组
	permutation(a):根据数组a的第一轴产生一个新的乱序数组，不改变原数组
	choice(a,[size,replace,p]):从一维数组a中以概率p抽取元素，形成size形状新数组，replce表示是否可以重用元素，默认false
	uniform(low,high,size):均匀分布
	normal(loc,scale,size):正态分布，loc均值，scale标准差
	poisson(lam,size):泊松分布，lam随机事件发生率

统计函数：
	sum(a,axis):元素之和
	mean(a,axis):元素的期望
	average(a,axis,weight):加权平均值
	std(a,axis):标准差
	var(a,axis):方差

梯度函数：
	np.gradient(f):计算f中元素的梯度，当f为多维时，返回每个维度梯度
