---
title: "自动化查找合作伙伴数据"
date: 2019-09-19T11:20:17+08:00
draft: false
---

[TOC]

# 自动化查找合作伙伴数据

## 用openpyxl操作excel

```python
#常用命令
import openpyxl
wb = openpyxl.load_workbook('gongshi_data.xlsx')
print(wb.sheetnames)                                      
wb.active
sheet = wb['Sheet1']   
sheet.cell(row=q, column=1,value=city_name[p])
sheet.cell(row=q, column=1).value=city_name[p]
wb.save(filename="gongshi_data.xlsx")
```

## 用selenium进行浏览器自动化操作

```python
#常用命令
from selenium import webdriver
driver= webdriver.Chrome()
driver.maximize_window()
driver.implicitly_wait(1)
driver.get("合作伙伴网站")
driver.find_element_by_id("需要输入的文本框元素id名").send_keys("需要输入的内容")
driver.find_element_by_id("需要输入的文本框元素id名").click()
driver.find_element_by_id("需要输入的文本框元素id名").clear()
driver.current_window_handle 
driver.execute_script("document.getElementsByClassName('隐藏的文本框元素class名')[0].style.display='block';")
driver.quit()
```

## 信息自动收集并存入表格

结合openpyxl和selenium进行自动化查找存储，用win32api模拟键盘操作进行辅助。

## 相同方法从天眼查爬数据并输出到txt

直接输出到excel，文字会乱码，猜测天眼查网站对数据的编码经行了特殊处理

## 从txt中将数据导入excel

```python
#关键函数
f1 = open("xx.txt","r") 
lines = f1.readlines()
i=2
for line in lines:
    t=line.split(" ")
    sheet.cell(row=i, column=4).value=""
    i=i+1
```

## 异常处理

```python
#关键结构
while:
    try:
        xxxxxxxxxx
    except:
        continue   
```

作用：出现异常时，自动化查找代码也会继续运行，异常部分可后期手动补全。

# 处理合作伙伴数据

## excel分类汇总功能

自定义排序，按照公司名排序（开始->排序->自定义）

删除相同行（数据->删除重复项）

分类汇总（数据->分类汇总->分类字段：公司名    /汇总方式：计数    /选定汇总项：合作伙伴类型和产品类型）

## excel合并公司相同的不同行数据合并

> 参考https://jingyan.baidu.com/article/8cdccae93575ec315413cdb0.html

```excel
"核心函数"
=IF(A3=A2,C2&"/"&B3,B3)
=IF(ISNUMBER(FIND(C3,C4)),0,1)
```

## excel图表的生成

[百度度度度度度度度度度度度度度度度度度度度度度度度](https://www.baidu.com)

# 分析合作伙伴数据

## 合作伙伴分类

见ppt

## 华为各类型合作伙伴数量表（广东）

见ppt

## 企业所拥有华为的身份数量统计（广东前十）

见ppt

# 还差一个应用数据

## ## ？

## ## 讨论？

# 将笔记部署到博客上

```git
hugo new post/huweiCooperation.md
git add -A
git commit -m "工作汇报"
git push origin master
```

www.zouliangqi.xyz