---
title: "runtime_error クラス | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- runtime_error
- stdexcept/std::runtime_error
dev_langs:
- C++
helpviewer_keywords:
- runtime_error class
ms.assetid: 4d0227bf-847b-45a2-a320-2351ebf98368
caps.latest.revision: 20
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.mt:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
ms.translationtype: Machine Translation
ms.sourcegitcommit: 66798adc96121837b4ac2dd238b9887d3c5b7eef
ms.openlocfilehash: 38434b2a3f50a2056ea9727fb69170bb6a0b8b8d
ms.contentlocale: ja-jp
ms.lasthandoff: 04/29/2017

---
# <a name="runtimeerror-class"></a>runtime_error クラス
このクラスは、プログラムの実行時にのみ検出可能なエラーを通知するためにスローされる例外すべてに対する基底クラスとして機能します。  
  
## <a name="syntax"></a>構文  
  
```  
class runtime_error : public exception {  
public:  
    explicit runtime_error(const string& message);

    explicit runtime_error(const char *message);

};  
```  
  
## <a name="remarks"></a>コメント  
 [exception クラス](../standard-library/exception-class.md)によって返される値は、**message**`.`[data](../standard-library/basic-string-class.md#data) のコピーです。  
  
## <a name="example"></a>例  
  
```cpp  
// runtime_error.cpp  
// compile with: /EHsc /GR  
#include <iostream>  
  
using namespace std;  
  
int main( )  
{  
// runtime_error  
   try   
   {  
      locale loc( "test" );  
   }  
   catch ( exception &e )   
   {  
      cerr << "Caught " << e.what( ) << endl;  
      cerr << "Type " << typeid( e ).name( ) << endl;  
   };  
}  
\* Output:   
Caught bad locale name  
Type class std::runtime_error  
*\  
```  
  
## <a name="requirements"></a>要件  
 **ヘッダー:** \<stdexcept>  
  
 **名前空間:** std  
  
## <a name="see-also"></a>関連項目  
[exception クラス](../standard-library/exception-class.md)

    
 [C++ 標準ライブラリ内のスレッド セーフ](../standard-library/thread-safety-in-the-cpp-standard-library.md)

