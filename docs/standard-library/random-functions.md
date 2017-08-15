---
title: "&lt;random&gt; 関数 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: []
ms.assetid: 2ac9ec59-619b-4b85-a425-f729277c1bc8
caps.latest.revision: 10
manager: ghogen
translationtype: Machine Translation
ms.sourcegitcommit: 3168772cbb7e8127523bc2fc2da5cc9b4f59beb8
ms.openlocfilehash: 3aebef535acb59046fab53d49051df16bd362c3c
ms.lasthandoff: 02/24/2017

---
# <a name="ltrandomgt-functions"></a>&lt;random&gt; 関数
  
##  <a name="generate_canonical"></a>  generate_canonical  
 ランダム シーケンスから浮動小数点値を返します。  
  
> [!NOTE]
>  ISO C++ 標準では、この関数は範囲 [ `0`, `1`) 内の値を返すと述べられています。 Visual Studio は、まだこの制約には準拠していません。 この範囲内の値を生成する代替手段として、[uniform_real_distribution](../standard-library/uniform-real-distribution-class.md) を使用します。  
  
```  
template <class RealType, size_t Bits, class Generator>  
RealType generate_canonical(Generator& Gen);
```  
  
### <a name="parameters"></a>パラメーター  
 `RealType`  
 浮動小数点整数型。 使用可能な型については、[\<random>](../standard-library/random.md) をご覧ください。  
  
 `Bits`  
 乱数ジェネレーター。  
  
 `Gen`  
 乱数ジェネレーター。  
  
### <a name="remarks"></a>コメント  
 このテンプレート関数は、`operator()` の `Gen` を繰り返し呼び出して、型 `x` の浮動小数点値 `RealType` に戻り値を埋め込みます。これは、指定された数の仮数部のビットが `x` に揃うまで続行されます。 指定された数とは、`Bits` (0 以外である必要があります) と `RealType` の仮数部のビット数の小さい方を示します。 最初の呼び出しで最下位のビットが提供されます。 `x` が返されます。  
  
## <a name="see-also"></a>関連項目  
 [\<random>](../standard-library/random.md)

