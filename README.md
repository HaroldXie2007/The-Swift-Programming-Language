# My Awesome Book

This file file serves as your book's preface, a great place to describe your book's content and ideas.

使用关键字**`static`**来定义**类型属性**。在为类定义**计算型类型属性**时，可以改用关键字**class**来支持子类对父类的实现进行重写。（参看属性）

在方法的`func关键字之前加上关键字`**`static`**`，来指定`**`类型方法`**`。类还可以用关键字`**`class`**`来允许子类重写父类的方法实现。（参看方法）`

如果你确实需要在某个特定的方法中**修改结构体或者枚举的属性**，你可以为这个方法选择**可变\(mutating\)**行为，然后就可以从其方法内部改变它的属性。（参看方法）

定义**下标**使用**`subscript`**关键字。

如果要重写某个特性，你需要在重写定义的前面加上`override关键字。这么做，你就表明了你是想提供一个重写版本，而非错误地提供了一个相同的定义。（参看继承）`

在合适的地方，你可以通过使用`super前缀来访问超类版本的方法，属性或下标。（参看继承）`

你可以通过把方法，属性或下标标记为_`final`_来防止它们被重写，只需要在声明关键字前加上`final修饰符即可（例如：final var，final func，final class func，以及final subscript）。(参看继承）`

**便利构造器**也采用相同样式的写法，但需要在`init`关键字之前放置**`convenience`**关键字，并使用空格将它们俩分开（参考构造过程）



