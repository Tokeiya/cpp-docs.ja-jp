---
title: "関数のオーバー ロード |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-language
ms.tgt_pltfrm: 
ms.topic: language-reference
dev_langs: C++
helpviewer_keywords:
- function overloading [C++], about function overloading
- function overloading
- declaring functions [C++], overloading
ms.assetid: 3c9884cb-1d5e-42e8-9a49-6f46141f929e
caps.latest.revision: "10"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 2486357766d2dbd9f5d4250e2d0fb38e02ba51bc
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="function-overloading"></a>関数のオーバーロード
C++ では、同じスコープ内で同じ名前の複数の関数を指定できます。 これらは、オーバーロードされた関数と呼ばれます。これについては、オーバーロードに関するトピックで詳しく説明します。 オーバーロードされた関数により、プログラマは、引数の種類と数に応じて関数に異なるセマンティクスを指定できます。  
  
 たとえば、**印刷**、文字列を受け取る関数 (または**char \*** ) 引数が型の引数を受け取る 1 よりも大幅に異なるタスクを実行**二重**. オーバーロードにより、統一性のある名前付けが可能になり、プログラマは `print_sz` や `print_d` のような名前を作成する必要がなくなります。 次の表は、同じスコープ内の同じ名前を持つ関数を区別するために、C++ で関数宣言のどの部分が使用されるかをまとめたものです。  
  
### <a name="overloading-considerations"></a>オーバーロードに関する考慮事項  
  
|関数宣言要素|オーバーロードに使用されるかどうか|  
|----------------------------------|---------------------------|  
|関数の戻り値の型|いいえ|  
|引数の数|はい|  
|引数の型|はい|  
|省略記号の有無|はい|  
|`typedef` 名の使用|いいえ|  
|未指定の配列の範囲|いいえ|  
|**const**または`volatile`(下記参照)|はい|  
  
 関数は戻り値の型に基づいて識別できますが、同じ基準でオーバーロードすることはできません。  `Const`または`volatile`に適用するクラスで使用される場合をオーバー ロードに、基準としてのみ使用される、**この**関数の戻り値型ではなく、クラスへのポインター。  つまり、オーバー ロードは場合にのみ、 **const**または`volatile`キーワード宣言内の関数の引数リストに依存します。  
  
## <a name="example"></a>例  
 次の例は、どのようにオーバーロードが使用できるかを示しています。  
  
```  
// function_overloading.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <math.h>  
  
// Prototype three print functions.  
int print( char *s );                  // Print a string.  
int print( double dvalue );            // Print a double.  
int print( double dvalue, int prec );  // Print a double with a  
//  given precision.  
using namespace std;  
int main( int argc, char *argv[] )  
{  
const double d = 893094.2987;  
if( argc < 2 )  
    {  
// These calls to print invoke print( char *s ).  
print( "This program requires one argument." );  
print( "The argument specifies the number of" );  
print( "digits precision for the second number" );  
print( "printed." );  
exit(0);  
    }  
  
// Invoke print( double dvalue ).  
print( d );  
  
// Invoke print( double dvalue, int prec ).  
print( d, atoi( argv[1] ) );  
}  
  
// Print a string.  
int print( char *s )  
{  
cout << s << endl;  
return cout.good();  
}  
  
// Print a double in default precision.  
int print( double dvalue )  
{  
cout << dvalue << endl;  
return cout.good();  
}  
  
// Print a double in specified precision.  
//  Positive numbers for precision indicate how many digits  
//  precision after the decimal point to show. Negative  
//  numbers for precision indicate where to round the number  
//  to the left of the decimal point.  
int print( double dvalue, int prec )  
{  
// Use table-lookup for rounding/truncation.  
static const double rgPow10[] = {   
10E-7, 10E-6, 10E-5, 10E-4, 10E-3, 10E-2, 10E-1, 10E0,  
10E1,  10E2,  10E3,  10E4, 10E5,  10E6  
    };  
const int iPowZero = 6;  
// If precision out of range, just print the number.  
if( prec < -6 || prec > 7 )  
return print( dvalue );  
// Scale, truncate, then rescale.  
dvalue = floor( dvalue / rgPow10[iPowZero - prec] ) *  
rgPow10[iPowZero - prec];  
cout << dvalue << endl;  
return cout.good();  
}  
```  
  
 上記のコードは、ファイル スコープでの `print` 関数のオーバーロードを示しています。  
  
 既定の引数は、関数型の一部とは見なされません。 したがって、オーバーロードされた関数の選択では使用されません。 既定の引数のみが異なる 2 つの関数は、オーバーロードされた関数ではなく複数の定義と見なされます。  
  
 既定の引数は、オーバーロードされた演算子に指定することはできません。  
  
  
## <a name="argument-matching"></a>引数の一致  
 オーバーロード関数は、関数呼び出しで指定された引数に最も合った現在のスコープ内の関数宣言に対して選択します。 適切な関数がある場合、その関数が呼び出されます。 "適切" とは、このコンテキストでは次のいずれかを意味します。  
  
-   厳密な一致が見つかりませんでした。  
  
-   単純変換が実行されました。  
  
-   整数の上位変換が実行されました。  
  
-   目的の引数の型への標準変換が存在します。  
  
-   目的の引数の型へのユーザー定義の変換 (変換演算子またはコンストラクター) が存在します。  
  
-   省略記号によって表される引数が見つかりませんでした。  
  
 コンパイラは、引数ごとに候補関数のセットを作成します。 候補関数は、その位置の実引数を仮引数の型に変換できる関数です。  
  
 一連の "最も一致する関数" は各引数にビルドされ、選択した関数はすべての設定の交差部分です。 交差部分に複数の関数が含まれている場合、オーバーロードはあいまいで、エラーが生成されます。 最終的に選択された関数は、少なくとも 1 つの引数についてはグループ内のどの関数よりも優れた一致です。 このようにならない場合 (明確な勝者が存在しない場合)、関数呼び出しでエラーが生成されます。  
  
 次の宣言を考えます (関数には、以下の説明での識別のために `Variant 1`、`Variant 2`、および `Variant 3` とマーク付けしています)。  
  
```  
Fraction &Add( Fraction &f, long l );       // Variant 1  
Fraction &Add( long l, Fraction &f );       // Variant 2  
Fraction &Add( Fraction &f, Fraction &f );  // Variant 3  
  
Fraction F1, F2;  
```  
  
 次のステートメントを考えます。  
  
```  
F1 = Add( F2, 23 );  
```  
  
 前のステートメントは 2 つのセットをビルドします。  
  
|セット 1: Fraction 型の第 1 引数を持つ候補関数|セット 2: 第 2 引数を int 型に変換できる候補関数|  
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------|  
|バリアント 1|バリアント 1 (`int` は、標準変換を使用して `long` に変換することができます)|  
|バリアント 3||  
  
 セット 2 の関数は、実際のパラメーターの型から仮パラメーターの型に暗黙的に変換される関数です。このような関数の中には、実際のパラメーターの型を仮パラメーターの型に変換する "コスト" が最も小さい関数が 1 つあります。  
  
 これら 2 つのセットの積集合は、バリアント 1 です。 あいまいな関数呼び出しの例は次のとおりです。  
  
```  
F1 = Add( 3, 6 );  
```  
  
 前の関数呼び出しは次のセットをビルドします。  
  
|セット 1: int 型の第 1 引数を持つ候補関数|セット 2: int 型の第 2 引数を持つ候補関数|  
|---------------------------------------------------------------------|----------------------------------------------------------------------|  
|バリアント 2 (`int` は、標準変換を使用して `long` に変換することができます)|バリアント 1 (`int` は、標準変換を使用して `long` に変換することができます)|  
  
 この 2 つのセット間の積集合が空であることに注意してください。 このため、エラー メッセージが生成されます。  
  
 引数の一致を使用して関数 *n* は既定の引数と見なさ *n* +1 の個別の関数、それぞれ異なる数の引数にします。  
  
 省略記号 (...) はワイルドカードとして機能します。これは任意の実際の引数と一致します。 オーバーロード関数セットを非常に注意して設計しないと、これが多くのあいまいさの原因になる可能性があります。  
  
> [!NOTE]
>  オーバーロードされた関数のあいまいさは、関数呼び出しが出現するまで判断できません。 その時点で、設定は関数呼び出しの引数ごとに構築され、明確なオーバーロードがあるかどうかを確認できます。 これは、それらが特定の関数呼び出しによって呼び出されるまで、コードにあいまいさが残ることを意味しています。  
  
## <a name="argument-type-differences"></a>引数の型の違い  
 オーバーロード関数では、異なる初期化子を受け取る引数型が区別されます。 したがって、指定された型の引数とその型への参照は、オーバーロードの目的では同一であると見なされます。 これらが同一であると見なされるのは、同じ初期化子を受け取るためです。 たとえば、`max( double, double )` は `max( double &, double & )` と同じであると見なされます。 このような関数を 2 つ宣言すると、エラーが発生します。  
  
 同じ理由で、関数によって修飾された型の引数**const**または`volatile`のオーバー ロードの目的で、基本データ型とは異なる処理されません。  
  
 ただし、関数のメカニズムをオーバー ロードを区別できるで修飾される参照**const**と`volatile`および基本型への参照。 これにより、次のようなコードが可能となります。  
  
```  
// argument_type_differences.cpp  
// compile with: /EHsc /W3  
// C4521 expected  
#include <iostream>  
  
using namespace std;  
class Over {  
public:  
   Over() { cout << "Over default constructor\n"; }  
   Over( Over &o ) { cout << "Over&\n"; }  
   Over( const Over &co ) { cout << "const Over&\n"; }  
   Over( volatile Over &vo ) { cout << "volatile Over&\n"; }  
};  
  
int main() {  
   Over o1;            // Calls default constructor.  
   Over o2( o1 );      // Calls Over( Over& ).  
   const Over o3;      // Calls default constructor.  
   Over o4( o3 );      // Calls Over( const Over& ).  
   volatile Over o5;   // Calls default constructor.  
   Over o6( o5 );      // Calls Over( volatile Over& ).  
}  
```  
  
### <a name="output"></a>出力  
  
```  
Over default constructor  
Over&  
Over default constructor  
const Over&  
Over default constructor  
volatile Over&  
```  
  
 ポインター **const**と`volatile`オブジェクトも見なされます、基本データ型をポインターから別のオーバー ロードの目的でします。  
  
## <a name="argument-matching-and-conversions"></a>引数の一致と変換  
 コンパイラは、関数宣言の引数と実際の引数を照合するとき、厳密な一致が見つからない場合は、正しい型を取得するために標準またはユーザー定義の変換を指定できます。 変換は、次の規則に従って行われます。  
  
-   複数のユーザー定義変換を含む変換のシーケンスは考慮されません。  
  
-   中間変換を削除することによって簡略化できる変換のシーケンスは考慮されません。  
  
 変換の結果のシーケンスが存在する場合、それは最適な一致シーケンスと呼ばれます。 型のオブジェクトに変換するいくつかの方法がある`int`入力`unsigned long`標準変換を使用して (」に記載[標準変換](../cpp/standard-conversions.md))。  
  
-   `int` から `long` に変換してから、`long` から `unsigned long` に変換します。  
  
-   `int` から `unsigned long` に変換します。  
  
 最初のシーケンスは、目的を達成しますが、さらに短いシーケンスが存在するので、最適の一致シーケンスではありません。  
  
 次の表は、どのシーケンスが最適な一致かの判断に一定の効果を持つ、単純変換と呼ばれる変換を示しています。 単純変換がシーケンスの選択に影響を与える例については、表の後で説明します。  
  
### <a name="trivial-conversions"></a>単純変換  
  
|変換前の型|変換後の型|  
|-----------------------|---------------------|  
|*型名*|*型名***&**|  
|*型名***&**|*型名*|  
|*型名* ****|*型名\**|  
|*型名* **(** *引数リスト* **)**|**(** *\*型名* **) (** *引数リスト* **)**|  
|*型名*|**const** *型名*|  
|*型名*|`volatile`*型名*|  
|*型名\**|**const** *型名\**|  
|*型名\**|`volatile`*型名\**|  
  
 変換が試行されたシーケンスは次のとおりです。  
  
1.  完全一致。 関数の呼び出しに使用された型と関数プロトタイプで宣言された型の完全な一致は、常に最適な一致です。 単純変換のシーケンスは、完全一致として分類されます。 ただし、次の変換を実行しないシーケンスは、実行するシーケンスよりも優先順位が高いと見なされます。  
  
    -   ポインターへのポインターから**const** (`type`  **\*** に**const** `type`  **\*** ).  
  
    -   ポインターへのポインターから`volatile`(`type`  **\*** に`volatile` `type`  **\*** )。  
  
    -   参照への参照から**const** (`type`  **&** に**const** `type`  **&** ).  
  
    -   参照への参照から`volatile`(`type`  **&** に`volatile` `type`  **&** )。  
  
2.  上位変換を使用した一致。 のみ整数の上位変換からの変換を含む完全一致として分類されていない任意のシーケンス**float**に**二重**、および単純変換が上位変換を使用して、一致として分類します。 完全一致による一致ほどではありませんが、標準変換を使用するより上位変換を使用する方が一致の程度が高くなります。  
  
3.  標準変換を使用した一致。 完全一致としても、標準変換および単純変換だけを含む上位変換を使用した一致としても分類されないシーケンスは、標準変換を使用した一致として分類されます。 このカテゴリ内では、次の規則が適用されます。  
  
    -   ポインターから直接または間接基底クラスへのポインターに、派生クラスへの変換が変換することをお勧め**void \*** または**const void \***です。  
  
    -   派生クラスへのポインターから基底クラスへのポインターに変換すると、基底クラスが直接基底クラスに近ければ近いほど、一致の程度が向上します。 次の図に示すクラスの階層構造を考えます。  
  
 ![優先変換](../cpp/media/vc391t1.gif "vc391T1")  
優先される変換を示すグラフ  
  
 `D*` 型から `C*` 型への変換は、`D*` 型から `B*` 型への変換よりも適しています。 同様に、`D*` 型から `B*` 型への変換は、`D*` 型から `A*` 型への変換よりも適しています。  
  
 この同じ規則が、参照変換に適用されます。 `D&` 型から `C&` 型への変換は、`D&` 型から `B&` 型への変換などよりも適しています。  
  
 この同じ規則は、ポインターからメンバーへの変換にも適用されます。 `T D::*` 型から `T C::*` 型への変換は、`T D::*` 型から `T B::*` 型への変換などよりも適しています (`T` はメンバーの型)。  
  
 上記の規則は、派生の特定のパスに沿ってのみ適用されます。 次の図に示すグラフについて考えます。  
  
 ![マルチ &#45; 優先変換を示す継承](../cpp/media/vc391t2.gif "vc391T2")  
優先される変換を示す複数継承のグラフ  
  
 `C*` 型から `B*` 型への変換は、`C*` 型から `A*` 型への変換よりも適しています。 理由は、これらが同じパスにあり、`B*` の方が近いからです。 しかし、`C*` 型から `D*` 型への変換が、`A*` 型への変換より適しているというわけではありません。これらの変換は違うパスをたどるので、優先順位が決まらないからです。  
  
1.  ユーザー定義変換を使用した一致。 これは、完全一致、上位変換を使用した一致、または標準変換を使用した一致のどれにも分類できないシーケンスです。 このシーケンスには、ユーザー定義の変換、標準変換、またはユーザー定義の変換を使用した一致として分類される単純変換だけが含まれます。 ユーザー定義の変換による一致は、省略記号を含む一致より程度の高い一致と見なされますが、標準変換による一致ほど程度の高い一致とは見なされません。  
  
2.  省略記号を使用した一致。 宣言内の省略記号に一致するシーケンスは、すべて省略記号による一致として分類されます。 これは最も弱い一致と見なされます。  
  
 組み込みの上位変換または変換が存在しない場合、ユーザー定義の変換が適用されます。 これらの変換は照合する引数の型に基づいて選択されます。 次のコードがあるとします。  
  
```  
// argument_matching1.cpp  
class UDC  
{  
public:  
   operator int()  
   {  
      return 0;  
   }  
   operator long();  
};  
  
void Print( int i )  
{  
};  
  
UDC udc;  
  
int main()  
{  
   Print( udc );  
}  
```  
  
 クラスの使用可能なユーザー定義の変換`UDC`型からは`int`および種類**長い**です。 したがって、コンパイラは照合対象のオブジェクトの型、`UDC` に応じて変換を検討します。 `int` への変換は存在しているため、それが選択されています。  
  
 引数の照合処理中は、引数とユーザー定義変換の結果の両方に標準変換を適用できます。 したがって、次のコードは機能します。  
  
```  
void LogToFile( long l );  
...  
UDC udc;  
LogToFile( udc );  
```  
  
 前の例では、ユーザー定義の変換の場合、**演算子 long**、変換が呼び出され`udc`入力**長い**です。 場合を入力するユーザー定義変換なし**長い**されていた定義されている場合、変換が進む次のように: 型`UDC`型に変換されますが`int`ユーザー定義の変換を使用します。 型から標準の変換、`int`入力**長い**が適用されて、宣言の引数の一致するようにします。  
  
 引数の一致にユーザー定義の変換が必要な場合、最適な一致を評価するときに標準の変換は使用されません。 このことは、複数の候補関数がユーザー定義変換を必要としている場合でも同じです。このような場合、それらの候補関数は等しいと判断されます。 例:  
  
```  
// argument_matching2.cpp  
// C2668 expected  
class UDC1  
{  
public:  
   UDC1( int );  // User-defined conversion from int.  
};  
  
class UDC2  
{  
public:  
   UDC2( long ); // User-defined conversion from long.  
};  
  
void Func( UDC1 );  
void Func( UDC2 );  
  
int main()  
{  
   Func( 1 );  
}  
```  
  
 `Func` のどちらのバージョンにも、`int` 型をクラス型の引数に変換するユーザー定義変換が必要です。 発生しうる変換は、次のとおりです。  
  
-   `int` 型から `UDC1` 型への変換 (ユーザー定義変換)。  
  
-   型から変換する`int`入力**長い**; 型に変換し、 `UDC2` (2 段階の変換)。  
  
 2 番目の場合は標準変換とユーザー定義の変換が必要ですが、2 つの変換は同じと見なされます。  
  
> [!NOTE]
>  ユーザー定義の変換は、コンストラクションによる変換または初期化による変換 (変換関数) と見なされます。 どちらの方法も、最適一致を検討する際には等しいと判断されます。  
  
## <a name="argument-matching-and-the-this-pointer"></a>引数一致と this ポインター  
 クラス メンバー関数は `static` として宣言されているかどうかによって処理が異なります。 非静的関数は `this` ポインターを提供する暗黙的な引数を持つため、非静的関数には静的関数より引数が 1 つ多いと見なされます。それ以外は、同じように宣言されます。  
  
 これらの非静的メンバー関数では、関数の呼び出しに使用されるオブジェクト型に暗黙の `this` ポインターが一致する必要があります。オーバーロードされた演算子の場合は、最初の引数が演算子の適用先のオブジェクトに一致する必要があります  (オーバー ロードされた演算子の詳細については、次を参照してください[オーバー ロードされた演算子](../cpp/operator-overloading.md)。)。  
  
 オーバーロードされた関数の他の引数とは異なり、`this` ポインター引数のマッチング時には、一時オブジェクトの導入も変換も行われません。  
  
 ときに、`->`メンバー選択演算子はクラスのメンバー関数にアクセスするために使用`class_name`、`this`ポインター引数の型を持つ`class_name * const`します。 メンバーとして宣言されている場合`const`または`volatile`、種類は、`const class_name * const`と`volatile class_name * const`、それぞれします。  
  
 `.` メンバー選択演算子は、暗黙の `&` (アドレス) 演算子がオブジェクト名の前に付けられている場合を除き、まったく同じ方法で動作します 次の例では、このしくみを説明します。  
  
```  
// Expression encountered in code  
obj.name  
  
// How the compiler treats it  
(&obj)->name  
```  
  
 引数マッチングに関して、`->*` 演算子および `.*` (メンバーへのポインター) 演算子の左オペランドは `.` 演算子および `->` (メンバー選択) 演算子と同じ方法で処理されます。  
  
## <a name="restrictions"></a>制約  
 許容可能なオーバーロード関数のセットには複数の制限が適用されます。  
  
-   一連のオーバーロードされた関数の 2 つの関数には、異なる引数リストが必要です。  
  
-   オーバーロードは、戻り値の型だけに基づいて同じ型の引数リストと共に機能するエラーです。  
  
     **Microsoft 固有の仕様**  
  
 オーバー ロードできます**new 演算子**情報だけを頼りに、に基づいて戻り値の型: 指定したメモリ モデル修飾子に基づいて具体的には、します。  
  
**Microsoft 固有の仕様はここまで**  
  
-   メンバー関数は、静的である一方と静的でない他方に基づいてのみオーバーロードすることはできません。  
  
-   `typedef` 宣言は、新しい型を定義しません。この宣言は、既存の型のシノニムを導入します。 オーバーロード メカニズムには影響しません。 次のコードがあるとします。  
  
    ```  
    typedef char * PSTR;  
  
    void Print( char *szToPrint );  
    void Print( PSTR szToPrint );  
    ```  
  
     先行する 2 つの関数の引数リストはまったく同じです。 `PSTR`型のシノニムは、 **char \***です。 メンバーのスコープでは、このコードによりエラーが発生します。  
  
-   列挙型は別個の型です。また、オーバーロードされた関数を識別するために使用できます。  
  
-   型 "array of " と "pointer to" は、オーバーロード関数を識別する目的では同一と見なされます。 これは、単独で次元設定された配列だけに当てはまります。 したがって、次のオーバーロードされた関数は競合し、エラー メッセージを生成します。  
  
    ```  
    void Print( char *szToPrint );  
    void Print( char szToPrint[] );  
    ```  
  
     次元配列の乗算では、2 番目以降のすべてのディメンションは、型の一部と見なされます。 したがって、オーバーロードされた関数を識別するために使用されます。  
  
    ```  
    void Print( char szToPrint[] );  
    void Print( char szToPrint[][7] );  
    void Print( char szToPrint[][9][42] );  
    ```  
  
## <a name="declaration-matching"></a>宣言の一致  
 同じスコープ内で同じ名前の 2 つの関数宣言は、同じ関数またはオーバーロードされる 2 種類の関数を参照できます。 宣言の引数リストに (前のセクションで説明したように) 型が同じ引数が含まれている場合、関数宣言は同じ関数を参照しています。 それ以外の場合は、オーバーロードを使用して選択された 2 つの異なる関数を参照します。  
  
 クラス スコープは、厳密に遵守されます。このため、基底クラスで宣言された関数は、派生クラスで宣言された関数と同じスコープ内にありません。 派生クラスの関数が基底クラスの関数と同じ名前で宣言されると、オーバーロードが発生するのではなく、派生クラスの関数で基底クラスの関数が非表示になります。  
  
 ブロック スコープは、厳密に遵守されます。このため、ファイル スコープで宣言された関数は、ローカルで宣言された関数と同じスコープ内にありません。 ローカルで宣言された関数の名前がファイル スコープで宣言された関数と同じ場合、ローカルで宣言された関数では、オーバーロードが発生する代わりに、ファイル スコープ関数を非表示にします。 例:  
  
```  
// declaration_matching1.cpp  
// compile with: /EHsc  
#include <iostream>  
  
using namespace std;  
void func( int i )  
{  
    cout << "Called file-scoped func : " << i << endl;  
}  
  
void func( char *sz )  
{  
   cout << "Called locally declared func : " << sz << endl;  
}  
  
int main()  
{  
   // Declare func local to main.  
   extern void func( char *sz );  
  
   func( 3 );   // C2664 Error. func( int ) is hidden.  
   func( "s" );  
}  
```  
  
 前のコードは、関数 `func` からの 2 つの定義を示します。 `char *` 型の引数を受け受ける定義は、`main` ステートメントのため、`extern` にローカルです。 したがって、型 `int` の引数を受け取る定義は表示されず、`func` への最初の呼び出しはエラーになります。  
  
 オーバーロードされたメンバー関数の場合は、関数の各バージョンにそれぞれ異なるアクセス権限を与えることができます。 これらは、依然として外側のクラスのスコープ内にあると見なされます。このため、オーバーロードされた関数です。 `Deposit` メンバー関数をオーバーロードしている次のコードを考えます。1 つのバージョンはパブリック、もう 1 つのバージョンはプライベートです。  
  
 このサンプルの目的は、預金を実行するために正しいパスワードが必要となる `Account` クラスを提供することです。 これは、オーバーロードを使用して行われます。  
  
 `Deposit` 内の `Account::Deposit` への呼び出しで、プライベート メンバー関数が呼び出されることに注意してください。 `Account::Deposit` はメンバー関数であり、クラスのプライベート メンバーにアクセスできるため、この呼び出しは適切です。  
  
```  
// declaration_matching2.cpp  
class Account  
{  
public:  
   Account()  
   {  
   }  
   double Deposit( double dAmount, char *szPassword );  
  
private:  
   double Deposit( double dAmount )  
   {  
      return 0.0;  
   }  
   int Validate( char *szPassword )  
   {  
      return 0;  
   }  
  
};  
  
int main()  
{  
    // Allocate a new object of type Account.  
    Account *pAcct = new Account;  
  
    // Deposit $57.22. Error: calls a private function.  
    // pAcct->Deposit( 57.22 );  
  
    // Deposit $57.22 and supply a password. OK: calls a  
    //  public function.  
    pAcct->Deposit( 52.77, "pswd" );  
}  
  
double Account::Deposit( double dAmount, char *szPassword )  
{  
   if ( Validate( szPassword ) )  
      return Deposit( dAmount );  
   else  
      return 0.0;  
}  
```  
  
## <a name="see-also"></a>関連項目  
 [関数 (C++)](../cpp/functions-cpp.md)