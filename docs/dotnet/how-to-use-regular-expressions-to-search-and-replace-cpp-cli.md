---
title: "方法: 正規表現の検索し、置換を使用 (C + + CLI) |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- search and replace
- Replace method
- regular expressions [C++], search and replace
ms.assetid: 12fe3e18-fe10-4b25-a221-19dc5eab3821
caps.latest.revision: "8"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 17710654b0af2e03019a1e7b888d86e42c5e35c9
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="how-to-use-regular-expressions-to-search-and-replace-ccli"></a>方法: 正規表現を使用して検索と置換を行う (C++/CLI)
次のコード例を示す方法、正規表現クラス<xref:System.Text.RegularExpressions.Regex>検索と置換を実行するために使用できます。 これは、<xref:System.Text.RegularExpressions.Regex.Replace%2A>メソッドです。 使用されているバージョンは 2 つの文字列を入力として受け取ります: 変更するには、文字列と (もしあれば) セクションでは、代わりに挿入する文字列に指定されたパターンに一致する、<xref:System.Text.RegularExpressions.Regex>オブジェクト。  
  
 このコードでは、文字列内のすべての桁をアンダー スコア (_) に置き換え、空の文字列、実質的に削除することでそれらを置き換えます。 シングル ステップでは、同じ効果を実現できますが、2 つの手順は、デモンストレーションのためここでも使用されます。  
  
## <a name="example"></a>例  
  
```  
// regex_replace.cpp  
// compile with: /clr  
#using <System.dll>  
using namespace System::Text::RegularExpressions;  
using namespace System;  
  
int main()  
{  
   String^ before = "The q43uick bro254wn f0ox ju4mped";  
   Console::WriteLine("original  : {0}", before);  
  
   Regex^ digitRegex = gcnew Regex("(?<digit>[0-9])");  
   String^ after = digitRegex->Replace(before, "_");  
   Console::WriteLine("1st regex : {0}", after);  
  
   Regex^ underbarRegex = gcnew Regex("_");  
   String^ after2 = underbarRegex->Replace(after, "");  
   Console::WriteLine("2nd regex : {0}", after2);  
  
   return 0;  
}  
```  
  
## <a name="see-also"></a>関連項目  
 [.NET Framework 正規表現](/dotnet/standard/base-types/regular-expressions)   
 [C++/CLI (Visual C++) による .NET プログラミング](../dotnet/dotnet-programming-with-cpp-cli-visual-cpp.md)