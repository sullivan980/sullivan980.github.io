---
title: "数学公式和图表示例"
date: 2023-07-15T10:30:00+08:00
lastmod: 2023-07-15T10:30:00+08:00
draft: false
author: "Sullivan"
tags: ["demo", "math", "diagram"]
categories: ["教程"]
description: "展示如何在博客中使用数学公式和Mermaid图表"
weight: 1
math: true      # 启用数学公式渲染
diagram: true   # 启用Mermaid图表

# 封面配置
cover:
    image: "https://picsum.photos/id/1073/800/300" 
    caption: "数学公式和图表示例" 
    alt: "数学公式和图表示例封面图" 
    relative: false
    hidden: false
---

## 数学公式示例

### 行内公式

爱因斯坦的质能方程 $E=mc^2$ 是物理学中最著名的公式之一。

当我们讨论二次方程 $ax^2 + bx + c = 0$ 的解时，可以使用公式 $x = \frac{-b \pm \sqrt{b^2-4ac}}{2a}$ 来求解。

### 独立公式

贝叶斯定理表述为：

$$P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)}$$

矩阵乘法可以表示为：

$$
\begin{pmatrix} 
a & b \\
c & d 
\end{pmatrix} \cdot
\begin{pmatrix} 
e & f \\
g & h 
\end{pmatrix} =
\begin{pmatrix} 
ae + bg & af + bh \\
ce + dg & cf + dh 
\end{pmatrix}
$$

积分公式示例：

$$\int_{a}^{b} f(x) \, dx = F(b) - F(a)$$

## Mermaid 图表示例

### 流程图

```mermaid
graph TD
    A[开始] --> B{是否已登录?}
    B -->|是| C[显示仪表盘]
    B -->|否| D[显示登录表单]
    C --> E[用户操作]
    D --> F[用户输入凭证]
    F --> G{验证凭证}
    G -->|成功| C
    G -->|失败| H[显示错误信息]
    H --> D
```

### 时序图

```mermaid
sequenceDiagram
    participant 用户
    participant 前端
    participant API
    participant 数据库
    
    用户->>前端: 点击登录按钮
    前端->>API: 发送登录请求
    API->>数据库: 查询用户信息
    数据库-->>API: 返回用户数据
    API->>API: 验证密码
    API-->>前端: 返回登录结果
    前端-->>用户: 显示登录成功/失败
```

### 类图

```mermaid
classDiagram
    class Animal {
        +String name
        +int age
        +makeSound()
    }
    
    class Dog {
        +fetch()
    }
    
    class Cat {
        +scratch()
    }
    
    Animal <|-- Dog
    Animal <|-- Cat
```

### 甘特图

```mermaid
gantt
    title 项目开发计划
    dateFormat  YYYY-MM-DD
    
    section 设计阶段
    需求分析        :a1, 2023-06-01, 7d
    原型设计        :a2, after a1, 5d
    
    section 开发阶段
    后端开发       :a3, after a2, 15d
    前端开发       :a4, after a2, 10d
    
    section 测试阶段
    单元测试        :a5, after a4, 5d
    集成测试        :a6, after a5, 5d
    
    section 发布
    部署上线        :a7, after a6, 2d
```

## 如何在文章中启用这些功能

要在文章中启用数学公式或图表功能，只需在文章的前置参数中添加以下配置：

```yaml
---
title: "文章标题"
math: true    # 启用数学公式
diagram: true # 启用图表
---
```

也可以在网站配置中全局启用这些功能：

```toml
[params.math]
  enable = true  # 全局启用数学公式

[params.diagram]
  enable = true  # 全局启用图表
```

这样配置后，只有在需要这些功能的页面才会加载相关资源，提高网站整体性能。 