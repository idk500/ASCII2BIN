# ASCII2BIN

## 功能

通过ASCII2BIN, 可以轻松的将 `ASCII码`文件 转换为 `BIN`文件.

## 使用方法

### 环境预配置

需要安装[Perl](http://www.perl.org/get.html)

### 命令

```powershell
    ./ASCII2BIN {INPUT_FILE} {OUTPUT_FILE} {-[OPTION]} 
```

例如:

```powershell
    ./ASCII2BIN test.txt test.bin -b
```

### 参数说明

- `{INPUT_FILE}`
  - `INPUT_FILE` 是输入文件的路径,输入文件应是以`ASN`编码的TXT文本文件.
  - 当此值为空时,将自动读取同级目录下第一个`txt`文件.
  - *在未来的版本中将会支持遍历当前目录下所有文件*

- `{OUTPUT_FILE}`
  - `OUTPUT_FILE` 是输出文件的路径,输入文件应是以`ASN`编码的TXT文本文件.
  - 当此值为空时,将自动以`txt`文件名生成`bin`文件.

- `{-[OPTION]}`
  - `[OPTION]` 是增强选项,可选配置如下
    - `B` : 以`Binary`输出
    - `H` : 以`Hex`输出
    - `help` : 显示帮助信息

### 文件要求

1. txt文件以`,`分隔每2个`ASCII`字符.
2. 十六进制应以`ABCDEF`而不是`abcdef`表示

符合格式的文本如下

```text
    A1,B2,3C,4D
    5E,6F,1A
```

如您的文本不符合要求,可以使用`正则表达式`或[ezTextFormat](https://github.com/ezTextFormat)项目来轻松转换.

## 环境

- 测试环境

- 测试环境1
  - OS:WINDOWS10 1809...
  - Perl: Perl V1.03LTS...
- 测试环境2
  - OS:UBUNTU 18.03 LTS ...
  - Perl: Perl V1.03LTS...

## ToDo

- [x] ASCII2BIN
- [ ] ASCII2HEX
- [x] 通过命令行读取文件名
- [ ] 增强指令功能
- [ ] BIN2ASCII/HEX2ASCII
- [ ] 遍历同级目录所有文件
- [ ] 跨平台
- [ ] 不再需要环境依赖
- [ ] 文件预处理
- [ ] 接口标准化,准备接入EzToyBox
