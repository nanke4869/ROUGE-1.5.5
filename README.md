# ROUGE-1.5.5
## pyrouge使用方法

### Step 1 : Install Pyrouge from source (not from pip)
```python
git clone https://github.com/bheinzerling/pyrouge
cd pyrouge
pip install -e .
```

### Step 2 : Install official ROUGE script
```python
git clone https://github.com/andersjo/pyrouge.git rouge
```

### Step 3 : Point Pyrouge to official rouge script
```python
pyrouge_set_rouge_path /home/pyrouge/rouge/tools/ROUGE-1.5.5/
```

The path given to pyrouge should be absolute path !

### Step 4 : Install libxml parser
You need to install libxml parser :
```python
sudo apt-get install libxml-parser-perl
```

### Step 5 : Regenerate the Exceptions DB

You need to regenerate the Exceptions DB :
```python
cd rouge/tools/ROUGE-1.5.5/data
rm WordNet-2.0.exc.db
./WordNet-2.0-Exceptions/buildExeptionDB.pl ./WordNet-2.0-Exceptions ./smart_common_words.txt ./WordNet-2.0.exc.db
```

### Step 6 : Run the tests
```python
python -m pyrouge.test
```
You should see the answer:
```python
Ran 11 tests in 6.322s
OK
```

### PS: Step 2已变为私有仓库，本仓库有原文件

Step 2的文件位于：[rouge](https://github.com/nanke4869/ROUGE-1.5.5/tree/main/rouge/tools/ROUGE-1.5.5)

------
最终的文件结构为：
```
├───pyrouge
│   ├───rouge
│   │   ├───tools
│   │   │   └───ROUGE-1.5.5
```
