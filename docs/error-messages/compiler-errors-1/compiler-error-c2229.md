---
title: "コンパイラ エラー C2229 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C2229"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2229"
ms.assetid: 933c7cf2-a463-4e74-b0b4-59dedad987fb
caps.latest.revision: 10
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 10
---
# コンパイラ エラー C2229
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

type 'identifier'' にサイズが 0 の配列があります。  
  
 構造体またはビット フィールドのメンバーに、最後のメンバーではないサイズ 0 の配列が含まれています。  
  
 サイズ 0 の配列は構造体の最後のメンバーにできますが、構造体を割り当てるときにそのサイズを指定する必要があります。  
  
 サイズ 0 の配列が構造体の最後のメンバーではない場合、コンパイラは、残りのフィールドのオフセットを計算できません。  
  
 次の例では警告 C2229 が生成されます。  
  
```  
// C2229.cpp  
struct S {  
   int a[0];  // C2229  zero-sized array  
   int b[1];  
};  
  
struct S2 {  
   int a;  
   int b[0];  
};  
  
int main() {  
   // allocate 7 elements for b field  
   S2* s2 = (S2*)new int[sizeof(S2) + 7*sizeof(int)];  
   s2->b[6] = 100;  
}  
```