## 显示版本和路径

```shell
pip --version
```

## 获取帮助

```shell
pip --help
```

## 升级pip
```shell
pip install --upgrade pip   #Linux/macOS 
pip install -U pip          #windows
```

## 列出所有pip包

```shell
pip list
```

## 安装

```shell
pip install 
```

## 卸载

```shell
pip uninstall
```



## 设置源

+ 全局源(清华源)

1. linux下会生成~/.config/pip/pip.conf
2. windows下会在%HOMEPATH%\pip下pip.ini（会有提示的）

```shell
pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple
```

+ 临时源

```shell
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple 【package-name】

# 例如
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple numpy
```

+ 其他源

中科大: https://pypi.mirrors.ustc.edu.cn/simple

阿里源：https://mirrors.aliyun.com/pypi/simple/

豆瓣源 ：http://pypi.douban.com/simple/

腾讯源：http://mirrors.cloud.tencent.com/pypi/simple
**注意是https和http，http的需要信任(因为未加密)**

1.安装时加入--trusted-host临时参数

```shell
pip install -i https://mirrors.aliyun.com/pypi/simple/ --trusted-host mirrors.aliyun.com【package-name】
```

2.在pip.conf中加入trusted-host选项，该方法是一劳永逸

```shell
[global]
index-url = http://mirrors.aliyun.com/pypi/simple/
[install]
trusted-host=mirrors.aliyun.com
```



## 注意缓存位置

每次pip都会下载一些包，不会自动删除，手动删除即可

1. Linux下~/.cache/pip 

2. Windows下%LocalAppData%\pip\Cache



## 时间超时问题

1. 添加参数--default-timeout=1000

2. 在配置里面[global]下添加timeout=1000



## 虚拟环境多python版本问题

使用python -m pip install

