---
title: "エクスポート |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords: vc-attr.export
dev_langs: C++
helpviewer_keywords: export attribute
ms.assetid: 70b3e848-fad6-4e09-8c72-be60ca72a4df
caps.latest.revision: "11"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 7a3229b1cc924c0268bf9a79df53bc18ce2684a1
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="export"></a>export
.Idl ファイルに配置するデータ構造が発生します。  
  
## <a name="syntax"></a>構文  
  
```  
  
[export]  
  
```  
  
## <a name="remarks"></a>コメント  
 **エクスポート**C++ 属性により、データ構造を .idl ファイルに配置してで使用できる任意の言語で使用するために使用できるようにするバイナリ互換性のある形式のタイプ ライブラリが発生します。  
  
 適用することはできません、**エクスポート**場合でも、クラスはパブリック メンバーのみがある属性をクラス (と同等、 `struct`)。  
  
 名前のないをエクスポートする場合`enum`s または`struct`s」で始まる名前が付けになる**体***x*ここで、 *x*連続番号です。  
  
 エクスポートの有効な typedef では、基本型、構造体、共用体、列挙型は、または、識別子を入力します。  参照してください[typedef](http://msdn.microsoft.com/library/windows/desktop/aa367287)詳細についてはします。  
  
## <a name="example"></a>例  
 次のコードを使用する方法を示しています、**エクスポート**属性。  
  
```  
// cpp_attr_ref_export.cpp  
// compile with: /LD  
[module(name="MyLibrary")];  
  
[export]  
struct MyStruct {  
   int i;  
};  
```  
  
## <a name="requirements"></a>要件  
  
### <a name="attribute-context"></a>属性コンテキスト  
  
|||  
|-|-|  
|**対象**|**共用体**、 `typedef`、 `enum`、 `struct`、または`interface`|  
|**反復可能**|いいえ|  
|**必要な属性**|なし|  
|**無効な属性**|なし|  
  
 詳細については、「 [属性コンテキスト](../windows/attribute-contexts.md)」を参照してください。  
  
## <a name="see-also"></a>関連項目  
 [コンパイラ属性](../windows/compiler-attributes.md)   
 [Typedef、Enum、Union、および Struct 型の属性](../windows/typedef-enum-union-and-struct-attributes.md)   
