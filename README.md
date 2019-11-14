#### 介绍
linux 系统安装字体。

自个的系统是Linux mint19版本，安装了WPS后总是提示某某字体没有安装。

特别是在安装navicat后，打开navicat后显示奇怪的字符，根本看不懂显示的内容。

最后发现是缺少字体。

#### 以安装wpsfont（wps字体）字体为例
将字体移动到系统文件夹下  
sudo mv  wpsfont /usr/share/fonts/  

更改文件夹权限  
sudo chmod 755 wpsfont   

进入文件夹wpsfont  
cd wpsfont 

更改文件权限   
sudo chmod 644 *  

建立字体索引信息，更新字体缓存信息
(前提示是在字体文件夹wpsfont下)   
mkfontdir  
mkfontscale   
fc-cache 