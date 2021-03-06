---
title: "コンパイラ エラー C2743 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2743
dev_langs:
- C++
helpviewer_keywords:
- C2743
ms.assetid: 644cd444-21d2-471d-a176-f5f52c5a0b73
caps.latest.revision: 8
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: f45e7617bbf162c23994897c42aab44abeacea88
ms.contentlocale: ja-jp
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c2743"></a>コンパイラ エラー C2743
'type': _ _clrcall デストラクターまたはコピー コンス トラクターを持つネイティブ型をキャッチできません  
  
 コンパイルされたモジュール**/clr**のネイティブ型と型のデストラクターまたはコピー コンス トラクターで使用されている例外をキャッチしようとしています。`__clrcall`呼び出し規約です。  
  
 コンパイルしたときに**/clr**、例外処理には、メンバー関数は、ネイティブ型にするが必要ですが[_ _cdecl](../../cpp/cdecl.md)および not [_ _clrcall](../../cpp/clrcall.md)です。 使用してメンバー関数を持つネイティブ型`__clrcall`でコンパイルされたモジュールの呼び出し規約をキャッチできない**/clr**です。  
  
 詳細については、「[/clr (共通言語ランタイムのコンパイル)](../../build/reference/clr-common-language-runtime-compilation.md)」を参照してください。  
  
## <a name="example"></a>例  
 次の例では、C2743 を生成します。  
  
```  
// C2743.cpp  
// compile with: /clr  
public struct S {  
   __clrcall ~S() {}  
};  
  
public struct T {  
   ~T() {}  
};  
  
int main() {  
   try {}  
   catch(S) {}   // C2743  
   // try the following line instead  
   // catch(T) {}  
  
   try {}  
   catch(S*) {}   // OK  
}  
```
