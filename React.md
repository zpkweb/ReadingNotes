组件的内容编写顺序如下：

static 开头的类属性，如 defaultProps、propTypes。
构造函数，constructor。
getter/setter（还不了解的同学可以暂时忽略）。
组件生命周期。
_ 开头的私有方法。
事件监听方法，handle*。
render*开头的方法，有时候 render() 方法里面的内容会分开到不同函数里面进行，这些函数都以 render* 开头。
render() 方法。