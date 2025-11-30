# DuckProto
DuckProto — A Lightweight, Extensible Binary Protocol

DuckProto 是一套基于 TCP 的轻量级、可扩展二进制通信协议。
它专为需要 
- 数据风控
- 行为模拟
- 设备数据上报
- 反爬虫，反渗透
- 跨平台（Linux / Android）通信 的场景设计

现在还处于玩具阶段，我也会有一些很烂的代码，各位看的时候可以开Issue或者PR

> win不考虑支持，除非有一个好心人自己全部移植一遍

DuckProto 的目标是提供一个 稳定、简洁、可演进 的底层数据交换标准，使上层业务能够灵活封装各种风控值、设备指纹、行为事件、结构化数据等。
