---
layout: post
title: "java 操作 excel"
description: ""
category: java
tags: [excel]
---
{% include JB/setup %}

###读取excel文件###
- 引入jxl.jar    
 
<br>
<pre>
<code>
//创建excel对象  
Workbook wbook = Workbook.getWorkbook(new File("g://javaexcel/test.xls"));  
//获取第一个工作对象  
Sheet sheet = wbook.getSheet(0);
//sheet行数
int rowsNum = sheet.getRows();
//sheet列数
int columNum = sheet.getColumns();
//第一行第一列的对象
Cell cell1 = sheet.getCell(0,0);
//第一行第二列的对象
Cell cell2 = sheet.getCell(1,0);
//获取内容
cell1.getContents();
</code>
</pre>

###生成excel文件###
<pre>
<code>
//打开文件
WritableWorkbook book = Workbook.createWorkbook(new File("g://javaexcel/new_test.xls"));
//创建第一页工作表
WritableSheet sheet = book.createSheet("sheet1", 0);
//第一行第一列
Label label1 = new Label(0, 0, "内容1");
//第一行第二列
Label label1 = new Label(1, 0, "内容2");
sheet.add(label1);
sheet.add(label2);
//写入并关闭
book.write();
book.close();
</code>
</pre>
