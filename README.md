# 生活小贴士
## 1、不同版本python
### .exe文件命名
通过python文件的不同命名，实现不同版本python的管理（python.exe以及python3.exe），一般下载后默认为python.exe，在原本文件夹中生成副本重新命名为pythonx.exe即可。
```
which python
which python3
```
![alt text](image.png)

### 用pip给不同python环境安装package
正常：默认python.exe
```
pip install xxx
```
指定python环境
```
python3 -m pip install xxx
``````

p.s. conda的话先activate环境，再pip？
```
conda activate transformers
pip install xxx
```

## 2、conda中的不同环境

```
# 检查conda版本
conda --version
# 查看所有环境
conda env list
# 创建新的环境
conda create -n env-name [list of package] [--clone xxx]
（1）-n env-name是设置新建环境的名字，list of package是可选项，选择要为该环境安装的包。
（2）如果我们没有指定安装python的版本，conda会安装我们最初安装conda时所装的那个版本的python。
（3）若创建特定python版本的包环境，需键入conda create -n env-name python=3.6
# 删除环境
conda remove -n [name] --all
```

## 3、github将master分支合并到main分支
```
# 切换本地分支为master
git checkout master
# 更新本地分支master代码为远程最新代码
git pull  
# 切换到自己的分支
git checkout [自己的分支名]  
# 合并master到自己的分支
git merge master  
# 提送自己本地分支到自己的远程分支
git push
# 若需要删除master分支
git push -d origin master # 本地合并时可能会遇到refusing to merge unrelated histories的错误，只需在后面加上--allow-unrelated-histories
```

## 4、一个有用的python库--collections【提供了高性能的数据类型】[详细介绍](https://zhuanlan.zhihu.com/p/343747724)
- Counter（计数器）

## 5、python的装饰器们
- @property：来创建只读属性，将方法转换为相同名称的只读属性，即调用的时候不用加括号()了
- @functools.lru_cache(maxsize = 300) / @functools.cache【import functools】


