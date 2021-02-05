---
title: 'javaScript EventLoop 运行顺序'
date: 2021-02-05 17:39:38
tags: []
published: true
hideInList: false
feature: 
isTop: false
---
javaScript是一门单线程语言就是运用EventLoop 来决定事物运行的顺序的顺序.
js执行代码分为同步和异步,进程会优先执行同步代码,之后轮询任务队列,但当异步代码执行完后会优先执行同步代码,再次轮询任务队列,直至所有任务都执行完成.
**使用异步的好处是你只需要设置好异步的触发条件就可以去干别的事情了，所以异步不会阻塞主干上事件的执行。特别是对于JS这种只有一个线程的语言，如果都像我们第一个例子那样去while(true)，那浏览器就只有一直卡死了，只有等这个循环运行完才会有响应。**
![](https://webopener.github.io/post-images/1612520265363.bmp)