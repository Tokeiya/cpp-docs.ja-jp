---
title: "dllexport、dllimport |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-language
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- dllimport_cpp
- dllexport_cpp
dev_langs:
- C++
helpviewer_keywords:
- dllexport __declspec keyword
- __declspec keyword [C++], dllexport
- dllimport __declspec keyword
- __declspec keyword [C++], dllimport
ms.assetid: ff95b645-ef55-4e72-b848-df44657b3208
caps.latest.revision: 13
author: mikeblome
ms.author: mblome
manager: ghogen
ms.translationtype: HT
ms.sourcegitcommit: 6ffef5f51e57cf36d5984bfc43d023abc8bc5c62
ms.openlocfilehash: 029f5b915b71395f81ada2e2174eafeb59230443
ms.contentlocale: ja-jp
ms.lasthandoff: 09/25/2017

---
# <a name="dllexport-dllimport"></a>dllexport、dllimport
**Microsoft 固有の仕様**  
  
 `dllexport`と**dllimport**ストレージ クラス属性は C および C++ 言語に Microsoft に固有の拡張機能です。 それらの属性を使用すると、関数、データ、オブジェクトを DLL との間でエクスポートおよびインポートできます。  
  
## <a name="syntax"></a>構文  
  
```  
  
      __declspec( dllimport ) declarator  
__declspec( dllexport ) declarator  
```  
  
## <a name="remarks"></a>コメント  
 これらの属性は、DLL のクライアント (実行可能ファイルまたは別の DLL) に対する DLL のインターフェイスを明示的に定義します。 関数を `dllexport` として宣言すると、少なくともエクスポートした関数の指定には、モジュール定義 (.def) ファイルが不要になります。 `dllexport` 属性は `__export` キーワードに置き換わるものです。  
  
 クラスを declspec(dllexport) とマークした場合、そのクラス階層内のクラス テンプレートの特殊化は暗黙的に declspec(dllexport) とマークされます。 つまり、クラス テンプレートが明示的にインスタンス化され、クラスのメンバーの定義が必要になります。  
  
 関数を `dllexport` とマークすると、その関数は装飾名で公開されます。 C++ の関数の場合、この処理には名前のマングルが含まれます。 C 関数または `extern "C"` として宣言されている関数の場合、この処理には呼び出し規約に基づいたプラットフォーム固有の装飾が含まれます。 C と C++ コードで名前の装飾については、次を参照してください。[装飾名](../build/reference/decorated-names.md)です。 `__cdecl` 呼び出し規約を使用する エクスポートされた C 関数や C++ `extern "C"` 関数には、名前の装飾が適用されません。  
  
 修飾されていない名前をエクスポートするには、EXPORTS セクションに非装飾名を定義したモジュール定義 (.def) ファイルを使用してリンクできます。 詳細については、次を参照してください。[エクスポート](../build/reference/exports.md)です。 非装飾名をエクスポートする別の方法が使用するには、`#pragma comment(linker, "/export:alias=decorated_name")`ディレクティブをソース コードにします。  
  
 宣言する場合`dllexport`または**dllimport**、使用する必要があります[拡張属性構文](../cpp/declspec.md)と`__declspec`キーワード。  
  
## <a name="example"></a>例  
  
```cpp  
// Example of the dllimport and dllexport class attributes  
__declspec( dllimport ) int i;  
__declspec( dllexport ) void func();  
```  
  
 または、コードをより読みやすくするために、マクロ定義を使用できます。  
  
```cpp  
#define DllImport   __declspec( dllimport )  
#define DllExport   __declspec( dllexport )  
  
DllExport void func();  
DllExport int i = 10;  
DllImport int j;  
DllExport int n;  
```  
  
 詳細については次を参照してください:  
  
-   [定義と宣言](../cpp/definitions-and-declarations-cpp.md)  
  
-   [dllexport と dllimport を使用したインライン C 関数の定義](../cpp/defining-inline-cpp-functions-with-dllexport-and-dllimport.md)  
  
-   [一般的な規則と制約](../cpp/general-rules-and-limitations.md)  
  
-   [C++ クラスでの dllimport と dllexport の使用](../cpp/using-dllimport-and-dllexport-in-cpp-classes.md)  
  
 **Microsoft 固有の仕様はここまで**  
  
## <a name="see-also"></a>関連項目  
 [_ _declspec](../cpp/declspec.md)   
 [キーワード](../cpp/keywords-cpp.md)
