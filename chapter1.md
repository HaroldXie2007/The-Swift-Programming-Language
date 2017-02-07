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
// 输出 "Bonjour!"Swift 用字符串插值（string interpolation）的方式把常量名或者变量名当做占位符加入到长字符串中：print("The current value of friendlyWelcome is \(friendlyWelcome)")        
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

Swift 并不强制要求你在每条语句的结尾处使用分号（`;），当然，你也可以按照你自己的习惯添加分号。`

## 整数 {#b5f1a7cd15761173a095c35c5a06f177}

Swift 提供了8，16，32和64位的有符号和无符号整数类型。这些整数类型和 C 语言的命名方式很像，比如8位无符号整数类型是`UInt8，32位有符号整数类型是Int32。就像 Swift 的其他类型一样，整数类型采用大写命名法。`

### 整数范围

你可以访问不同整数类型的`min和max属性来获取对应类型的最小值和最大值：`

```
let minValue = UInt8.min  // minValue 为 0，是 UInt8 类型
let maxValue = UInt8.max  // maxValue 为 255，是 UInt8 类型
```

### Int

在32位平台上，Int和Int32长度相同。（-2,147,483,648~2,147,483,647）

在64位平台上，Int和Int64长度相同。

除非你需要特定长度的整数，一般来说使用`Int就够了。`

### UInt

尽量不要使用UInt，除非你真的需要存储一个和当前平台原生字长相同的无符号整数。除了这种情况，最好使用Int,即使你要存储的值已知是非负的。

## 浮点数 {#40eac52238bc9b30a14bc057d26b25a3}

Double表示64位浮点数。当你需要存储很大或者很高精度的浮点数时请使用此类型。

Float表示32位浮点数。精度要求不高的话可以使用此类型。

