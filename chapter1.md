# First Chapter

### 常量和变量

用`let来声明常量，用var来声明变量`

`let maximumNumberOfLoginAttempts = 10        
 var currentLoginAttempt = 0`

### 类型标注_（type annotation）_

```
var welcomeMessage: String 声明中的冒号代表着“是...类型”
```

可以在一行中定义多个同样类型的变量，用逗号分割，并在最后一个变量名之后添加类型标注：var red, green, blue: Double

### 常量和变量的命名

常量与变量名不能包含数学符号，箭头，保留的（或者非法的）Unicode 码位，连线与制表符。也不能以数字开头，但是可以在常量与变量名的其他地方包含数字。

### 输出常量和变量

`print(friendlyWelcome)  
// 输出 "Bonjour!"  
`Swift 用字符串插值（string interpolation）的方式把常量名或者变量名当做占位符加入到长字符串中：`  
print("The current value of friendlyWelcome is \(friendlyWelcome)")  
// 输出 "The current value of friendlyWelcome is Bonjour!`

## 注释 {#ee656aa13bfbf6dfd83440765959d43f}

```
// 这是一个注释
/* 这是一个,
多行注释 */
嵌套的多行注释：
* 这是第一个多行注释的开头
/* 这是第二个被嵌套的多行注释 */
这是第一个多行注释的结尾 */
```

## 分号 {#cb368833d4910b55cc4cdc5539b69b97}

Swift 并不强制要求你在每条语句的结尾处使用分号（`;`），当然，你也可以按照你自己的习惯添加分号。





