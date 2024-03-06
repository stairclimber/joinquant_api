# 兼容聚宽回测环境的API接口

## 使用场景

如果你不喜欢聚宽官网在线的代码编辑器，想要在本地开发你的量化程序（vscode、pycharm），并获得良好的智能提醒和代码补全。
那么你可以使用本项目(joinquant_api)来实现目的。

## 使用方法

考虑到聚宽平台用户在程序工程化方面可能不太专业，本工具采用简单直观的使用方式，但可能不规范，望谅解~

1. 克隆本项目代码
2. 在克隆后的目录中创建您的量化策略程序，例如sma.py
3. 在量化程序中导入本项目函数定义 `from joinquant_api import *`
4. 编写您的回测代码，此时代码补全和智能提示已经正常工作
5. 量化程序编写完成后，将你的代码拷贝到聚宽在线编辑器中运行，在运行前建议在代码前加入以上几行导入语句，以确保API中的所有函数能够正常使用：
    ```python
    from jqdata import *
    from jqfactor import *
    from jqlib.optimizer import *
    from jqlib.alpha101 import *
    from jqlib.alpha191 import *
    from jqlib.technical_analysis import *
    ```
6. 大功告成

## 注意事项

1. 本代码库只包含兼容聚宽回测编程接口的函数签名、全局变量规范等接口内容，并不包含实现，只用于辅助编写代码，代码编写完成后需粘贴至聚宽在线编辑器执行。
2. 如有意见或建议，请在issue区反馈，我会尽快解决。