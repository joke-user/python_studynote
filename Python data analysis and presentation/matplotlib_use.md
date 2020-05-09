##常用函数
---
* plt.plot(x,y,format_string,\*\*kwargs)  
	x:x轴数据，列表或数组  
	y:y轴数据，列表或数组。  
	format_string:控制曲线格式的字符串  
	\**kwargs:第二组或更多(x,Y,format_string)  
---
##中文字体显示
---
matplotlib默认无法显示中文字体需要修改字体  
1. rcParams属性：  
	* font.family ：用于显示字体的名字  
	* font.style “ 字体风格，正常normal或斜体italic  
	* font.size ：字体大小，整数字号或者large x-small  
	*几种中文字体种类*：  
		* SimHei  中文黑体  
		* Kaiti 中文楷体  
		* LiSu 中文隶书  
		* FangSong 中文仿宋  
		* YouYuan 中文幼圆  
		* STSong 中文宋体  
2. 在有中文输出的地方，增加一个属性：fontproperties  

---
##pyplot文本显示
---
pyplot的文本显示函数：  
* plt.xlabel() 对x轴增加文本标签  
* plt.ylabel() 对y轴增加文本显示标签  
* plt.title() 对图形整体增加文本标签  
* plt.text() 在任意位置增加文本  
* plt.annotate() 在图形中增加带箭头的注解  

---
##子图
---
1. subplot(col,row,num)  
2. subplot2grid(GridSpec,CurSpec,colspan,rowspan)  
3. GridSpec类
	import matplot.gridspec as gridspec
	gs = gridspec.GridSpec(3,3)
	ax1 = subplot(gs[0,:])
	ax2 = subplot(gs[1,0])
	ax3 = subplot(gs[1:,1:])
	ax4 = subplot(gs[2,0])  
  
<img src="/home/jokesnow/图片/note_pic/GridSpec.png" alt="GridSpec" title="GridSpec示例" width="80%" height="80%" />


