
## 使用 tinypng，一键批量压缩指定文件(夹)所有文件
[引用文章](https://zhuanlan.zhihu.com/p/40944091)

### 一 到项目目录，手动创建并激活虚拟环境
#### 1. 执行创建虚拟环境
```python3
python3 -m venv venv
```
#### 2. 进入虚拟环境
```python3
source venv/bin/activate
```
#### 3. 安装tinify依赖库
```pip3
pip3 install tinify
```
#### 4. 申请tinify key
[申请KEY](https://tinypng.com/developers) 每个 key 每个月可以压缩 500 个文件。
也可以直接用我的key测试。

#### 5. 执行脚本
申请完 key 之后，更新到代码段中的：
```python3
tinify.key = "your key" # AppKey
```

```python3
python3 tinypng.py [filepath] [key]
```
参数一：filepath，必选，可以是文件，也可以是文件夹。

参数二：key，可选，自定义 key，如果输入了第三个参数，则优先使用自定义 key

压缩后的文件，默认输出到当前脚本所在目录下的 tinypng 文件夹中，如果要输出到其他位置，可以自行修改脚本实现。

PS：已使用 Python2.7 和 Python3.4 亲测有效，其他 Python 版本如果有异常，请反馈

**执行命令**
```python3
python3 tinypng.py /Users/cj/PycharmProjects/tinypng/black_dog.jpg
```


