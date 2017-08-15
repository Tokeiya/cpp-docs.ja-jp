---
title: "コンパイラ エラー C2815 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2815
dev_langs:
- C++
helpviewer_keywords:
- C2815
ms.assetid: d0256fd6-0721-4c99-b03c-52d96e77a613
caps.latest.revision: 9
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
ms.translationtype: Machine Translation
ms.sourcegitcommit: 66798adc96121837b4ac2dd238b9887d3c5b7eef
ms.openlocfilehash: 7cd85d29ee14376b46d05ac5cfa95496fffdc9e5
ms.contentlocale: ja-jp
ms.lasthandoff: 04/29/2017

---
# <a name="compiler-error-c2815"></a>{1&gt;コンパイラ エラー C2815&lt;1}
'operator delete': 仮引数の最初のパラメーターである必要があります ' void *'、'param' が使用されましたが、  
  
 ユーザー定義[演算子 delete](../../standard-library/new-operators.md#op_delete)関数は、型の最初の仮パラメーターを受け取る必要があります`void *`です。  
  
 次の例では、C2815 が生成されます。  
  
```  
// C2815.cpp  
// compile with: /c  
class CMyClass {  
public:  
   void mf1(int *a);  
   void operator delete(CMyClass *);   // C2815  
   void operator delete(void *);   
};  
```