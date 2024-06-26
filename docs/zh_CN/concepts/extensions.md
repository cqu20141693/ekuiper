# 扩展

eKuiper 提供了内置的源、动作和函数作为规则的构建模块。然而，它不可能覆盖所有外部系统的源/动作连接，例如用户的私有系统与私有协议的连接。此外，内置的功能不能涵盖所有用户需要的所有计算。因此，在很多情况下，用户需要定制源、动作和功能。eKuiper 提供了扩展机制，让用户可以定制这三个方面。

## 扩展点

我们支持3种扩展点。

- 源：为 eKuiper 添加新的源类型，以便从中获取数据。新的扩展源可以在流/表定义中使用。
- 动作 Sink: 为 eKuiper 增加新的 sink 类型来发送数据。新的扩展 sink 可以在规则动作定义中使用。
- 函数: 为eKuiper添加新的函数类型来处理数据。新的扩展函数可以在规则 SQL 中使用。

## 扩展类型

我们支持3种类型的扩展。

- [Go 原生](../extension/native/overview.md)：作为 Go 插件扩展。它是性能最好的，但在开发和部署方面有很多限制。
- [Portable 插件](../extension/portable/overview.md)用 Go 或 Python 语言，以后会支持更多语言。它简化了开发和部署，限制较少。
- [外部服务](../extension/external/external_func.md)：通过配置将现有的外部 REST 或 RPC 服务包装成 eKuiper SQL 函数。这是一种快速的方式来扩展现有的服务，但它只支持函数扩展。

## 参考阅读

- [扩展参考](../extension/overview.md)
