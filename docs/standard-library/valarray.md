---
title: '&lt;valarray&gt; | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- std.<valarray>
- valarray/std::<valarray>
- std::<valarray>
- <valarray>
dev_langs:
- C++
helpviewer_keywords:
- valarray header
ms.assetid: 30835415-21c1-4801-8f24-6bbef7dd8ecd
caps.latest.revision: 19
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
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
ms.openlocfilehash: 830078013287ec0efc94d0b7fa3f0adb4ea6c22e
ms.contentlocale: ja-jp
ms.lasthandoff: 04/29/2017

---
# <a name="ltvalarraygt"></a>&lt;valarray&gt;
テンプレート クラス valarray、および多数のサポート テンプレート クラスと関数を定義します。  
  
## <a name="syntax"></a>構文  
  
```  
#include <valarray>  
  
```  
  
## <a name="remarks"></a>コメント  
 これらのテンプレート クラスと関数には、パフォーマンス向上を目的として特別な許容度が認められています。 具体的には、**valarray\<**T1**>** 型を返す関数はすべて、他の T2 型のオブジェクトを返すこともできます。 その場合、**valarray\<**T2**>** 型の 1 つ以上の引数を受け取る関数すべてに、T2 型引数に置換された個々の引数が任意に組み合わされたものを受け取るオーバーロードが必要です。  
  
### <a name="functions"></a>関数  
  
|||  
|-|-|  
|[abs](../standard-library/valarray-functions.md#abs)|入力 valarray の要素を演算し、入力 valarray の要素の絶対値と等しい要素を持つ valarray を返します。|  
|[acos](../standard-library/valarray-functions.md#acos)|入力 valarray の要素を演算し、入力 valarray の要素のアークコサインと等しい要素を持つ valarray を返します。|  
|[asin](../standard-library/valarray-functions.md#asin)|入力 valarray の要素を演算し、入力 valarray の要素のアークサインと等しい要素を持つ valarray を返します。|  
|[atan](../standard-library/valarray-functions.md#atan)|入力 valarray の要素を演算し、入力 valarray の要素のアークタンジェントの主値と等しい要素を持つ valarray を返します。|  
|[atan2](../standard-library/valarray-functions.md#atan2)|valarray の定数と要素の組み合わせによって指定されたデカルト成分のアークタンジェントと等しい要素を持つ valarray を返します。|  
|[cos](../standard-library/valarray-functions.md#cos)|入力 valarray の要素を演算し、入力 valarray の要素のコサインと等しい要素を持つ valarray を返します。|  
|[cosh](../standard-library/valarray-functions.md#cosh)|入力 valarray の要素を演算し、入力 valarray の要素のハイパーボリック コサインと等しい要素を持つ valarray を返します。|  
|[exp](../standard-library/valarray-functions.md#exp)|入力 valarray の要素を演算し、入力 valarray の要素の自然指数と等しい要素を持つ valarray を返します。|  
|[log](../standard-library/valarray-functions.md#log)|入力 valarray の要素を演算し、入力 valarray の要素の自然対数と等しい要素を持つ valarray を返します。|  
|[log10](../standard-library/valarray-functions.md#log10)|入力 valarray の要素を演算し、入力 valarray の要素の常用対数 (底が 10 の対数) と等しい要素を持つ valarray を返します。|  
|[pow](../standard-library/valarray-functions.md#pow)|入力 valarray と定数の要素を演算し、入力 valarray の要素によって指定されている底と等しい要素を持つ valarray か、入力 valarray か定数の要素で指定された値だけ定数を指数乗したものと等しい要素を持つ valarray を返します。|  
|[sin](../standard-library/valarray-functions.md#sin)|入力 valarray の要素を演算し、入力 valarray の要素のサインと等しい要素を持つ valarray を返します。|  
|[sinh](../standard-library/valarray-functions.md#sinh)|入力 valarray の要素を演算し、入力 valarray の要素のハイパーボリック サインと等しい要素を持つ valarray を返します。|  
|[sqrt](../standard-library/valarray-functions.md#sqrt)|入力 valarray の要素を演算し、入力 valarray の要素の平方根と等しい要素を持つ valarray を返します。|  
|[swap](../standard-library/valarray-functions.md#swap)||  
|[tan](../standard-library/valarray-functions.md#tan)|入力 valarray の要素を演算し、入力 valarray の要素のタンジェントと等しい要素を持つ valarray を返します。|  
|[tanh](../standard-library/valarray-functions.md#tanh)|入力 valarray の要素を演算し、入力 valarray の要素のハイパーボリック タンジェントと等しい要素を持つ valarray を返します。|  
  
### <a name="operators"></a>演算子  
  
|||  
|-|-|  
|[operator!=](../standard-library/valarray-operators.md#op_neq)|サイズが等しい 2 つの valarray の対応する要素が等しくないか、あるいはある valarray のすべての要素が valarray の要素型の指定値と等しくないかをテストします。|  
|[operator%](../standard-library/valarray-operators.md#op_mod)|サイズが等しい 2 つの valarray の対応する要素を除算した剰余か、valarray の要素型の指定値で valarray を除算した剰余、または valarray で指定値を除算した剰余を取得します。|  
|[operator&](../standard-library/valarray-operators.md#op_amp)|サイズが等しい 2 つの valarray の対応する要素間、または valarray と要素型の指定値との間でビットごとの **AND** を計算した結果を取得します。|  
|[operator&&](../standard-library/valarray-operators.md#op_amp_amp)|サイズが等しい 2 つの valarray の対応する要素間、または valarray と valarray の要素型の指定値との間で論理 **AND** を計算した結果を取得します。|  
|[operator>](../standard-library/valarray-operators.md#op_gt)|ある valarray の要素がサイズが等しい valarray の要素より大きいか、またはある valarray のすべての要素が valarray の要素型の指定値より大きいか、もしくは指定値より小さいかをテストします。|  
|[operator>=](../standard-library/valarray-operators.md#op_gt_eq)|ある valarray の要素がサイズが等しい valarray の要素以上であるか、またはある valarray のすべての要素が valarray の要素型の指定値以上であるか、もしくは指定値以下であるかをテストします。|  
|[operator>>](../standard-library/valarray-operators.md#op_gt_gt)|valarray の各要素のビットを、指定された位置数だけ右にシフトさせるか、2 番目の valarray で指定された要素ごとの量だけ右にシフトさせます。|  
|[operator<](../standard-library/valarray-operators.md#op_lt)|ある valarray の要素がサイズが等しい valarray の要素未満であるか、またはある valarray のすべての要素が valarray の要素型の指定値より大きいか、もしくは指定値未満であるかをテストします。|  
|[operator<=](../standard-library/valarray-operators.md#op_lt_eq)|ある valarray の要素がサイズが等しい valarray の要素以下であるか、またはある valarray のすべての要素が valarray の要素型の指定値以上であるか、もしくは指定値以下であるかをテストします。|  
|[operator<<](../standard-library/valarray-operators.md#op_lt_lt)|valarray の各要素のビットを、指定された位置数だけ左にシフトさせるか、2 番目の valarray で指定された要素ごとの量だけ左にシフトさせます。|  
|[operator*](../standard-library/valarray-operators.md#op_star)|サイズが等しい 2 つの valarray の対応する要素間の要素ごとの積、または valarray と valarray の要素型の指定値との間の積を取得します。|  
|[operator+](../standard-library/valarray-operators.md#op_add)|サイズが等しい 2 つの valarray の対応する要素間の要素ごとの和、または valarray と valarray の要素型の指定値との間の和を取得します。|  
|[operator-](../standard-library/valarray-operators.md#operator-)|サイズが等しい 2 つの valarray の対応する要素間の要素ごとの差、または valarray と valarray の要素型の指定値との間の差を取得します。|  
|[operator/](../standard-library/valarray-operators.md#op_div)|サイズが等しい 2 つの valarray の対応する要素間の要素ごとの商、または valarray と valarray の要素型の指定値との間の商を取得します。|  
|[operator==](../standard-library/valarray-operators.md#op_eq_eq)|サイズが等しい 2 つの valarray の対応する要素が等しいか、あるいはある valarray のすべての要素が valarray の要素型の指定値と等しいかをテストします。|  
|[operator^](../standard-library/valarray-operators.md#op_xor)|サイズが等しい 2 つの valarray の対応する要素間、または valarray と要素型の指定値との間でビットごとの排他的 `OR` を計算した結果を取得します。|  
|[operator&#124;](../standard-library/valarray-operators.md#op_or)|サイズが等しい 2 つの valarray の対応する要素間、または valarray と要素型の指定値との間でビットごとの `OR` を計算した結果を取得します。|  
|[operator&#124;&#124;](../standard-library/valarray-operators.md#op_lor)|サイズが等しい 2 つの valarray の対応する要素間、または valarray と valarray の要素型の指定値との間で論理 `OR` を計算した結果を取得します。|  
  
### <a name="classes"></a>クラス  
  
|||  
|-|-|  
|[gslice Class](../standard-library/gslice-class.md)|valarray の多次元スライスを定義するのに使用する valarray のユーティリティ クラス。|  
|[gslice_array Class](../standard-library/gslice-array-class.md)|valarray の一般的なスライスで定義されるサブセット配列間の演算を実行して一般的なスライス オブジェクトをサポートする、内部の補助テンプレート クラス。|  
|[indirect_array Class](../standard-library/indirect-array-class.md)|親 valarray のインデックスのサブセットを指定することにより定義されるサブセット配列間の演算を実行して valarray のサブセットとして機能するオブジェクトをサポートする、内部の補助テンプレート クラス。|  
|[mask_array Class](../standard-library/mask-array-class.md)|サブセット配列間の演算を提供することにより、ブール式で指定された親 valarray のサブセットとして機能するオブジェクトをサポートする、内部の補助テンプレート クラス。|  
|[slice Class](../standard-library/slice-class.md)|valarray のベクター的 1 次元サブセットを定義するのに使用する valarray のユーティリティ クラス。|  
|[slice_array Class](../standard-library/slice-array-class.md)|valarray のスライスで定義されるサブセット配列間の演算を提供することによりスライス オブジェクトをサポートする、内部の補助テンプレート クラス。|  
|[valarray Class](../standard-library/valarray-class.md)|このテンプレート クラスは、配列として格納され、高速数値演算を実行するように設計されている、計算パフォーマンス用に最適化された **Type** 型の要素のシーケンスを制御するオブジェクトについて記述します。|  
  
### <a name="specializations"></a>特殊化  
  
|||  
|-|-|  
|[valarray\<bool> クラス](../standard-library/valarray-bool-class.md)|テンプレート クラス valarray\<**Type**> を `bool` 型の要素に特化したバージョン。|  
  
## <a name="see-also"></a>関連項目  
 [ヘッダー ファイル リファレンス](../standard-library/cpp-standard-library-header-files.md)   
 [C++ 標準ライブラリ内のスレッド セーフ](../standard-library/thread-safety-in-the-cpp-standard-library.md)



