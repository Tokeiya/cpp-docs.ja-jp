---
title: "コンパイラの警告 (レベル 1) C4905 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C4905"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C4905"
ms.assetid: 40240bf4-b14e-4c22-aeb2-52f2851532f6
caps.latest.revision: 8
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 8
---
# コンパイラの警告 (レベル 1) C4905
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'LPSTR' にキャストされた幅の広いリテラル文字列  
  
 認識できないキャストが見つかりました。  キャストは成功しましたが、変換ルーチンを使用する必要があります。  
  
 既定では、この警告はオフに設定されています。  詳細については、「[Compiler Warnings That Are Off by Default](../Topic/Compiler%20Warnings%20That%20Are%20Off%20by%20Default.md)」を参照してください。  
  
## 使用例  
 次の例では C4905 エラーが生成されます。  
  
```  
// C4905.cpp  
// compile with: /W1  
#pragma warning(default : 4905)  
#include <windows.h>  
#include <stdlib.h>  
#include <stdio.h>  
  
int main()  
{  
    LPSTR y = (LPSTR)L"1234";   // C4905  
  
    // try the following lines instead  
    // wchar_t y[128];  
    // size_t  sizeOfConverted;  
    // errcode err = 0;  
    //  
    // err = mbstowcs_s(&sizeOfConverted, &y[0], 128, "12345", 4);  
    // if (err != 0)  
    // {  
    //     printf_s("mbstowcs_s failed!");  
    //     exit (-1);  
    // }  
    // wprintf(L"%s\n", y);  
  
    return 0;  
}  
```