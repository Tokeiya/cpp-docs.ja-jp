---
title: "C++ (Modern C) へようこそ |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-language
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
ms.assetid: 1cb1b849-ed9c-4721-a972-fd8f3dab42e2
caps.latest.revision: "23"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 45cb4bb1537f7d897b1dd53ada413e73a54162ab
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="welcome-back-to-c-modern-c"></a>C++ へようこそ (Modern C++)
C++ は世界で最も広く使用されているプログラミング言語の 1 つです。 適切に記述された C++ プログラムは、高速で効率的です。 この言語は、楽しめるゲームから、高性能な科学的ソフトウェア、デバイス ドライバー、埋め込みプログラム、さらに Windows クライアント アプリケーションに至るまで、幅広いアプリケーションの作成に使用でき、他の言語よりも柔軟性があります。 20 年以上にわたって、C++ はそれらをはじめとするさまざまなソリューション使用されてきました。 ますます多くの C++ プログラマが、旧来の C のプログラミング スタイルから卒業して、最新の C++ の手法を身に着けていることを、ご存知でない方もいるかもしれません。  
  
 C++ の最初の要件の 1 つは、C 言語との下位互換性でした。 それ以来、C++ はさまざまな進化をとげています。C 言語でのクラスの使用に始まり、最初の C++ 言語仕様が作成され、それに続く多くの拡張が行われてきました。 この経緯のため、C++ はマルチパラダイムのプログラミング言語と呼ばれることが多くあります。 C++ では、生のポインター、配列、null で終わる文字列、カスタム データ構造、その他の機能を使って、純粋な手続き型の C スタイルのプログラミングを行うことも可能です。これにより優れたパフォーマンスが可能となりますが、バグと複雑性も生じることになります。  C スタイルのプログラミングはそのようなリスクを抱えていたため、C++ の当初のねらいの 1 つは、タイプ セーフで、作成、拡張、保守の容易なプログラムを作成可能にすることでした。 C++ は、早い段階でオブジェクト指向プログラミングなどのプログラミング パラダイムを追加しました。 長年にわたり、十分に検証されたデータ構造やアルゴリズムの標準ライブラリと共に、さまざまな機能が言語に追加されました。 これらの拡張が最新の C++ のスタイルを可能にしています。  
  
 最新の C++ では下記のような点が強化されています。  
  
-   ヒープまたは静的なグローバル スコープではなく、スタック ベースのスコープ。  
  
-   明示的な型名ではなく、自動型推論。  
  
-   生のポインターではなく、スマート ポインター。  
  
-   `std::string`および`std::wstring`型 (を参照してください[\<文字列 >](../standard-library/string.md)) ではなく生`char[]`配列。  
  
-   [C++ 標準ライブラリ](../standard-library/cpp-standard-library-header-files.md)などのコンテナー `vector`、 `list`、および`map`生配列またはカスタムのコンテナーの代わりにします。 参照してください[\<ベクター >](../standard-library/vector.md)、 [\<リスト >](../standard-library/list.md)、および[\<マップ >](../standard-library/map.md)です。  
  
-   C++ 標準ライブラリ[アルゴリズム](../standard-library/algorithm.md)の代わりに手動でコーディングされました。  
  
-   例外はエラー状態の報告と処理のためだけに使用される。  
  
-   C++ 標準ライブラリを使用して通信をスレッド間のロック制御不要`std::atomic<>`(を参照してください[\<アトミック >](../standard-library/atomic.md)) その他のスレッド間通信メカニズムの代わりにします。  
  
-   インライン[ラムダ関数](../cpp/lambda-expressions-in-cpp.md)個別に実装される小さい関数の代わりにします。  
  
-   範囲ベースの for ループ、フォーム内のコレクションを配列、C++ 標準ライブラリのコンテナー、および Windows ランタイムで動作するより堅牢なループを記述して`for ( for-range-declaration : expression )`です。 これは、コア言語サポートの一部です。 詳細については、次を参照してください。[ステートメント (C++) の範囲に基づく](../cpp/range-based-for-statement-cpp.md)です。  
  
 C++ 言語自体も進化しました。 次の 2 つのコード スニペットを比較してみます。 このスニペットは以前の C++ を使ったものです。  
  
```cpp  
// circle and shape are user-defined types  
circle* p = new circle( 42 );   
vector<shape*> v = load_shapes();  
  
for( vector<circle*>::iterator i = v.begin(); i != v.end(); ++i ) {  
    if( *i && **i == *p )  
        cout << **i << " is a match\n";  
}  
  
for( vector<circle*>::iterator i = v.begin();  
        i != v.end(); ++i ) {  
    delete *i; // not exception safe  
}  
  
delete p;  
```  
  
 このスニペットは最新の C++ で同じことを行うものです。  
  
```cpp  
#include <memory>  
#include <vector>  
// ...  
// circle and shape are user-defined types  
auto p = make_shared<circle>( 42 );  
vector<shared_ptr<shape>> v = load_shapes();  
  
for( auto& s : v ) {  
    if( s && *s == *p )  
        cout << *s << " is a match\n";  
} 
```  
  
 最新の C++ では、スマート ポインターを使用できるため、新規/削除を使用したり、明示的な例外処理を使用する必要はありません。 使用すると、`auto`控除を入力し、[ラムダ関数](../cpp/lambda-expressions-in-cpp.md)、迅速なコードを記述することができます、それを引き締めより的確に把握します。 ってきた方、特に型の大部分が参照型であり、値型が非常に少ない、他のマネージ言語から移ってきた方は、C++ のクラスは既定で値型であることに注意してください。さらに `for_each` を使用すると、簡単にすっきりしたコードを記述でき、`for` ループを使用するよりも、意図しないエラーを生じることが少なくなります。 スケルトン コードを使って、最小限のコードでアプリケーションを記述できます。 さらにそのコードを例外セーフでメモリ セーフにすることができ、割り当て/解放や、エラー コードを取り扱う必要はありません。  
  
 最新の C++ では、2 種類のポリモーフィズムが組み込まれています: コンパイル時にテンプレート経由によるもの、および実行時に継承と仮想化によるものです。 2 種類のポリモーフィズムを活用することにより、優れた効果を生じることができます。 C++ 標準ライブラリ テンプレート`shared_ptr`内部仮想メソッドを使用して、非常に簡単型消去を実現します。 ただし、テンプレートが最適な選択である場合には、ポリモーフィズムの仮想化を過度に使用しないでください。 テンプレートは非常に強力です。  
  
 他の言語から C++ に移ってきた方、特に型の大部分が参照型であり、値型が非常に少ない、他のマネージ言語から移ってきた方は、C++ のクラスは既定で値型であることに注意してください。 ただし、それらを参照型として指定して、オブジェクト指向プログラミングをサポートするポリモーフィックな動作を可能とすることもできます。 値型はメモリとレイアウト コントロールに関するものであり、参照型はポリモーフィズムをサポートする基底クラスと仮想関数に関するものであることを理解すると、役に立ちます。 既定では、値型はコピー可能で、それぞれにコピー コンストラクターとコピー代入演算子があります。 参照型を指定する場合は、コピー コンストラクターとコピー代入演算子を無効化して、クラスをコピー不可にし、ポリモーフィズムをサポートする仮想デストラクターを使用します。 また値型はコンテンツに関するものであり、コピーされるときに、それぞれ変更可能な 2 つの個別の値を持ちます。 一方、参照型はオブジェクトがどのようなものであるかについての識別に関するものであり、このためポリモーフィックな型として参照される場合もあります。  
  
 再びパワーが重要視されてきているため、C++ にとってのルネサンスが訪れています。 プログラマの生産性が重要である場合には Java や C# などの言語が適していますが、パワーとパフォーマンスがより重要である場合には、それらの言語には限界があります。 高い効率性とパワーに関しては、特に制限のあるハードウェアによるデバイスでは、最新の C++ に勝るものはありません。  
  
 言語が最新であるだけでなく、開発ツールも最新です。 [!INCLUDE[vsprvs](../assembler/masm/includes/vsprvs_md.md)] により、開発サイクルのすべての部分が堅牢で効率的になります。 これにはアプリケーション ライフサイクル管理 (ALM) ツール、IntelliSense などの IDE の強化、XAML などのツールに適した方法、ビルド、デバッグ、および他のツールが含まれています。  
  
 ドキュメントのこの部分の記事は、最新の C++ プログラムを作成するために、最も重要な機能および技術に関する、高レベルのガイドラインとベスト プラクティスを提供します。  
  
-   [C++ 型システム](../cpp/cpp-type-system-modern-cpp.md)  
  
-   [均一な初期化とコンストラクターのデリゲート](../cpp/uniform-initialization-and-delegating-constructors.md)  
  
-   [オブジェクトの有効期間とリソースの管理](../cpp/object-lifetime-and-resource-management-modern-cpp.md)  
  
-   [リソースを所有するオブジェクト (RAII)](../cpp/objects-own-resources-raii.md)  
  
-   [スマート ポインター](../cpp/smart-pointers-modern-cpp.md)  
  
-   [コンパイル時のカプセル化の Pimpl](../cpp/pimpl-for-compile-time-encapsulation-modern-cpp.md)  
  
-   [コンテナー](../cpp/containers-modern-cpp.md)  
  
-   [アルゴリズム](../cpp/algorithms-modern-cpp.md)  
  
-   [文字列および I/O の書式設定 (Modern C)](../cpp/string-and-i-o-formatting-modern-cpp.md)  
  
-   [エラーと例外処理](../cpp/errors-and-exception-handling-modern-cpp.md)  
  
-   [ABI の境界での移植性](../cpp/portability-at-abi-boundaries-modern-cpp.md)  
  
 詳細については、StackOverflow の記事を参照してください。 [C++ の表現形式は、c++ 11 で廃止されました。](http://go.microsoft.com/fwlink/?LinkId=402836)  
  
## <a name="see-also"></a>関連項目  
 [C++ 言語リファレンス](../cpp/cpp-language-reference.md)   
 [ラムダ式](../cpp/lambda-expressions-in-cpp.md)   
 [.NET 標準ライブラリ](../standard-library/cpp-standard-library-reference.md)  
 [Visual C++ 言語への準拠](../visual-cpp-language-conformance.md)  
