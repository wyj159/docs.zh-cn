---
title: 对分组操作执行子查询（C# 中的 LINQ）
description: 如何使用 C# 中的 LINQ 对分组操作执行子查询。
ms.date: 12/1/2016
ms.assetid: d75a588e-9b6f-4f37-b195-f99ec8503855
ms.openlocfilehash: 514db81b80557a3026589f00177910cc9446c0f4
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2018
ms.locfileid: "47193468"
---
# <a name="perform-a-subquery-on-a-grouping-operation"></a>对分组操作执行子查询

本文演示创建查询的两种不同方式，此查询将源数据排序成组，然后分别对每个组执行子查询。 每个示例中的基本方法是使用名为 `newGroup` 的“接续块”对源元素进行分组，然后针对 `newGroup` 生成新的子查询。 针对由外部查询创建的每个新组运行此子查询。 请注意，在此特定示例中，最终输出不是组，而是一系列匿名类型。  
  
有关如何分组的详细信息，请参阅 [group 子句](../language-reference/keywords/group-clause.md)。  
  
有关接续块的详细信息，请参阅 [into](../language-reference/keywords/into.md)。 下面的示例使用内存数据结构作为数据源，但相同的原则适用于任何类型的 LINQ 数据源。  
  
## <a name="example"></a>示例

> [!NOTE]
> 此示例包含对[查询对象集合](query-a-collection-of-objects.md)内示例代码中所定义对象的引用。

[!code-csharp[csProgGuideLINQ#23](~/samples/snippets/csharp/concepts/linq/how-to-perform-a-subquery-on-a-grouping-operation_1.cs)]  

## <a name="see-also"></a>请参阅

- [语言集成查询 (LINQ)](index.md)
