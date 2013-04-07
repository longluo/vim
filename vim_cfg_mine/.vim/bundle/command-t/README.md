
      How to Install?

1. 从下载地址下载最新版本的vba文件，目前最新版本是1.4，所以安装文件是command-t-1.4.vba

2. 在~/.vim/bundle目录下创建文件夹command-t

3. 用Vim打开command-t-1.4.vba
4. 执行:UseVimball ~/.vim/bundle/command-t

进入ruby目录下编译C扩展

cd ~/.vim/bundle/command-t/ruby/command-t
ruby extconf.rb
make

      使用说明
输入:CommandT可进入文件快速定位功能，如图所示：



      ctrl+j/k 上下选择文件，选中后回车打开文件
      ctrl+t 以tab方式打开文件
      ctrl+s/v 可以水平或垂直分割窗口打开文件
      ctrl+c 退出该模式
      该插件还有个常用命令，:CommandTBuffer，可以浏览缓冲区的文件，并重新打开。操作方式同上。

      注意事项
Vim版本需要支持ruby扩展。我们可以在Vim中输入:ruby 1检查，如果出现E319: Sorry, the command is not available in this version就表示不支持。
      如果出现上述情况，我们就需要自己去编译能够支持ruby的Vim，嫌麻烦的话可以直接安装vim-nox，自带Ruby支持，在Ubuntu下安装命令如下：sudo apt-get install vim-nox。

执行ruby extconf.rb命令时如果出现找不到mkmf包的情况，说明你需要安装ruby-dev的包，在Ubuntu下安装命令如下：sudo apt-get install ruby1.8-dev。
