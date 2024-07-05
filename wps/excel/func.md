# shortcuts
## insert function
S F3
## sum
 M =
 
# functions
## 计算奖金
> if 销售额 > 50, then 奖金 = 2000, otherwise 0
- inerst func
	- set 或选择类别 = 逻辑, select IF
	- set 测试条件 = “销售额”对应的单元格, set 真值 = 2000, 假值 = 0
## 计算个人所得税
- insert func
	- 常用公式-计算个人所得税, fill blanks in 参数输入

## count duplicated data
COUNTIF("data area","the data to count")

## lookup 单价 of 香酥花生
![01a4331937a9b83355d51044ff444776.png](:/15cabaaabac041eebd2e399b62d5a4ae)
=VLOOKUP(I7,C$7:E$16,FALSE)
> I7 = 香酥花生（名称） corresponding to 单价
> C$7:C$15:E$7:E$15 = data area（include col名称 and col 单价）
> 3 = serial number of col单价（单价 is the 3rd col）
> FALSE  = precise match (TRUE  = approx match)

## extract 性别 and birthday from 身份证
- 公式-函数-常用函数
- 提取身份证生日
	- 点击“身份证号码”右边的按钮，选择选区
- 提取身份证性别
	- the same goes

## extract first n chars / extract n chars begining from number n chars
![853aec7ed4ebb5a96da482eccdc250d4.png](../../../_resources/853aec7ed4ebb5a96da482eccdc250d4.png)
- extract 地区代码 of current 身份证, which is the 1st 6 chars
	- LEFT(A2,6)
> A2 = current 身份证
- extract 出生年份 of current 身份证, which is the 4 chars begining from the 7th char
	- MID(A2, 7, 4)
> A2 = current 身份证

## extract last n chars
![02c477ae9dfda3444dbf4b582730b919.png](../../../_resources/02c477ae9dfda3444dbf4b582730b919.png)
- extract 所在部门 from current 姓名和部门, which is the last 3 chars
RIGHT(A2,3)

## transfrom 20020908 into 2002-09-08
TEXT(B2, "0000-00-00")
> B2 = 20020908
>  "0000-00-00" = format of 2002-09-08

## evaluate the sum of 销售量 of DD(产品类别)
= SUMIF("产品类别"data_area，"DD" in col产品类别，“销售量”data_area)

## IF 迟到时间 < 0, then 0. Otherwise 迟到时间
= IF("迟到时间" < 0, 0, "迟到时间")

## evaluate date of 3 months from start_date
= EDATE(start_date, 3)

## combine/split date and time
![5dab3651344b7ebac4441893dbab3f01.png](../../../_resources/5dab3651344b7ebac4441893dbab3f01.png)
= 日期cell + 时间cell
![3cf8d12d4ce50cb505caf371a5d9578d.png](../../../_resources/3cf8d12d4ce50cb505caf371a5d9578d.png)
- 日期
	- =INT("日期+时间"cell)
- 时间
	- = 日期cell - 时间cell
