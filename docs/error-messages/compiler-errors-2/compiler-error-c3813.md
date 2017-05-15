---
title: "コンパイラ エラー C3813 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C3813
dev_langs:
- C++
helpviewer_keywords:
- C3813
ms.assetid: ffdbc489-71bf-4cd6-988c-f824c9ab3ceb
caps.latest.revision: 10
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
translationtype: Machine Translation
ms.sourcegitcommit: 65e7a7bd56096fbeec61b651ab494d82edef9c90
ms.openlocfilehash: 74c976fb090533ade91e5debf067371d5d3295c1
ms.lasthandoff: 02/24/2017

---
# <a name="compiler-error-c3813"></a>コンパイラ エラー C3813
プロパティ宣言はマネージ型または WinRT 型の定義内でのみ使用できます  
  
A[プロパティ](../../dotnet/how-to-use-properties-in-cpp-cli.md)マネージまたは Windows ランタイム内でのみ宣言可能型です。 ネイティブ型では、`property` キーワードがサポートされていません。  
  
## <a name="example"></a>例  
次の例では、C3813 を生成し、その修正方法を示しています。  
  
```cpp  
// C3813.cpp  
// compile by using: cl /c /clr C3813.cpp  
class A  
{  
   property int Int; // C3813  
};  
  
ref class B  
{  
   property int Int; // OK - declared within managed type  
};  
```