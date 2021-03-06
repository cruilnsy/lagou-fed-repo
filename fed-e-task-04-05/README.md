# 崔锐 | Part 4 | 模块五

## 简答题

### 1.通过该项目，请简要说明 typescript 比 javascript 的优势在哪？

Typescript 是 JavaScript 的超集，在项目中我们可以使用它来约束变量的类型，减少代码错误的发生。同时我们可以使用typescript带来的许多新的类型帮助我们提升代码的可读性与维护性。

主要不同点如下：

1.TS 是一种面向对象编程语言，而 JS 是一种脚本语言（尽管 JS 是基于对象的）。
2.TS 支持可选参数， JS 则不支持该特性。
3.TS 支持静态类型，JS 不支持。通过类型声明，在书写代码的时候，通过运算符就可以有准确的智能提示，提高效率。 严格的类型声明，可以在开发阶段就对代码的正确性做了一道保障。
4.TS 支持接口，JS 不支持接口。

具体优势例如：

a. 静态输入 静态类型化是一种功能，可以在开发人员编写脚本时检测错误。查找并修复错误是当今开发团队的迫切需求。有了这项功能，就会允许开发人员编写更健壮的代码并对其进行维护，以便使得代码质量更好、更清晰。

b. 大型的开发项目 有时为了改进开发项目，需要对代码库进行小的增量更改。这些小小的变化可能会产生严重的、意想不到的后果，因此有必要撤销这些变化。使用TypeScript工具来进行重构更变的容易、快捷。

c. 更好的协作 当发开大型项目时，会有许多开发人员，此时乱码和错误的机也会增加。类型安全是一种在编码期间检测错误的功能，而不是在编译项目时检测错误。这为开发团队创建了一个更高效的编码和调试过程。

d. 更强的生产力 干净的 ECMAScript 6 代码，自动完成和动态输入等因素有助于提高开发人员的工作效率。这些功能也有助于编译器创建优化的代码。


### 2.请简述一下支付流程

（1）点击提交订单，向服务器端发送请求，这个请求会向客户端返回一个支付地址。客户端就会跳转到这个支付地址，从而开始支付过程。（e.g. Alipay）

（2）当用户完成支付，支付系统会重定向到我们平台设置好的一个客户端地址。这会告诉用户，支付成功与否。同时，支付平台会向我们的服务器端发送一个请求（post），这个地址也提前设置好，这个请求也会告诉服务器支付成功与否。服务器端会创建订单（无论支付成功失败还是成功，会显示支付状态）

### 3.react-redux 的主要作用是什么，常用的 api 有哪些，什么作用？

Common api

Provider 有store属性：全局作用域，提供状态的存储到下面的组建中，使组建可以使用 Redux store state。

function component:

useDispatch：（相当于 mapDispatchToProps）配发任务action。

useSelector：（相当于mapStateToProps）从store中提取想要的数据

class component:

connect：连接component与store。把redux store中的变量和方法分发到component中。 connect(mapStateToProps?, mapDispatchToProps?, mergeProps?, options?)



### 4.redux 中的异步如何处理？

可以用 redux-thunk 或者 redux-saga 处理异步。redux-saga 更常用些，因为可以独立出异步函数。