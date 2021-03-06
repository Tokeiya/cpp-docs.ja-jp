---
title: "コンパイラの警告 C4439 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C4439
dev_langs:
- C++
helpviewer_keywords:
- C4439
ms.assetid: 9449958f-f407-4824-829b-9e092f2af97d
caps.latest.revision: 6
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: eec228922a6f5796587243fe2d1f2c6cc1cf6b1c
ms.contentlocale: ja-jp
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-warning-c4439"></a>コンパイラの警告 C4439
'function': シグネチャのマネージ型を伴う関数定義は _ _clrcall 呼び出し規約を持つ必要があります  
  
 コンパイラでは、呼び出し規約を暗黙的に置き換えられます[_ _clrcall](../../cpp/clrcall.md)です。 この警告を解決するには、削除、`__cdecl`または`__stdcall`呼び出し規約です。  
  
 C4439 は常に、エラーとして発行されます。 この警告をオフにすることができます、`#pragma warning`または**/wd**; を参照してください[警告](../../preprocessor/warning.md)または[/w、/W0、/W1、/W2、/W3、/W4、/w1、/w2、/w3、/w4、/Wall、/wd、//wo、/Wv、/WX (警告レベル)](../../build/reference/compiler-option-warning-level.md)詳細についてはします。  
  
## <a name="example"></a>例  
 次の例では、C4439 を生成します。  
  
```  
// C4439.cpp  
// compile with: /clr  
void __stdcall f( System::String^ arg ) {}   // C4439  
void __clrcall f2( System::String^ arg ) {}   // OK  
void f3( System::String^ arg ) {}   // OK  
```
