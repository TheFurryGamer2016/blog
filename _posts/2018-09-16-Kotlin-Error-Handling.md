---
layout: post
title: Kotlin Error Handling
date: 2018-09-16 13:10 -0400
---


At work, I write software in [Swift](https://Swift.org). In my personal projects, I write in [Kotlin](https://KotlinLang.org).  I found Kotlin because I wanted a way to write Swift on the JVM, and was told that Kotlin is quite similar. And that it is! But there are many key differences that, I think, make Swift just barely edge out Kotlin as the better of the two.

Today, the difference in question is error<sup>[*](#errors-are-exceptions-in-this-post)</sup> handling. Kotlin has none! Well, to be clear, Kotlin lets you _handle_ errors, but it doesn't let you know when they might or might not be thrown. In contrast, Swift forces you to explicitly handle how and where errors are thrown.

There are Kotlin libraries, like [Arrow](https://arrow-kt.io/), that attempt to add this missing functionality ([`Try` for Arrow](https://arrow-kt.io/docs/datatypes/try/)).



---

<aside>
    <ul>
        <li id="errors-are-exceptions-in-this-post" style="list-style-type:'*'">In this post, I use "error" as a storthand for all checked exceptions. That is, Kotlin's [`Throwable`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/)s that don't extend [`RuntimeException`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-runtime-exception/), and Swift's [`Error`](https://developer.apple.com/documentation/swift/error)s</li>
    </ul>
</aside>
