# 只能用账号密码登录，其他方式会报错？

# textnowProtect

[![License](https://img.shields.io/github/license/Issac-v/textnowProtect.svg?colorB=44cc11?maxAge=2592000)](https://github.com/Issac-v/textnowProtect/blob/master/LICENSE)

Modified based on [Arronlong / py_scripts](https://github.com/Arronlong/py_scripts), removed all other scripts, only textnow_protect_number is reserved.


# 在settings--secrets中添加变量
添加名为TEXTNOW_USERNAME、TEXTNOW_PASSWORD、TEXTNOW_NUMBER、TEXTNOW_MSG的变量
值分别为账号、密码、接收方号码、短信内容
支持多账号，多接收方号码，之间用半角逗号分隔，账号于密码的个数要对应
示例：TEXTNOW_USERNAME:aaa,bbb，TEXTNOW_PASSWORD:a11,b22，TEXTNOW_NUMBER：（123） 456-7890、TEXTNOW_MSG：from tn [by py_scripts]，注意短信内容不要输入中文，否则会报错...

# 修改发送时间
在[.github/workflows/actions.yml]中修改

语法如下：   
Minute Hour Day Month Dayofweek command   
分钟 小时 天 月 天每星期 命令   
每个字段代表的含义及取值范围如下：   
Minute ：分钟（0-59），表示每个小时的第几分钟执行该任务   
Hour ： 小时（1-23），表示每天的第几个小时执行该任务   
Day ： 日期（1-31），表示每月的第几天执行该任务   
Month ： 月份（1-12），表示每年的第几个月执行该任务   
DayOfWeek ： 星期（0-6，0代表星期天），表示每周的第几天执行该任务   
Command ： 指定要执行的命令（如果要执行的命令太多，可以把这些命令写到一个脚本里面，然后在这里直接调用这个脚本就可以了，调用的时候记得写出命令的完整路径）   
在这些字段里，除了“Command”是每次都必须指定的字段以外，其它字段皆为可选字段，可视需要决定。对于不指定的字段，要用“*”来填补其位置。同时，cron支持类似正则表达式的书写，支持如下几个特殊符号定义：   
“ * ” ，代表所有的取值范围内的数字；   
” / “， 代表”每”（“*/5”，表示每5个单位）；   
” – “， 代表从某个数字到某个数字（“1-4”，表示1-4个单位）；   
” , “， 分开几个离散的数字；   
段 含义 取值范围   
第一段 代表分钟 0—59   
第二段 代表小时 0—23   
第三段 代表日期 1—31   
第四段 代表月份 1—12   
第五段 代表星期几，0代表星期日 0—6   
