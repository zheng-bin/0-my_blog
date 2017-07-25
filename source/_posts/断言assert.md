---
title: 断言assert
date: 2015-07-25 21:33:09
tags:
  - C++
  - assert
---

# assert()
* 程序一般分为 Debug 版本和 Release 版本，Debug 版本用于内部调试，Release 版本发行给用户使用。
* 断言 assert 是仅在 Debug 版本起作用的宏，它用于检查“不应该”发生的情况。

eg:内存赋值函数
```
void *memcpy(void *pvTo, const void *pvFrom, size_t size)
{
    assert((pvTo != NULL) && (pvFrom != NULL)); // 使用断言

    byte *pbTo = (byte *) pvTo;  // 防止改变 pvTo 的地址
    byte *pbFrom = (byte *) pvFrom;  // 防止改变 pvFrom 的地址

    while(size -- > 0 )
        *pbTo ++ = *pbFrom ++ ;

    return pvTo;
}
```

* 如果程序在 assert 处终止了，并不是说含有该处终止了，并不是说含有该 assert  的函数有错误，而是调用者出了差错，assert 可以帮助我们找到发生错误的原因。
