---
title: "可変個の引数リストを取る関数 (C++) | Microsoft Docs"
ms.custom: ""
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "引数リスト [C++], 可変数の"
  - "引数 [C++], 可変数の"
  - "宣言子, 関数"
  - "宣言 (関数を), 変数"
  - "関数呼び出し, 可変数の引数"
  - "可変個引数リスト"
ms.assetid: 27c2f83a-21dd-44c6-913c-2834cb944703
caps.latest.revision: 16
caps.handback.revision: 16
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# 可変個の引数リストを取る関数 (C++)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

最後のメンバーが省略記号 \(...\) である関数宣言は、可変数の引数を受け取ることができます。  このような場合、C\+\+ は、明示的に宣言された引数に対してのみ型チェックを行います。  引数の数や型も変わるほどの汎用関数を作成する必要がある場合は、可変個引数リストを使用できます。  ファミリの関数は、可変個引数リストを使用する関数の例です。`printf`*argument\-declaration\-list*  
  
## 可変個の引数を取る関数  
 宣言した後の引数にアクセスするには、以下に示すように、標準インクルード ファイル STDARG.H に含まれているマクロを使用します。  
  
 **Microsoft 固有の仕様 →**  
  
 Microsoft C\+\+ では、省略記号が最後の引数であり、省略記号の前にコンマにある場合、省略記号を引数として指定できます。  したがって、宣言 `int Func( int i, ... );` は有効ですが、`int Func( int i ... );` は有効ではありません。  
  
 **END Microsoft 固有の仕様**  
  
 可変個の引数を受け取る関数の宣言には、使用しない場合でも、少なくとも 1 つのプレースホルダー引数が必要です。  このプレースホルダー引数が指定されていない場合、残りの引数にアクセスする方法はありません。  
  
 `char` 型の引数が可変個の引数として渡される場合は、`int` 型に変換されます。  同様に、**float** 型の変数が可変個の引数として渡される場合は、**double** 型に変換されます。  他の型の引数は、通常の整数および浮動小数点の上位変換を受ける可能性があります。  詳細については、「[整数の上位変換](../misc/integral-promotions.md)」を参照してください。  
  
 変数リストを必要とする関数は、引数リストで省略記号 \(...\) を使用して宣言されます。  変数リストによって渡された引数にアクセスするには、STDARG.H インクルード ファイル内に記述された型とマクロを使用します。  これらのマクロの詳細については、「[va\_arg、va\_copy、va\_end、va\_start](../c-runtime-library/reference/va-arg-va-copy-va-end-va-start.md)」を参照してください。  これは、C ランタイム ライブラリのドキュメントにあります。  
  
 次の例で、マクロが型 \(STDARG.H で宣言\) とどのように協働するかを示します: `va_list` `va_end` `va_arg` `va_start`  
  
```  
// variable_argument_lists.cpp  
#include <stdio.h>  
#include <stdarg.h>  
  
//  Declaration, but not definition, of ShowVar.  
void ShowVar( char *szTypes, ... );  
int main() {  
   ShowVar( "fcsi", 32.4f, 'a', "Test string", 4 );  
}  
  
//  ShowVar takes a format string of the form  
//   "ifcs", where each character specifies the  
//   type of the argument in that position.  
//  
//  i = int  
//  f = float  
//  c = char  
//  s = string (char *)  
//  
//  Following the format specification is a variable   
//  list of arguments. Each argument corresponds to   
//  a format character in the format string to which   
// the szTypes parameter points   
void ShowVar( char *szTypes, ... ) {  
   va_list vl;  
   int i;  
  
   //  szTypes is the last argument specified; you must access   
   //  all others using the variable-argument macros.  
   va_start( vl, szTypes );  
  
   // Step through the list.  
   for( i = 0; szTypes[i] != '\0'; ++i ) {  
      union Printable_t {  
         int     i;  
         float   f;  
         char    c;  
         char   *s;  
      } Printable;  
  
      switch( szTypes[i] ) {   // Type to expect.  
         case 'i':  
            Printable.i = va_arg( vl, int );  
            printf_s( "%i\n", Printable.i );  
         break;  
  
         case 'f':  
             Printable.f = va_arg( vl, double );  
             printf_s( "%f\n", Printable.f );  
         break;  
  
         case 'c':  
             Printable.c = va_arg( vl, char );  
             printf_s( "%c\n", Printable.c );  
         break;  
  
         case 's':  
             Printable.s = va_arg( vl, char * );  
             printf_s( "%s\n", Printable.s );  
         break;  
  
         default:  
         break;  
      }  
   }  
   va_end( vl );  
}  
//Output:   
// 32.400002  
// a  
// Test string  
```  
  
 前の例は、次のような重要な概念を示しています。  
  
1.  いずれかの可変個引数がアクセスされる前に、型 `va_list` の変数としてリスト マーカーを確立する必要があります。  前の例では、マーカーは `vl` と呼ばれます。  
  
2.  個々の引数は `va_arg` マクロを使用してアクセスします。  スタックから正しいバイト数を転送できるように、取得する引数の型を `va_arg` マクロで指定する必要があります。  呼び出し元プログラムによって `va_arg` に指定された型とは異なるサイズの正しくない型を指定した場合、結果は予測不能となります。  
  
3.  `va_arg` マクロを使用して取得した結果を、必要な型に明示的にキャストする必要があります。  
  
 マクロを呼び出して、可変個引数の処理を終了する必要があります。`va_end`