## 数组的类型

- 在 TypeScript 中，数组类型有多种定义方式，比较灵活。

### 「类型 + 方括号」表示法

- 最简单的方法是使用 「类型 + 方括号」来表示数组：

- 数组的项中 **不允许** 出现其他的类型

- 数组的一些方法的参数也会根据数组在定义时约定的类型进行限制

### 数组泛型

- 我们也可以使用数组泛型（Array Generic）`Array<elemType>` 来表示数组

### 用接口表示数组

- 接口也可以用来描述数组

- 虽然接口也可以用来描述数组，但是我们一般不会这么做，因为这种方式比前两种方式复杂多了。

- 不过有一种情况例外，那就是它常用来表示类数组。

### 类数组

- 类数组（Array-like Object）不是数组类型，比如 `arguments`

- `arguments` 实际上是一个类数组，不能用普通的数组的方式来描述，而应该用接口

- 事实上常用的类数组都有自己的接口定义，如 IArguments, NodeList, HTMLCollection 等

### any 在数组中的应用

- 一个比较常见的做法是，用 `any` 表示数组中允许出现任意类型