---
title: "tuple_element クラス | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- tuple_element
- std::tuple_element
- utility/std::tuple_element
dev_langs:
- C++
helpviewer_keywords:
- tuple_element Class
ms.assetid: 4c51a6c1-ce81-462f-8c6c-291d69f2b77c
caps.latest.revision: 23
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
ms.sourcegitcommit: aadbf7d2c6fece48ab29c1b818995464a790c38b
ms.openlocfilehash: b5568eb951738b1c0c53321d7430c84db6bac9ec
ms.contentlocale: ja-jp
ms.lasthandoff: 03/07/2017

---
# <a name="tupleelement-class"></a>tuple_element クラス
`tuple` 要素をラップします。 `array` 要素および `pair` 要素のラップの特殊化。  
  
## <a name="syntax"></a>構文  
  
```  
// CLASS tuple_element (find element by index)  
template <size_t Index, class Tuple>  
   struct tuple_element;  
 
// tuple_element for const 
template <size_t Index, class Tuple>  
   struct tuple_element<Index, const Tuple>;  
 
// tuple_element for volatile  
template <size_t Index, class Tuple>  
   struct tuple_element<Index, volatile Tuple>;  
 
// tuple_element for const volatile  
template <size_t Index, class Tuple>  
   struct tuple_element<Index, const volatile Tuple>;  
 
// Helper typedef
template <size_t Index, class Tuple>  
   using tuple_element_t = typename tuple_element<Index, Tuple>::type; 

// Specialization for arrays  
template <size_t Index, class Elem, size_t Size>  
   struct tuple_element<Index, array<Elem, Size>>;  
  
// Specializations for pairs
// struct to determine type of element 0 in pair
template <class T1, class T2>
   struct tuple_element<0, pair<T1, T2>>;

// struct to determine type of element 1 in pair
template <class T1, class T2>
   struct tuple_element<1, pair<T1, T2>>;
```  
  
### <a name="parameters"></a>パラメーター  
*インデックス*  
指定した要素のインデックス。  
  
*Tuple*  
組の型。  
  
*Elem*  
配列要素の型。  
  
*Size*  
配列のサイズ。  

*T1* ペアの 1 番目の要素の型。
  
*T2*  
ペアの 2 番目の要素の型。

## <a name="remarks"></a>コメント  
このテンプレート クラス `tuple_element` では、タプル型 `Tuple` のインデックス `Index` にある型のシノニムである typedef `type` が入れ子になっています。  

Typedef `tuple_element_t` は `tuple_element<Index, Tuple>::type` の便利なエイリアスです。  
  
配列のテンプレート クラスの特殊化では、同じ型の `Size` 要素のタプルとして `array` にインターフェイスを提供します。 それぞれの特殊化は入れ子の typedef `type` を持ち、これは `Index` の `array`要素の型のシノニムであり、const-volatile 制限が保持されます。  
  
`pair` の型のテンプレートの特殊化では、それぞれ 1 つのメンバーの typedef である `type` を提供します。これはペアの指定された位置にある要素の型のシノニムであり、const または volatile の制限が保持されます。 Typedef `tuple_element_t` は `tuple_element<N, pair<T1, T2>>::type` の便利なエイリアスです。  
  
使用して、 [get 関数&lt;ユーティリティ&gt;](../standard-library/utility-functions.md#get)または指定した種類の指定位置にある要素を返します。 
  
## <a name="example"></a>例  
  
```cpp  
#include <tuple>  
#include <string>  
#include <iostream>  
  
using namespace std;  
typedef tuple<int, double, string> MyTuple;  
  
int main() {  
    MyTuple c0{ 0, 1.5, "Tail" };  
  
    tuple_element_t<0, MyTuple> val = get<0>(c0); //get by index  
    tuple_element_t<1, MyTuple> val2 = get<1>(c0);  
    tuple_element_t<2, MyTuple> val3 = get<string>(c0); // get by type  
  
    cout << val << " " << val2 << " " << val3 << endl;  
}  
```  
  
```Output  
0 1.5 Tail  
```  
  
## <a name="example"></a>例  
  
```cpp  
#include <array>   
#include <iostream>   
  
using namespace std;  
typedef array<int, 4> MyArray;  
  
int main()  
{  
    MyArray c0 { 0, 1, 2, 3 };  
  
    for (const auto& e : c0)  
    {  
        cout << " " << e;  
    }  
    cout << endl;  
  
    // display first element " 0"   
    tuple_element<0, MyArray>::type val = c0.front();  
    cout << " " << val << endl;  
}  
```  
  
```Output  
 0 1 2 3  
 0  
```  
  
## <a name="example"></a>例  
  
```cpp  
#include <utility>   
#include <iostream>   
  
using namespace std;  
  
typedef pair<int, double> MyPair;  
int main() {  
    MyPair c0(0, 1.333);  
  
    // display contents " 0 1"   
    cout << " " << get<0>(c0);  
    cout << " " << get<1>(c0) << endl;  
  
    // display first element " 0" by index  
    tuple_element<0, MyPair>::type val = get<0>(c0);  
    cout << " " << val;  
  
    // display second element by type   
    tuple_element<1, MyPair>::type val2 = get<double>(c0);  
    cout << " " << val2 << endl;  
}  
```  
  
```Output  
 0 1.333  
 0 1.333  
```  

## <a name="requirements"></a>要件  
 **ヘッダー:** \<tuple>  
 **ヘッダー:** \<array> (配列の特殊化用)  **ヘッダー:** \<utility> (ペアの特殊化用)  **名前空間:** std  
  
## <a name="see-also"></a>関連項目  
[tuple ](../standard-library/tuple-class.md)
