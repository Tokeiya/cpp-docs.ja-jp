---
title: "is_error_code_enum 構造体 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- future/std::is_error_code_enum
dev_langs:
- C++
ms.assetid: 84ae4b99-66d2-41ba-9b50-645fcbe14630
caps.latest.revision: 13
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- ru-ru
- zh-cn
- zh-tw
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
ms.translationtype: Machine Translation
ms.sourcegitcommit: 4ecf60434799708acab4726a95380a2d3b9dbb3a
ms.openlocfilehash: f9b576e6d69cc499aa05cbd857b3cd35f99a8adc
ms.contentlocale: ja-jp
ms.lasthandoff: 04/19/2017

---
# <a name="iserrorcodeenum-structure"></a>is_error_code_enum 構造体
[future_errc](../standard-library/future-enums.md#future_errc) が [error_code](../standard-library/error-code-class.md) の格納に適していることを示す特殊化です。  
  
## <a name="syntax"></a>構文  
  
```
template <>
struct is_error_code_enum<Future_errc> : public true_type;
```  
  
## <a name="requirements"></a>要件  
 **ヘッダー:** \<将来 >  
  
 **名前空間:** std  
  
## <a name="see-also"></a>関連項目  
 [ヘッダー ファイル リファレンス](../standard-library/cpp-standard-library-header-files.md)   
 [\<future>](../standard-library/future.md)



