# Monkey
用Go自制解释器/编译器

# 解释器

## 词法分析

**源代码** => **词法单元** => **抽象语法树**

### 定义词法单元

``` sh
let five = 5;
let ten = 10;

let add = fn(x, y) {
    x + y;
};

let result = add(five, ten);
```

``` go
type TokenType string

type Token struct {
    Type TokenType
    Literal string
}
```

### 词法分析器

词法分析器将源代码作为输入，并输出对应的词法单元。词法分析器会遍历输入的字符，然后逐个输出识别的词法单元。


# 编译器

