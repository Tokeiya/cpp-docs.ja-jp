---
title: "コンパイラ エラー C3809 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C3809
dev_langs:
- C++
helpviewer_keywords:
- C3809
ms.assetid: 37eca584-c20c-464e-8e45-a987214b7ce4
caps.latest.revision: 9
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: e68e6f3b1309a0135b439bfe8f3f067a0c90a6ac
ms.contentlocale: ja-jp
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c3809"></a>コンパイラ エラー C3809
'class' : マネージ型または WinRT 型にフレンド関数、クラス、インターフェイスを含めることはできません。  
  
 マネージ型と Windows ランタイム型では、フレンドは許可されません。 このエラーを修復するには、マネージ型または Windows ランタイム型内でフレンドを宣言しないようにします。  
  
 次の例では、C3809 エラーが生成されます。  
  
```  
// C3809a.cpp  
// compile with: /clr  
ref class A {};  
  
ref class B  
{  
public:  
   friend ref class A;   // C3809  
};  
  
int main()  
{  
}  
```
