# Test_2_UniXGen
这是我在学习深度学习过程中尝试的第二个项目。这是UniXGen模型。详细的研究代码请参见：[UniXGen GitHub链接](https://github.com/ttumyche/UniXGen)

## week1
遇到的第一个问题：仓库里面找不到aiosignal包的1.3.1版本，于是从PIPY官网进行下载。首先下载到本地，然后再远程传输到服务器。
Python包的地址：
~~~
cd ~/.conda/envs/UniXGen/lib/python3.6/site-packages
~~~
工程地址：
~~~
cd ~/temp/UniXGen/code/UniXGen
~~~
解压`.tar.gz`文件：
~~~
tar -xzvf test.tar.gz
~~~
进入到这个包文件夹里面，使用:
~~~
python setup.py install
~~~

参考网站：[如何使用.tar.gz文件](https://blog.csdn.net/abcdrachel/article/details/100665420)。

好多包装不上,问题出在python的版本上，从3.6换成3.9就解决了。

## week2

第一次运行报错，
~~~
requests.exceptions.ConnectionError: HTTPSConnectionPool(host='heibox.uni-heidelberg.de', port=443): Max retries exceeded with url: /f/607503859c864bc1b30b/?dl=1 (Caused by NewConnectionError('<urllib3.connection.HTTPSConnection object at 0x7f94a5d76
~~~
解决方法是手动访问该地址进行下载，在远程上传到对应文件夹里面。
第二次运行报错：![不存在对应的文件夹](https://github.com/Gbone414/Test_2_UniXGen/assets/143300567/9b991991-ec2b-4090-ac12-e310c91a4f08)，是数据集中的report部分（数据集有report部分和JPG部分），名字在csv文件中有，直接根据`/metadate`中的.csv生成这些.txt文件，几十万个。生成之后再运行。运行过程中发现img的路径应该设置错了，可能读取完report之后读不到图片数据集，之后看看报错

