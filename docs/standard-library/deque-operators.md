---
title: "&lt;deque&gt; の演算子 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- deque/std::operator!=
- deque/std::operator&gt;
- deque/std::operator&gt;=
- deque/std::operator&lt;
- deque/std::operator&lt;=
- deque/std::operator==
dev_langs: C++
ms.assetid: 482d7c92-54c7-493b-99e6-2a73617481a5
caps.latest.revision: "7"
manager: ghogen
helpviewer_keywords:
- std::operator!= (deque)
- std::operator&gt; (deque)
- std::operator&gt;= (deque)
- std::operator&lt; (deque)
- std::operator&lt;= (deque)
- std::operator== (deque)
ms.openlocfilehash: 81645c8f645a3c3a09ef641b2fce003260bcd5f6
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="ltdequegt-operators"></a>&lt;deque&gt; の演算子
||||  
|-|-|-|  
|[operator!=](#op_neq)|[operator&gt;](#op_gt)|[operator&gt;=](#op_gt_eq)|  
|[operator&lt;](#op_lt)|[operator&lt;=](#op_lt_eq)|[operator==](#op_eq_eq)|  
  
##  <a name="op_neq"></a>  operator!=  
 演算子の左側の deque オブジェクトが右側の deque オブジェクトと等しくないかどうかを調べます。  
  
```
bool operator!=(const deque<Type, Allocator>& left, const deque<Type, Allocator>& right);
```  
  
### <a name="parameters"></a>パラメーター  
 `left`  
 `deque` 型のオブジェクト。  
  
 `right`  
 `deque` 型のオブジェクト。  
  
### <a name="return-value"></a>戻り値  
 deque オブジェクトが等しくない場合は **true**、deque オブジェクトが等しい場合は **false**。  
  
### <a name="remarks"></a>コメント  
 deque オブジェクト間の比較は、要素のペアの比較に基づいています。 2 つの deque オブジェクトは、同じ数の要素を持ち、各要素の値が同じである場合に等しくなります。 それ以外の場合は等しくありません。  
  
### <a name="example"></a>例  
  
```cpp  
// deque_op_ne.cpp  
// compile with: /EHsc  
#include <deque>  
#include <iostream>  
  
int main( )   
{  
   using namespace std;   
   deque <int> c1, c2;  
  
   c1.push_back( 1 );  
   c2.push_back( 2 );  
  
   if ( c1 != c2 )  
      cout << "The deques are not equal." << endl;  
   else  
      cout << "The deques are equal." << endl;  
}  
\* Output:   
The deques are not equal.  
*\  
```  
  
##  <a name="op_lt"></a>  operator&lt;  
 演算子の左側の deque オブジェクトが右側の deque オブジェクトより小さいかどうかを調べます。  
  
```
bool operator<(const deque<Type, Allocator>& left, const deque<Type, Allocator>& right);
```  
  
### <a name="parameters"></a>パラメーター  
 `left`  
 `deque` 型のオブジェクト。  
  
 `right`  
 `deque` 型のオブジェクト。  
  
### <a name="return-value"></a>戻り値  
 演算子の左辺の deque が演算子の右辺の deque 未満である場合は **true**、それ以外の場合は **false**。  
  
### <a name="remarks"></a>コメント  
 deque オブジェクト間の比較は、要素のペアの比較に基づいています。 2 つのオブジェクト間の小なり関係は、最初の等しくない要素のペアの比較に基づいています。  
  
### <a name="example"></a>例  
  
```cpp  
// deque_op_lt.cpp  
// compile with: /EHsc  
#include <deque>  
#include <iostream>  
  
int main( )   
{  
   using namespace std;   
   deque <int> c1, c2;  
  
   c1.push_back( 1 );  
   c1.push_back( 2 );  
   c1.push_back( 4 );  
  
   c2.push_back( 1 );  
   c2.push_back( 3 );  
  
   if ( c1 < c2 )  
      cout << "Deque c1 is less than deque c2." << endl;  
   else  
      cout << "Deque c1 is not less than deque c2." << endl;  
}  
\* Output:   
Deque c1 is less than deque c2.  
*\   
```  
  
##  <a name="op_lt_eq"></a>  operator&lt;=  
 演算子の左側の deque オブジェクトが右側の deque オブジェクト以下かどうかを調べます。  
  
```
bool operator<=(const deque<Type, Allocator>& left, const deque<Type, Allocator>& right);
```  
  
### <a name="parameters"></a>パラメーター  
 `left`  
 `deque` 型のオブジェクト。  
  
 `right`  
 `deque` 型のオブジェクト。  
  
### <a name="return-value"></a>戻り値  
 演算子の左辺の deque が演算子の右辺の deque 以下である場合は **true**、それ以外の場合は **false**。  
  
### <a name="remarks"></a>コメント  
 deque オブジェクト間の比較は、要素のペアの比較に基づいています。 2 つのオブジェクト間の "以下" 関係は、最初の等しくない要素のペアの比較に基づいています。  
  
### <a name="example"></a>例  
  
```cpp  
// deque_op_le.cpp  
// compile with: /EHsc  
#include <deque>  
#include <iostream>  
  
int main( )   
{  
   using namespace std;   
   deque <int> c1, c2;  
  
   c1.push_back( 1 );  
   c1.push_back( 2 );  
   c1.push_back( 4 );  
  
   c2.push_back( 1 );  
   c2.push_back( 3 );  
  
   if ( c1 <= c2 )  
      cout << "Deque c1 is less than or equal to deque c2." << endl;  
   else  
      cout << "Deque c1 is greater than deque c2." << endl;  
}  
\* Output:   
Deque c1 is less than or equal to deque c2.  
*\  
  
```  
  
##  <a name="op_eq_eq"></a>  operator==  
 演算子の左側の deque オブジェクトが右側の deque オブジェクトと等しいかどうかを調べます。  
  
```
bool operator==(const deque<Type, Allocator>& left, const deque<Type, Allocator>& right);
```  
  
### <a name="parameters"></a>パラメーター  
 `left`  
 `deque` 型のオブジェクト。  
  
 `right`  
 `deque` 型のオブジェクト。  
  
### <a name="return-value"></a>戻り値  
 演算子の左辺の deque が演算子の右辺の deque と等しい場合は **true**、それ以外の場合は **false**。  
  
### <a name="remarks"></a>コメント  
 deque オブジェクト間の比較は、要素のペアの比較に基づいています。 2 つの deque は、同じ数の要素を持ち、各要素の値が同じである場合に等しくなります。 それ以外の場合は等しくありません。  
  
### <a name="example"></a>例  
  
```cpp  
// deque_op_eq.cpp  
// compile with: /EHsc  
#include <deque>  
#include <iostream>  
  
int main( )   
{  
   using namespace std;  
   deque <int> c1, c2;  
  
   c1.push_back( 1 );  
   c2.push_back( 1 );  
  
   if ( c1 == c2 )  
      cout << "The deques are equal." << endl;  
   else  
      cout << "The deques are not equal." << endl;  
  
   c1.push_back( 1 );  
   if ( c1 == c2 )  
      cout << "The deques are equal." << endl;  
   else  
      cout << "The deques are not equal." << endl;  
}  
\* Output:   
The deques are equal.  
The deques are not equal.  
*\  
  
```  
  
##  <a name="op_gt"></a>  operator&gt;  
 演算子の左側の deque オブジェクトが右側の deque オブジェクトより大きいかどうかを調べます。  
  
```
bool operator>(const deque<Type, Allocator>& left, const deque<Type, Allocator>& right);
```  
  
### <a name="parameters"></a>パラメーター  
 `left`  
 `deque` 型のオブジェクト。  
  
 `right`  
 `deque` 型のオブジェクト。  
  
### <a name="return-value"></a>戻り値  
 演算子の左辺の deque が演算子の右辺の deque より大きい場合は **true**、それ以外の場合は **false**。  
  
### <a name="remarks"></a>コメント  
 deque オブジェクト間の比較は、要素のペアの比較に基づいています。 2 つのオブジェクト間の大なり関係は、最初の等しくない要素のペアの比較に基づいています。  
  
### <a name="example"></a>例  
  
```cpp  
// deque_op_gt.cpp  
// compile with: /EHsc  
#include <deque>  
#include <iostream>  
  
int main( )   
{  
   using namespace std;   
   deque <int> c1, c2;  
  
   c1.push_back( 1 );  
   c1.push_back( 3 );  
   c1.push_back( 1 );  
  
   c2.push_back( 1 );  
   c2.push_back( 2 );  
   c2.push_back( 2 );  
  
   if ( c1 > c2 )  
      cout << "Deque c1 is greater than deque c2." << endl;  
   else  
      cout << "Deque c1 is not greater than deque c2." << endl;  
}  
\* Output:   
Deque c1 is greater than deque c2.  
*\  
  
```  
  
##  <a name="op_gt_eq"></a>  operator&gt;=  
 演算子の左側の deque オブジェクトが右側の deque オブジェクト以上かどうかを調べます。  
  
```
bool operator>=(const deque<Type, Allocator>& left, const deque<Type, Allocator>& right);
```  
  
### <a name="parameters"></a>パラメーター  
 `left`  
 `deque` 型のオブジェクト。  
  
 `right`  
 `deque` 型のオブジェクト。  
  
### <a name="return-value"></a>戻り値  
 演算子の左辺の deque が演算子の右辺の deque 以上である場合は **true**、それ以外の場合は **false**。  
  
### <a name="remarks"></a>コメント  
 deque オブジェクト間の比較は、要素のペアの比較に基づいています。 2 つのオブジェクト間の "以上" 関係は、最初の等しくない要素のペアの比較に基づいています。  
  
### <a name="example"></a>例  
  
```cpp  
// deque_op_ge.cpp  
// compile with: /EHsc  
#include <deque>  
#include <iostream>  
  
int main( )   
{  
   using namespace std;  
   deque <int> c1, c2;  
  
   c1.push_back( 1 );  
   c1.push_back( 3 );  
   c1.push_back( 1 );  
  
   c2.push_back( 1 );  
   c2.push_back( 2 );  
   c2.push_back( 2 );  
  
   if ( c1 >= c2 )  
      cout << "Deque c1 is greater than or equal to deque c2." << endl;  
   else  
      cout << "Deque c1 is less than deque c2." << endl;  
}  
\* Output:   
Deque c1 is greater than or equal to deque c2.  
*\  
```  
  
## <a name="see-also"></a>関連項目  
 [\<deque>](../standard-library/deque.md)



