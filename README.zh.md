翻译时间： 2021-12-21
翻译版本号： 1c3edd6fb3cec5786ec528f12960f6749770a5e9 / Evan You / 2021-12-12
# Vue RFCs

## What is an RFC?  // 什么是RFC?

The "RFC" (request for comments) process is intended to provide a
consistent and controlled path for new features to enter the framework.

"RFC"全拼是`request for comments`意思即为请求评议，它存在的意义就是为了新特性纳入框架提供了一个一致且可控的地方

Many changes, including bug fixes and documentation improvements can be
implemented and reviewed via the normal GitHub pull request workflow.

通过github的PR操作，许多包括bugs的修复和文档的改进等变化能够被实施和复审


Some changes though are "substantial", and we ask that these be put
through a bit of a design process and produce a consensus among the Vue
core team and the community.

尽管有些改变是'substantial',我们要求通过一些设计过程来完成并在Vue核心团队和社区中产生一个共识

## The RFC life-cycle   // 一个RFC的生命周期

An RFC goes through the following stages:
一个 RFC 将会经历下列几种阶段：

- **Pending:** when the RFC is submitted as a PR.   // 当这个RFC作为一个PR被提交时
- **Active:** when an RFC PR is merged and undergoing implementation.   // 当一个RFC被合并并且正在被实施时
- **Landed:** when an RFC's proposed changes are shipped in an actual release.  // 当一个RFC提出的改动在一个实际的版本中被实现时
- **Rejected:** when an RFC PR is closed without being merged.  // 当一个RFC的PR被关闭没有给被合并进分支时


[Pending RFC List](https://github.com/vuejs/rfcs/pulls)
所有的RFC列表

## When to follow this process  // 什么时候需要遵循这个流程

You need to follow this process if you intend to make "substantial"
changes to one of the projects listed below:

如果你打算提出一个关于下列项目清单中任一个相关的'substantial'改变，你需要遵循下面这个过程

- [Vue core](https://github.com/vuejs/vue)
- [Vue Router](https://github.com/vuejs/vue-router)
- [Vuex](https://github.com/vuejs/vuex)
- [Vue CLI](https://github.com/vuejs/vue-cli)

We are limiting the RFC process for these repos to test out the process in a more manageable fashion, 
and may expand it to cover more projects under the `vuejs` organization in the future. 
For now, if you wish to suggest changes to those other projects, please use their respective issue lists.
我们正在限制这些repos的RFC流程，以便他们以一种更加便于管理的方式来检验该流程，并可能在未来将其扩展以覆盖`VueJS`组织下更多的项目。
现在，如果你想对其他项目提出更改建议，请使用他们个字的issue lists


What constitutes a "substantial" change is evolving based on community norms, but may include the following:
一个'substantial'改变是基于社区规范而演变的，但可能包括以下内容：

- A new feature that creates new API surface area   // 创建新的API的新特性
- Changing the semantics or behavior of an existing API // 改变一个现有API的语义或行为
- The removal of features that are already shipped as part of the release channel.  // 删除已作为发布渠道的一部分提供的功能
- The introduction of new idiomatic usage or conventions, even if they do not include code changes to Vue itself.
  // 引入新的惯用用法或约定，即使它们不包括对 Vue 本身的代码更改。

Some changes do not require an RFC:
还有一些改变并不能作为RFC：

- Additions that strictly improve objective, numerical quality criteria (speedup, better browser support)   
  // 严格改进客观、数字质量标准的添加项（加速、更好的浏览器支持）
- Fixing objectively incorrect behavior // 修正客观上不正确的行为
- Rephrasing, reorganizing or refactoring   // 改写、重组或者重构现有的代码
- Addition or removal of warnings   // 添加或删除警告
- Additions only likely to be _noticed by_ other implementors-of-Vue, invisible to users-of-Vue.
  // 添加的只会被Vue的实现者注意到而不会被Vue使用者注意到的改动

If you submit a pull request to implement a new feature without going
through the RFC process, it may be closed with a polite request to
submit an RFC first.
如果你提交了一个PR但是没有通过RFC的流程来实施一个新特性，它可能会被关闭，然后要求你先提交一个RFC

## Why do you need to do this   // 为什么你需要做这些

It is great that 
you are considering suggesting new features or changes to Vue - we appreciate your willingness to contribute! 
However, as Vue becomes more widely used, we need to take stability more seriously, 
and thus have to carefully consider the impact of every change we make that may affect end users. 
On the other hand, 
we also feel that Vue has reached a stage where we want to start consciously preventing further complexity from new API surfaces.

很高兴您考虑对 Vue 提出新功能或更改建议 - 我们感谢您愿意做出贡献！
但是，随着 Vue 的使用越来越广泛，我们需要更加重视稳定性，因此必须仔细考虑我们所做的每一个可能影响最终用户的更改的影响。
另一方面，我们也觉得 Vue 已经到了一个阶段，我们希望开始有意识地防止新 API 表面的进一步复杂性。


These constraints and tradeoffs 
may not be immediately obvious to users who are proposing a change just to solve a specific problem they just ran into. 
The RFC process serves as a way to guide you through our thought process when making changes to Vue, 
so that we can be on the same page when discussing why or why not these changes should be made.

对于那些只是为了解决他们刚刚遇到的特定问题而提出更改的用户来说，这些限制和权衡可能不会立即更改。
在对 Vue 进行更改时，RFC 流程可作为指导您完成我们的思考过程的一种方式，这样我们就可以在讨论为什么应该或为什么不应该进行这些更改在同一页面上。

## Gathering feedback before submitting // 提交前先收集反馈

It's often helpful to get feedback on your concept before diving into the level of API design detail required for an RFC. 
**You may open an issue on this repo to start a high-level discussion**, 
with the goal of eventually formulating an RFC pull request with the specific implementation design.

在深入研究 RFC 所需的 API 设计细节级别之前，获得有关您的概念的反馈通常很有帮助。
**你也可以在这个repo打开一个新的issue来开始一个更深层次的讨论**
目标是最终制定一个具有特定实现设计的 RFC-PR


## What the process is  // 流程是什么

In short, to get a major feature added to Vue, one must first get the RFC merged into the RFC repo as a markdown file. 
At that point the RFC is 'active' and may be implemented with the goal of eventual inclusion into Vue.

简而言之，要为 Vue 添加一个主要功能，首先必须将 RFC 作为 Markdown 文件合并到 RFC repo 中。
在那时候 RFC 是“活跃的”，并且可能会以最终包含到 Vue 中的目标来实现。

1.  Work on your proposal in a Markdown file based on the template (`0000-template.md`) found in this repo.
    根据此 repo 中的模板 (`0000-template.md`) 在 Markdown 文件中处理您的提案。

    - Put care into the details:    // 关注这些细节：
        **RFCs that do not present convincing motivation, 
        demonstrate understanding of the impact of the design, 
        or are disingenuous about the drawbacks or alternatives tend to be poorly-received**.
      **没有提出令人信服的动机，没有证明对设计影响的理解，或者对缺点或替代方案不诚实的 RFC 往往不受欢迎**

2.  Open a new thread in [Discussions](https://github.com/vuejs/rfcs/discussions) and make sure to set category to "RFC Discussions".
    在此repo的`Discussions`中新建一个新的Discussions`New discussions`,然后在`Select category`选项中选择`RFC Discussions`

    - Build consensus and integrate feedback in the discussion thread.  // 在`Discussions`中达成共识并整合反馈
      RFCs that have broad support are much more likely to make progress than those that don't receive any comments.
      // 获得广泛支持的 RFC 比那些没有收到任何评论的 RFC 更有可能取得进展。

3.  If the proposal receives non-trivial interest from community members and generally positive feedback, you can prepare a Pull Request:
    如果提案收到社区成员的非凡兴趣和普遍积极的反馈，您可以准备拉取请求：

    - Fork this repo.   // Fork this repo

    - Create your proposal as `active-rfcs/0000-my-feature.md` (where "my-feature" is descriptive. don't assign an RFC number yet).
    - 将您的提案创建为 `active-rfcs0000-my-feature.md`（其中“my-feature”是描述性的。不要分配 RFC 编号）。

    - Submit a pull request. Make sure to link to the discussion thread.    // 提交一个PR。确保链接到讨论线程。

4.  Eventually, the [core team] will decide whether the RFC is a candidate
    for inclusion in Vue.   // 最终，[核心团队] 将决定 RFC 是否是包含在 Vue 中的候选者。

    - An RFC can be modified based upon feedback from the [core team] and community.    // 可以根据 [核心团队] 和社区的反馈修改 RFC。
      Significant modifications may trigger a new final comment period. // 重大修改可能会触发新的最终评论期。

    - An RFC may be rejected after public discussion has settled and comments have been made summarizing the rationale for rejection. 
      A member of the [core team] should then close the RFC's associated pull request.
    - RFC 可能会在公众讨论结束并且评论总结拒绝理由后被拒绝。然后，[核心团队] 的成员应该关闭 RFC 的相关拉取请求。

    - An RFC may be accepted at the close of its final comment period. 
      A [core team] member will merge the RFC's associated pull request, at which point the RFC will become 'active'.
    - RFC 可能会在其最终评论期结束时被接受。 [核心团队] 成员将合并 RFC 的关联拉取请求，此时 RFC 将变为“活动”状态。

## Details on Active RFCs   // 有关活动 RFC 的详细信息

Once an RFC becomes active then authors may implement it and submit the feature as a pull request to the Vue repo. 
Becoming 'active' is not a rubber stamp, and in particular still does not mean the feature will ultimately be merged; 
it does mean that the core team has agreed to it in principle and are amenable to merging it.
一旦 RFC 变为活动状态，作者就可以实现它并将该功能作为拉取请求提交给 Vue 存储库。
变得“活跃”并不是板上钉钉，仍然不意味着该功能最终会被合并；
这只是意味着核心团队原则上同意并愿意合并


Furthermore, 
the fact that a given RFC has been accepted and is'active' implies nothing about what priority is assigned to its implementation, 
nor whether anybody is currently working on it.
此外，给定的 RFC 已被接受并处于“活动状态”这一事实并不意味着为其实施分配了何种优先级，也并不意味着目前是否有人正在致力于此。

Modifications to active RFC's can be done in followup PR's. 
We strive to write each RFC in a manner that it will reflect the final design of the feature; 
but the nature of the process means that 
we cannot expect every merged RFC to actually reflect what the end result will be at the time of the next major release; 
therefore we try to keep each RFC document somewhat in sync with the language feature as planned, 
tracking such changes via followup pull requests to the document.
对活动 RFC 的修改可以在后续 PR 中完成。
我们努力以反映功能最终设计的方式编写每个 RFC；
但是这个过程的性质意味着我们不能期望每个合并的 RFC 都能真正反映下一个主要版本发布时的最终结果；
因此，我们尝试按计划使每个 RFC 文档与语言功能保持一定程度的同步，并通过对文档的后续拉取请求来跟踪此类更改。

## Implementing an RFC  // 实施一个RFC

The author of an RFC is not obligated to implement it.  // RFC的作者并没有义务去实现它
Of course, the RFC author (like any other developer) is welcome to post an implementation for review after the RFC has been accepted.
当然，在 RFC 被接受后，欢迎 RFC 作者（与任何其他开发人员一样）发布实现以供审查。

An active RFC should have the link to the implementation PR listed if there is one.   // 一个活跃的 RFC 应该有一个链接到实现 PR 列出（如果有的话）。
Feedback to the actual implementation should be conducted in the implementation PR instead of the original RFC PR.
对实际实现的反馈应该在实现 PR 中而不是原始 RFC PR 中进行。

If you are interested in working on the implementation for an 'active' RFC, // 如果您对“活跃”RFC 的实施感兴趣，
but cannot determine if someone else is already working on it, feel free to ask (e.g. by leaving a comment on the associated issue).
但无法确定其他人是否已经在处理它，请随时提issue（例如，对相关问题发表评论）。

## Reviewing RFC's  // 审查RFC's

Members of the [core team] will attempt to review some set of open RFC pull requests on a regular basis. 
If a core team member believes an RFC PR is ready to be accepted into active status, 
they can approve the PR using GitHub's review feature to signal their approval of the RFC.
[核心团队] 的成员将尝试定期审查一些开放的 RFC 拉取请求。
如果核心团队成员认为 RFC PR 已准备好被接受为活动状态，
他们可以使用 GitHub 的审查功能批准 PR，以表示他们批准了 RFC。

**Vue's RFC process owes its inspiration to the [React RFC process], [Rust RFC process] and [Ember RFC process]**

[react rfc process]: https://github.com/reactjs/rfcs
[rust rfc process]: https://github.com/rust-lang/rfcs
[ember rfc process]: https://github.com/emberjs/rfcs
[core team]: https://vuejs.org/v2/guide/team.html
