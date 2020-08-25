# textnowProtect

[![License](https://img.shields.io/github/license/Issac-v/textnowProtect.svg?colorB=44cc11?maxAge=2592000)](https://github.com/Issac-v/textnowProtect/blob/master/LICENSE)

Modified based on [Arronlong / py_scripts](https://github.com/Arronlong/py_scripts), removed all other scripts, only textnow_protect_number is reserved.



添加名为TEXTNOW_USERNAME、TEXTNOW_PASSWORD、TEXTNOW_NUMBER、TEXTNOW_MSG的变量
值分别为账号、密码、接收方号码、短信内容
支持多账号，多接收方号码，之间用半角逗号分隔，账号于密码的个数要对应
示例：TEXTNOW_USERNAME:aaa,bbb，TEXTNOW_PASSWORD:a11,b22，TEXTNOW_NUMBER：（123） 456-7890、TEXTNOW_MSG：from tn [by py_scripts]，注意短信内容不要输入中文，否则会报错...
