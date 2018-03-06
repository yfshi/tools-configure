# gitconfig
gitconfig读取顺序是系统级->全局级->本地，如果有相同的key，后面的会覆盖之前的。
* 系统级配置
	/etc/gitconfig或git config --system
* 全局级配置
	~/.gitconfig或git config --global
* 本地配置
	.git/config或git config
