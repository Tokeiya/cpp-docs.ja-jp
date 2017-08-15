---
title: "スレッド ローカル ストレージ | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-language
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- thread-local variables
- TLS (thread local storage)
- thread storage-class attribute
- thread-local storage
- storage, thread local storage
ms.assetid: a0f1b109-c953-4079-aa10-e47f5483173d
caps.latest.revision: 10
author: mikeblome
ms.author: mblome
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d6eb43b2e77b11f4c85f6cf7e563fe743d2a7093
ms.openlocfilehash: 726627607d02fd559af3ab42b45d90a2435db777
ms.contentlocale: ja-jp
ms.lasthandoff: 05/18/2017

---
# <a name="thread-local-storage"></a>スレッド ローカル ストレージ
**Microsoft 固有の仕様**  
  
 スレッド ローカル ストレージ (TLS) は、指定されたマルチスレッド プロセスの各スレッドが、スレッド固有のデータを格納するための場所を割り当てる手段です。 標準のマルチスレッド プログラムでは、データは特定のプロセスのすべてのスレッド間で共有されますが、スレッド ローカル ストレージはスレッドごとのデータを割り当てるための機能です。 スレッドの詳細については、[!INCLUDE[winsdkshort](../atl-mfc-shared/reference/includes/winsdkshort_md.md)] の「[Processes and Threads (プロセスとスレッド)](http://msdn.microsoft.com/library/windows/desktop/ms684841)」をご覧ください。  
  
 Microsoft C 言語には、スレッド ローカル変数を宣言するために __declspec キーワードと共に使用される、拡張ストレージ クラスの属性、スレッドが含まれています。 たとえば、次に示すコードは、整数型のスレッド ローカル変数を宣言して特定の値に初期化します。  
  
```  
__declspec( thread ) int tls_i = 1;  
```  
  
 静的に連結されるスレッド ローカル変数を宣言する場合は、次のガイドラインに従ってください。  
  
-   **__declspec(thread)** の属性の使用は、DLL のインポートの[遅延読み込み](../build/reference/linker-support-for-delay-loaded-dlls.md)に干渉する可能性があります**。**  
  
-   スレッド属性は、データの宣言と定義だけに適用できます。 関数の宣言や定義には使用できません。 たとえば、次のコードはコンパイラ エラーになります。  
  
    ```  
    #define Thread   __declspec( thread )  
    Thread void func();      /* Error */  
    ```  
  
-   thread 属性は、静的ストレージ存続期間のあるデータ項目にのみ指定できます。 これには、グローバル データ (static と extern の両方) およびローカル スタティック データの両方が含まれます。 自動データは、thread 属性を使用して宣言することはできません。 たとえば、次のコードはコンパイラ エラーになります。  
  
    ```  
    #define Thread   __declspec( thread )  
    void func1()  
    {  
        Thread int tls_i;            /* Error */  
    }  
  
    int func2( Thread int tls_i )    /* Error */  
    {  
       return tls_i;  
    }  
    ```  
  
-   宣言と定義が同じファイルと個別のファイルのどちらで発生するかにかかわらず、スレッド ローカル データの宣言と定義にスレッド属性を使用する必要があります。 たとえば、次のコードはエラーになります。  
  
    ```  
    #define Thread   __declspec( thread )  
    extern int tls_i;     /* This generates an error, because the   */  
    int Thread tls_i;     /* declaration and the definition differ. */  
    ```  
  
-   thread 属性を型修飾子として使用することはできません。 たとえば、次のコードはコンパイラ エラーになります。  
  
    ```  
    char *ch __declspec( thread );      /* Error */  
    ```  
  
-   スレッドのローカル変数のアドレスは定数とは見なされず、またそのようなアドレスが含まれている式は、定数式とは見なされません。 これは、スレッドのローカル変数のアドレスをポインターの初期化子として使用できないことを意味します。 たとえば、コンパイラは次のコードをエラーとします。  
  
    ```  
    #define Thread   __declspec( thread )  
    Thread int tls_i;  
    int *p = &tls_i;      /* Error */  
    ```  
  
-   C では、自分自身を参照している式で変数を初期化できます。ただし、この場合のオブジェクトは、非静的なものに限られます。 例:  
  
    ```  
    #define Thread   __declspec( thread )  
    Thread int tls_i = tls_i;             /* Error */  
    int j = j;                            /* Error */  
    Thread int tls_i = sizeof( tls_i )    /* Okay  */  
    ```  
  
     初期化される変数が含まれている sizeof 式は、式自体の参照が発生しないので、有効になります。  
  
-   **__declspec(thread)** の属性の使用は、DLL のインポートの[遅延読み込み](../build/reference/linker-support-for-delay-loaded-dlls.md)に干渉する可能性があります**。**  
  
 スレッド属性の使用の詳細については、[マルチスレッドのトピック](../parallel/multithreading-support-for-older-code-visual-cpp.md)に関するページをご覧ください。  
  
 **END Microsoft 固有の仕様**  
  
## <a name="see-also"></a>関連項目  
 [C 拡張ストレージ クラス属性](../c-language/c-extended-storage-class-attributes.md)