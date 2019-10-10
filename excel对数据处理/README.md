# excel 数据处理

 ## 导入文件

可以从链接导入

可以从数据库导入

可以从文件导入

## 填充 

- =sum(J1,L1)

填充出现+ 直接双击就行

还有一种

- 在要截止的地方按shift选中 ，之后按ctrl +D

以十位等差填充，选中两行数据他们相差10 ，然后下拉

## 拆分数据

![1570715078873](C:\Users\14148\AppData\Local\Temp\1570715078873.png)

## 行列转换

 ![1570715286045](C:\Users\14148\AppData\Local\Temp\1570715286045.png)

## 按照颜色排序

右键按颜色排序

## 数据透视表

![1570729080850](C:\Users\14148\AppData\Local\Temp\1570729080850.png)

## 函数

sum  count

=SUMIF(D1:D20,>50)

=SUM(区域，条件，求和区域)

![1570731549035](C:\Users\14148\AppData\Local\Temp\1570731549035.png)

=COUNTIF(A:A,A1)     我用这个函数来去重玩

![1570731409360](C:\Users\14148\AppData\Local\Temp\1570731409360.png)

类似的还有AVERAGE MAX　MIN



- IF

这个函数能够用来获取指定条件的数据 比如  =IF(A1=1000025,1,0)  然后再筛选，再求和算出现几次

![1570732241273](C:\Users\14148\AppData\Local\Temp\1570732241273.png)



if 和其他函数配合使用![1570732375579](C:\Users\14148\AppData\Local\Temp\1570732375579.png)

- VLOOPUP 纵向的搜索查找 （可以用来比较两个excel 的重复情况）比如excel 和

  mysql中导出的数据是否吻合有无残缺重复 （当然用去重后的countif然后筛选也能做）

  用vloopup 的时候如果匹配不到救回是这样报错，如何解决呢？自行解决

  ![1570733738756](C:\Users\14148\AppData\Local\Temp\1570733738756.png)

  ![1570733209843](C:\Users\14148\AppData\Local\Temp\1570733209843.png)

  

- HLOOPUP 横向的搜索查找（貌似是没试过）







注：寻求office 官方文档的帮助比如

输入=sum按tab鼠标点击链接就能看