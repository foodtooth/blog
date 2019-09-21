+++ 
draft = true
date = 2019-09-20T04:01:13-04:00
title = "Detailed explanation of thread pool in C++"
description = ""
slug = "" 
tags = ["c++","thread pool"]
categories = ["c++"]
externalLink = ""
series = []
+++

## 关于[Thread pool][Thread pool wiki]

> In computer programming, a thread pool is a software design pattern for achieving concurrency of execution in a computer program. Often also called a replicated workers or worker-crew model, a thread pool maintains multiple threads waiting for tasks to be allocated for concurrent execution by the supervising program.

它有以下几个关注点：

1. Thread pool会管理数个thread
1. 对thread的管理包括了，
    1. 对thread总个数的把控
    1. thread创建后不会主动销毁，而是在“执行task”、“等待task”等状态中切换
1. 它的基本运作模式为producer-consumer pattern，即：
    1. 维护一个task queue，包含所有待执行的任务
    1. 维护一个thread pool，由等待task状态的线程执行task queue中的task
1. 通过C++11的future特性，从已执行的任务中返回结果
1. Task（任务）可以是任何的Function objects
1. 可用atomic特性保证对task queue操作的线程同步，同时用bounded queue的概念达到对内存使用的限制

## Detailed explanation
我们可以从Thread pool的基本概念中，抽取以下基本的轮廓：

```cpp
namespace thread_pool {

class BoundedQueue {
};

class ThreadPool {
 private:
  std::vector<std::thread> pool_(std::thread::hardware_concurrency());
  BoundedQueue task_queue_;
};

}  // namespace thread_pool
```

[Thread pool wiki]: https://en.wikipedia.org/wiki/Thread_pool