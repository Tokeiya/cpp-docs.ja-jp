---
title: "DLL インポートおよびエクスポート関数 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-language
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- DLLs [C++], importing
- dllimport attribute [C++], storage-class attribute
- DLL exports [C++]
- declaring functions, with dllexport and dllimport
- extended storage-class attributes
- dllexport attribute [C++], storage-class attribute
ms.assetid: 08d164b9-770a-4e14-afeb-c6f21d9e33e4
caps.latest.revision: "9"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 78d1dacd764a7d171c9cacb54a64fab241f8603a
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="dll-import-and-export-functions"></a>DLL インポートおよびエクスポート関数
**Microsoft 固有の仕様**  
  
 このトピックの最も完全な最新情報は「[dllexport、dllimport](../cpp/dllexport-dllimport.md)」で確認できます。  
  
 **dllimport** および `dllexport` ストレージ クラス修飾子は C 言語への Microsoft 固有の拡張です。 これらの修飾子は、クライアント (実行可能ファイルまたは別の DLL) に DLL のインターフェイスを明示的に定義します。 関数を `dllexport` として宣言すると、モジュール定義 (.DEF) ファイルが不要になります。 また、データとオブジェクトに対して **dllimport** および `dllexport` 修飾子を使用することもできます。  
  
 **dllimport** および `dllexport` ストレージ クラス修飾子は、この例に示すように拡張属性構文のキーワード、`__declspec` と共に使用する必要があります。  
  
```  
#define DllImport   __declspec( dllimport )  
#define DllExport   __declspec( dllexport )  
  
DllExport void func();  
DllExport int i = 10;  
DllExport int j;  
DllExport int n;  
```  
  
 拡張ストレージ クラス修飾子の構文に関する具体的な情報については、「[拡張ストレージ クラス属性](../c-language/c-extended-storage-class-attributes.md)」を参照してください。  
  
 **END Microsoft 固有の仕様**  
  
## <a name="see-also"></a>関連項目  
 [C 関数の定義](../c-language/c-function-definitions.md)