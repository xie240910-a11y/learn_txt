grep常用参数
	-i 忽略大小写
	-v 反向匹配，不包含
	-r 递归搜索 
	-R 递归 + 跟随软链接
	-l 只显示文件名
	-L 显示不匹配的文件
	-c 统计匹配次数
	-w 完整单词匹配
	-o 只输出匹配部分
	-A 显示后几行
	-B 只显示前几行
	-C 显示上下文
	-E 扩展正则
	--color 高亮 grep --color=auto "ERROR" log.txt
	
netstat -anu 查看端口信息
ss -tuln 查看端口信息 
	-t TCP
	-u UDP
	-l 只显示监听（LISTEN）
	-n 数字显示，不解析域名
	-p 显示PID/程序名
	
readelf -h 文件名 查看文件的属性
uname -m 查看系统类型是x86还是arm

vim命令
	i 在光标前插入
	a 在光标后插入
	o 在下一行插入
	O 在上一行插入
	
	h j k l 左下上右
	0 行首
	^ 行首第一个非空字符
	$ 行尾
	gg 文件开头
	G 文件末尾
	:10 跳到第10行
	
	x 删除当前字符
	dd 删除整行
	dw 删除一个单词
	d$ 删除到行尾
	
	yy 复制整行
	yw 复制单词
	p 拷贝后面 + 跟O、o联动
	P 拷贝前面 
	
	u 撤销
	ctrl + r 重做
	
	/ xxx 向下搜索
	? xxx 向上搜索
	n 下一个
	N 上一个
	
	:s/old/new/g 当前行替换
	:%s/old/new/g 全文替换
	:%s/old/new/gc 全文替换 + 确认
	
	:set nu显示行号

# go交叉编译ARM环境
GOOS=linux GOARCH=arm64 go build -o app_arm64 main.go