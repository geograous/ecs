# ECS (Element Component System)

## 游戏领域的一种架构方式，也适用于复杂交互的场景。把数据和行为分离了，方便数据驱动的方式编写代码。

## 优点：高性能，易扩展。

## 个人理解：Component 为某种原子抽象，是一种数据描述，所有和数据相关的操作都在这里进行。Element 包含了 Component 。System 为各个功能子系统，具有 query 和 execute 两个操作。根据某种条件查找到 Element ，再依次对 Element 进行操作，或者修改 Element 中的其他 Component ，或者进行渲染等。这里比较迷幻的是没有说明视图层，个人感觉，可以把视图抽象成一个 schema 描述，当作一个 Component 存储。然后在负责渲染的 System 中进行渲染。

## 疑问：ECS 中对嵌套是怎么描述的？在复用这一块有什么实践吗？
