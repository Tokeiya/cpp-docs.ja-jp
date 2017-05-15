---
title: "コンパイラ エラー C3232 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3232
dev_langs:
- C++
helpviewer_keywords:
- C3232
ms.assetid: 3119b3a9-0eff-4a3f-b805-e4d160af9e39
caps.latest.revision: 7
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- ru-ru
- zh-cn
- zh-tw
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
translationtype: Machine Translation
ms.sourcegitcommit: 0d9cbb01d1ad0f2ea65d59334cb88140ef18fce0
ms.openlocfilehash: 3aeccffb4adce417b113d32ba399346ee0454fc2
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c3232"></a>コンパイラ エラー C3232
'param' : ジェネリック型パラメーターは修飾名では使用できません  
  
 ジェネリック型パラメーターが正しく使用されていません。  
  
 次の例では C3232 が生成されます。  
  
```  
// C3232.cpp  
// compile with: /clr  
generic <class T>  
ref class C {  
   typename T::TYPE t;   // C3232  
};  
```