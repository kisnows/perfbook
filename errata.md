## 勘误

- XI 页

`笔者在优化过程中常常根据有趣的知识来梳理思路` 应该修改为 `笔者在性能优化和整理相关思路的过程中常常遇到很多有趣的知识`。

- 18 页

`所以“盲目”优化是万恶之源` 应该修改为 `“盲目优化”才是万恶之源`。

- 18 页

在开头应该补充下面的内容

```
> 过早优化是万恶之源

这句话出自于 Donald Knuth 的《计算机编程艺术》，原话是

> We should forget about small efficiencies, say about 97% of the time: premature optimization is the root of all evil. Yet we should not pass up our opportunities in that critical 3%.
> 我们应该忘记小的效率，比如大约 97% 的时间：过早优化是万恶之源。然而，我们不应该放弃那关键的 3% 的机会。
```

- 49 页

`可以使用一些优化手段让 First Byte 刻意大一些` 改为 `有些优化手段会使得 First Byte 更晚一些`。

- 207 页补充段落在 `小结` 前

需要注意的是，使用 ServiceWorker 并不代表能给性能带来直接的提升。事实上 ServiceWorker 之所以可以被用于改善性能，是因为 ServiceWorker 提供了更加灵活的缓存和预缓存策略，使得我们可以在一些 HTTP 缓存无法满足使用条件的场景使用缓存和预缓存的能力，从而带来性能的提升，而并非因为 ServiceWorker 本身。

事实上，单纯的引入 ServiceWorker 因为增加本身的网络请求、增加冷启动和使用逻辑反而会带来一些性能上的负担。所以在 HTTP 缓存能够满足需求的场景，引入 ServiceWorker 替代原有的 HTTP 缓存是没有必要的。


- 176 页，`宏任务` 描述不精确，在整个章节中都应该替换为 `任务`，同时补充以下内容


注：也有一些文章或书籍将任务（Task）称为宏任务（MacroTask）用于和微任务（MicroTask）区分，但事实上在 W3C 标准中只有任务和微任务，并没有宏任务这样的名称。


- 181 页，应该为 `涉及` 而不是 `设计`
- 181 页补充说明


虽然本节以 Promise Polyfill 为例讲解了采取任务和微任务对于性能的影响，但并非所有的 Promise Polyfill 的性能都存在问题，事实上只要采取正确的方式实现，例如在老版本浏览器中采用 Mutation Observer 模拟，Promise Polyfill 的性能并不会和浏览器原生的 Promise 实现存在明显差异。

- 第 19 章应该命名为 `跨端技术与性能`
- 第 6 篇应该命名为 `泛前端技术与性能`