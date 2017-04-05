---
layout: post
title: C#OOP第三章 泛型集合简介
categories:
- 教学笔记
- S2
- C# OOP
permalink: c_oop/3
---

---

##### **泛型集合作为C#常用的数据存储容器，在实际开发中的地位非常重要。本次笔记主要内容为 集合的声明与常用方法列表。**

---

<!-- more -->


### 集合的使用

---

#### 声明:

`List<数据类型> 集合名称= new List<数据类型>();`

---

#### 方法列表：

`Add(T t)`  添加元素到集合的末尾

`Insert(int index , T t)` 添加元素到指定的位置。之后的元素自动后移。

`Any(lambda 表达式)` / `Exists(lambda)` 判断 集合中是否有元素 满足 条件，有 返回 T ，否则返回F.

`AddRange(另一个集合/数组)`  将另一个集合/数组 整体追加到当前集合的末尾。

`All(lambda 表达式)` 判断集合中是否所有元素都满足条件，如果是 则返回T ，否则返回F。

`Average(元素=>元素.属性)` 计算集合中元素 指定的 属性的平均值.

`Clear()` 清空元素。

`集合1.Concat(集合2/数组)` 将两个集合/数组进行拼接，返回IEnumable<T>类型结果。

`XXX.ToList()` 将xxx 转换为 集合  (IEnumable<T> , 数组， 集合)

`Contains(T t)` 判断集合中是否包含指定元素。如果包含返回T 否则返回F。

`Count(lambda 表达式)` 统计集合中满足条件的元素的个数。

`ElementAtOrDefault(int index)` 返回指定索引处元素，如果索引超出范围，返回元素的默认值。

`Find(lambda 表达式)` 返回集合中第一个满足条件的元素。如果没有则返回 元素的默认值。

`FindLast(lambda 表达式)` 返回集合中最后一个满足条件的元素。如果没有则返回 元素的默认值。

`FindAll(lambda 表达式)`/ `Where(lambda 表达式)` 返回集合中所有满足条件的元素。形成新的集合。

`FindIndex(lambda 表达式)` 返回集合中第一个满足条件元素的 下标。

`FindLastIndex(lambda 表达式)` 返回集合中最后一个满足条件元素的 下标。

`First(lambda 表达式)` 返回集合第一个满足条件的元素，如果有返回，否则抛出异常

`First()` 返回集合的第一个元素，如果没有，则抛出异常。

`FirstOrDefault(lambda 表达式)` 作用 同 Find 一样.

`FirstOrDefault()` 返回集合第一个元素 ， 如果没有元素则返回集合元素的默认值。

`GetRange(int index ,int count)` 从原有集合中指定的索引开始，复制 count个元素到新的集合。

`InsertRange(int index,集合/数组)` 在集合指定位置，插入另一个集合/数组.

`Last(lambda 表达式)` 返回集合最后一个满足条件的元素，如果有返回，否则抛出异常

`Last()` 返回集合的最后一个元素，如果没有，则抛出异常。

`Remove(元素)` 删除指定的元素。

`RemoveAt(int index)` 删除指定索引的元素。如果索引超出范围，抛出异常。

`RemoveAll(lambda )` 删除满足条件的元素

`RemoveRange(int index,int count)` 从指定位置删除 指定个数的元素，如果个数超过集合数量，则抛出异常。

`Reverse()` 集合元素翻转

`Reverse(int index ,int count)` 从指定位置开始，反转count 个元素。
