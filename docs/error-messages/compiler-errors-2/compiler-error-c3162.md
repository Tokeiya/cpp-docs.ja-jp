---
title: "コンパイラ エラー C3162 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C3162
dev_langs: C++
helpviewer_keywords: C3162
ms.assetid: 0d4c4a24-1456-4191-b7d8-c38cb7b17c32
caps.latest.revision: "4"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 8bfde260ef0efe58ed70469a80a8bf7316eefa46
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-error-c3162"></a>コンパイラ エラー C3162
'type': デストラクターを含む参照型は静的データ メンバー 'member' の型として使用することはできません  
  
 共通言語ランタイムは、クラスには、静的メンバー関数も含まれている場合は、ユーザー定義のデストラクターを実行するタイミングを知ることはできません。  
  
 オブジェクトが明示的に削除しない限り、デストラクターは実行されません。  
  
 詳細については、次のトピックを参照してください。  
  
-   [/clr (共通言語ランタイムのコンパイル)](../../build/reference/clr-common-language-runtime-compilation.md)  
  
-   [Visual C++ の 64 ビットへの移行に関する一般的な問題](../../build/common-visual-cpp-64-bit-migration-issues.md)  
  
## <a name="example"></a>例  
 次の例では、C3162 を生成します。  
  
```  
// C3162.cpp  
// compile with: /clr /c  
ref struct A {  
   ~A() { System::Console::WriteLine("in destructor"); }  
   static A i;   // C3162  
   static A^ a = gcnew A;   // OK  
};  
  
int main() {  
   A ^ a = gcnew A;  
   delete a;  
}  
```