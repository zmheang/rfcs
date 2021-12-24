- Start Date: (fill me in with today's date, YYYY-MM-DD)        // 开始时间
- Target Major Version: (2.x / 3.x)                             // 目标Vue版本
- Reference Issues: (fill in existing related issues, if any)   // 相关的issue
- Implementation PR: (leave this empty)                         // 关于实施

# Summary   // 概要

Brief explanation of the feature.   // 功能的简要说明

# Basic example // 基本例子

If the proposal involves a new or changed API, include a basic code example.
Omit this section if it's not applicable.
如果提案涉及新的或更改的 API，请包含基本代码示例。如果不适用，请省略此部分。

# Motivation    // 动机

Why are we doing this? What use cases does it support? What is the expected
outcome?
我们为什么要这样做呢？它支持哪些用例？预期的结果是什么？

Please focus on explaining the motivation so that if this RFC is not accepted,
the motivation could be used to develop alternative solutions. In other words,
enumerate the constraints you are trying to solve without coupling them too
closely to the solution you have in mind.
请重点解释动机，以便如果不接受此 RFC，则动机可用于开发替代解决方案。
换句话说，列举您尝试解决的约束条件，但不要将它们与您想到的解决方案耦合得太紧密。

# Detailed design   // 详细设计

This is the bulk of the RFC. Explain the design in enough detail for somebody
familiar with Vue to understand, and for somebody familiar with the
implementation to implement. This should get into specifics and corner-cases,
and include examples of how the feature is used. Any new terminology should be
defined here.
这是 RFC 的大部分内容。
足够详细地解释设计，让熟悉 Vue 的人理解，熟悉实现的人去实现。
这应该涉及细节和极端情况，并包括如何使用该功能的示例。
任何新术语都应在此处定义。

# Drawbacks // 缺点

Why should we *not* do this? Please consider:
为什么我们不应该这样做？请考虑：

- implementation cost, both in term of code size and complexity // 代码大小和复杂性方面的实现成本
- whether the proposed feature can be implemented in user space // 提议的功能是否可以在用户空间中实现
- the impact on teaching people Vue // 对学习Vue成本的影响
- integration of this feature with other existing and planned features  // 将此功能与其他现有和计划中的功能集成
- cost of migrating existing Vue applications (is it a breaking change?)    // 迁移现有 Vue 应用程序的成本（这是一个重大变化吗？）

There are tradeoffs to choosing any path. Attempt to identify them here.    // 选择任何路径都需要权衡。尝试在此处识别它们。

# Alternatives  // 备用方案

What other designs have been considered? What is the impact of not doing this?  // 还考虑了哪些其他设计？不这样做有什么影响？

# Adoption strategy     // 采用策略

If we implement this proposal, how will existing Vue developers adopt it? 
Is this a breaking change? 
Can we write a codemod? 
Can we provide a runtime adapter library for the original API it replaces? 
How will this affect other projects in the Vue ecosystem?
如果我们实施这个提议，现有的 Vue 开发者将如何采用它？
这是一个突破性的变化吗？
我们可以写一个codemod吗？
我们可以为它替换的原始 API 提供运行时适配器库吗？
这将如何影响 Vue 生态系统中的其他项目？

# Unresolved questions  // 未解决的问题

Optional, but suggested for first drafts. What parts of the design are still
TBD?
可选，但建议用于初稿。设计的哪些部分仍然待定？