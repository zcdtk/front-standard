# TypeScript 编写代码

前端发展至今，基于 JavaScript 的语言编写代码，已经被很多人诟病。他丢失了语言内很大的一个特性，类型约束。

没有类型约束，既可以将代码编程写出任意类型。

这对开发和维护而言，都是具体的成本

示例如下：

```javascript
class A {
    
}
A.prototype.doSomeThing = function(data){
    *******
    *******
    *******
    *******
    return data;
}
```

> 注：该代码由 JavaScript 编写

在上述示例中，该函数执行一段逻辑，返回了一个传入的数据。现在的问题在于，说明文档不足，无法理解该函数传入一个说明参数。

如果需要理解，则需要开发人员调试断点，确定最后的返回参数。



```typescript
class A {
   public doSomeThing(data: Array<string>) {
        *******
        *******
        *******
        *******
        retrun data;
    } 
}
```

> 注：该代码由 TypeScript 编写

上述示例中，数据类型已经在使用时，就说明清楚了。

TypeScript  语言的出现，基本解决了 JavaScript 编写困难的那些问题，将前端语言有弱类型转换为强类型，这样的特性，是新一代前端所必须的内容.