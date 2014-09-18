这是一段跨平台 C 代码的尝试，利用 pthread 和 socket 实现的一个支持多客户端连接的代码。
现阶段仅测试 linux 和 windows 下可用，后续还会考虑其他平台的支持，
比如 macos 以及 arm 平台下的一些情况。
编译命令格式：
	windows MinGW
		$ gcc -o test tcp_Server.c -lpthread -lwsock32
		$ ./test.exe
	linux 
		$ gcc -o test tcp_Server.c -lpthread
		$ ./test

测试方法：
	$ nc 127.0.0.1 8888


在尝试之初尝试过 QT 的开发，可以说其跨平台性质做的还算不错，可惜发布版本需要一起打包很多库文件，
而在渗透测试过程中，对工具大小的要求很显著，所以只好转为这种人肉跨平台代码编写。