# 一 基础部分

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

### 浮点数

Double表示64位浮点数。当你需要存储很大或者很高精度的浮点数时请使用此类型。

Float表示32位浮点数。精度要求不高的话可以使用此类型。

### 类型安全和类型推断

由于 Swift 是类型安全的，所以它会在编译你的代码时进行_类型检查（type checks）_，并把不匹配的类型标记为错误。这可以让你在开发的时候尽早发现并修复错误。

当你在声明常量或者变量的时候赋给它们一个字面量（literal value 或 literal）即可触发类型推断。（字面量就是会直接出现在你代码中的值，比如`42`和`3.14159`。）

例如，如果你给一个新常量赋值`42`并且没有标明类型，Swift 可以推断出常量类型是`Int`，因为你给它赋的初始值看起来像一个整数：

```
let meaningOfLife = 42
// meaningOfLife 会被推测为 Int 类型
```

同理，如果你没有给浮点字面量标明类型，Swift 会推断你想要的是`Double`：

```
let pi = 3.14159
// pi 会被推测为 Double 类型
```

当推断浮点数的类型时，Swift 总是会选择`Double`而不是`Float`。

如果表达式中同时出现了整数和浮点数，会被推断为`Double`类型：

```
let anotherPi = 3 + 0.14159
// anotherPi 会被推测为 Double 类型
```

原始值`3`没有显式声明类型，而表达式中出现了一个浮点字面量，所以表达式会被推断为`Double`类型。

### 数值型字面量

```
let decimalInteger = 17
let binaryInteger = 0b10001       // 二进制的17
let octalInteger = 0o21           // 八进制的17
let hexadecimalInteger = 0x11     // 十六进制的17

数值类字面量可以包括额外的格式来增强可读性。整数和浮点数都可以添加额外的零并且包含下划线，并不会影响字面量：

let paddedDouble = 000123.456
let oneMillion = 1_000_000
let justOverOneMillion = 1_000_000.000_000_1
```

### 整数转换

`SomeType(ofInitialValue)`

是调用 Swift 构造器并传入一个初始值的默认方法。

```
let twoThousand: UInt16 = 2_000
let one: UInt8 = 1
let twoThousandAndOne = twoThousand + UInt16(one)
```

### 整数和浮点数转换

整数和浮点数的转换必须显式指定类型：

```
let three = 3
let pointOneFourOneFiveNine = 0.14159
let pi = Double(three) + pointOneFourOneFiveNine
// pi 等于 3.14159，所以被推测为 Double 类型
```

## 类型别名 {#51c4a47321d555f07442c0e6ea9b934e}

_类型别名（type aliases）_就是给现有类型定义另一个名字。你可以使用`typealias`关键字来定义类型别名。

```
typealias AudioSample = UInt16
```

## 布尔值 {#06e1ad9139447d870c245ffbd0af2636}

Swift 有两个布尔常量，`true`和`false。`

## 元组 {#cda9f200088a3396902af2d4b5efb290}

_元组（tuples）_把多个值组合成一个复合值。元组内的值可以是任意类型，并不要求是相同类型。



