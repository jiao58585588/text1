- subversion  
	- checkout：第一次将远程仓库检出到本地  
	- update  ：更新远程仓库的内容
	- commit  ：提交本地的代码到远程仓库

- 三个辅助操作
	- show log  查看版本历史记录
	- revert  撤销本地代码的修改操作，还未提交代码时 
	- update to version 更新到指定版本   
	
- 忽略文件 ignore  
- 冲突 collision   
	- 原因：在同一个文件，同一处地方，修改或新增了内容，这时候产生冲突  
	- 解决  
		- svn解决， edit conflicts
			- 解决保存并mark as resolved
		- 手动解决
			- 在冲突文件删除（<<>>===）或者合并
			- 删除产生的三个多余文件
			
- 提交代码的规范
	- 先更新
	- 多提交
	- 标注明晰
	- 没有bug
	- 慎用锁定
	- 不提交自动生成文件
	- 不提交自己不明白的代码
- 分支  
	- trunk（主干）  
	- tags（处理bug等，被merge）  
	- branches（）  
	
- 上传图片可以使用相对路径  

 - PC端项目：
	- 头部布局:
		 - 导航块每个li中添加两个div，其中一行设为绝对定位以使两行重合  
	- 过渡效果在一开始就生效，需要在css样式中设置一个最初的默认值，以及transition，否则页面刷新后第一次触发过渡事件时不会产生过渡效果。
	  
- 函数反斗：对于一个频繁触发的函数，为了节约性能，在规定时间内只让最后一次函数触发生效，其他的都忽略 
	- 设置一个定时器，clearTimeout（wheelTimeout）；whelTimer=setTimeout（function（）{
	- }，200）  
- 函数的节流  
	-在全局中 var lastTime=0；函数中var nowTime=Date.now
();if(nowTime-lastTime<2000;return;)函数结尾同步时间：lastTime=nowTime；

- 1.MUI使用：  
	- 移动端使用准备：进入手机设置》开发者工具（部分手机无此设置）》。。。
- 2.一般在移动端，重置（开关按钮重置，清除定时器，清除过渡等）在touchstart中设置，尽量不要在touchend中设置，尽管也可。  
 - 3.SVN(subversion)：版本控制器  
  使用/需求：备份还原，协同修改，权限控制  

- 4.还原（已提交）：show log||update to version  
- 5.撤销（未提交）：revert？  
- 7.忽略（以使不会提交系统默认生成的无用文件）：选中被忽略文件右击tortoise》Unversion and add to ignore list》first  
- 8.用Webstrom管理svn项目：本地什么也没有，先checkout  
配置：file》settings》（search svn）subversion》右侧文件目录选择C盘》program files》sliksvn  
- >bin>svn.exe>OK  
- vcs（version control server）》checkout from local X >subversion>repositary URL>存放目录（在desktop创建新文件夹）》在新页面中打开>         打开文件>编辑>(右侧图标)commit changes/update/revert/show history  

- 9.SVN复制:右击被复制文件>subversion>branch or tag>copy from :rospository location  copy to:any licoation(选择version)  
也可以克隆整个文件夹 选择location上边的working x路径
- 10.内存溢出（timer不清除），最终导致内存泄漏  
- arr[i].splice(i,1);continue;i--(continue不能少，i--保证所有元素都被遍历，没有遗漏)  
- css选择器是从右往左解析的  
- 所有的选择器都会有开销（消耗一定时间，性能），选择器一旦多开销大  
	- 选择器一般三到四层  
- 11.引入外部资源的相对路径
	- 当在html中引入了外部css/js,那么在css、js中引入外部资源的路径是相对于html的路径，而非是相对于被引入的css/js
- 不同的选择器开销不同，开销最小的是id选择器，其次是class选择器；》type》adjacent sibling》child》伪类。（https：//csswizardry.com/2011/09/writing-efficient-css-selectors）  
- 12.css中注意问题：  
	- 子元素从父元素溢出问题  overflow：hidden
	- 层级覆盖问题 开启定位 改变z-index  
	- 2d变化和animation效果  

- 网站（https：//caniuse.com）：有关所有css、js兼容性问题

- 13.DOMContentLoaded:触发时间1.75s，等待dom元素加载完成，就立即触发，触发时间比onload早得多，Load触发时间13.43s，等到所有资源都加载完成。    
	- 所以绑定DOMContentLoaded会使浏览器解析更快。可兼容IE8以上版本浏览器if（windowt.DOMContentLoaded）{box.addEventListener('window.DOMContentLoaded',fun)}else{box.addEventListener('window.onload',fun)}
	
- 14.git
	- 分布式版本控制工具
	- 打开git.bash,命令行输入	$ git config --global user.name "username"  摁回车设置用户名成功。	  
	- cd 进入指定文件夹	
	- a.text/js/css 
