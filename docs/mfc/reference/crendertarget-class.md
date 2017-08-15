---
title: "CRenderTarget クラス |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CRenderTarget
- AFXRENDERTARGET/CRenderTarget
- AFXRENDERTARGET/CRenderTarget::CRenderTarget
- AFXRENDERTARGET/CRenderTarget::Attach
- AFXRENDERTARGET/CRenderTarget::BeginDraw
- AFXRENDERTARGET/CRenderTarget::Clear
- AFXRENDERTARGET/CRenderTarget::COLORREF_TO_D2DCOLOR
- AFXRENDERTARGET/CRenderTarget::CreateCompatibleRenderTarget
- AFXRENDERTARGET/CRenderTarget::Destroy
- AFXRENDERTARGET/CRenderTarget::Detach
- AFXRENDERTARGET/CRenderTarget::DrawBitmap
- AFXRENDERTARGET/CRenderTarget::DrawEllipse
- AFXRENDERTARGET/CRenderTarget::DrawGeometry
- AFXRENDERTARGET/CRenderTarget::DrawGlyphRun
- AFXRENDERTARGET/CRenderTarget::DrawLine
- AFXRENDERTARGET/CRenderTarget::DrawRectangle
- AFXRENDERTARGET/CRenderTarget::DrawRoundedRectangle
- AFXRENDERTARGET/CRenderTarget::DrawText
- AFXRENDERTARGET/CRenderTarget::DrawTextLayout
- AFXRENDERTARGET/CRenderTarget::EndDraw
- AFXRENDERTARGET/CRenderTarget::FillEllipse
- AFXRENDERTARGET/CRenderTarget::FillGeometry
- AFXRENDERTARGET/CRenderTarget::FillMesh
- AFXRENDERTARGET/CRenderTarget::FillOpacityMask
- AFXRENDERTARGET/CRenderTarget::FillRectangle
- AFXRENDERTARGET/CRenderTarget::FillRoundedRectangle
- AFXRENDERTARGET/CRenderTarget::Flush
- AFXRENDERTARGET/CRenderTarget::GetAntialiasMode
- AFXRENDERTARGET/CRenderTarget::GetDpi
- AFXRENDERTARGET/CRenderTarget::GetMaximumBitmapSize
- AFXRENDERTARGET/CRenderTarget::GetPixelFormat
- AFXRENDERTARGET/CRenderTarget::GetPixelSize
- AFXRENDERTARGET/CRenderTarget::GetRenderTarget
- AFXRENDERTARGET/CRenderTarget::GetSize
- AFXRENDERTARGET/CRenderTarget::GetTags
- AFXRENDERTARGET/CRenderTarget::GetTextAntialiasMode
- AFXRENDERTARGET/CRenderTarget::GetTextRenderingParams
- AFXRENDERTARGET/CRenderTarget::GetTransform
- AFXRENDERTARGET/CRenderTarget::IsSupported
- AFXRENDERTARGET/CRenderTarget::IsValid
- AFXRENDERTARGET/CRenderTarget::PopAxisAlignedClip
- AFXRENDERTARGET/CRenderTarget::PopLayer
- AFXRENDERTARGET/CRenderTarget::PushAxisAlignedClip
- AFXRENDERTARGET/CRenderTarget::PushLayer
- AFXRENDERTARGET/CRenderTarget::RestoreDrawingState
- AFXRENDERTARGET/CRenderTarget::SaveDrawingState
- AFXRENDERTARGET/CRenderTarget::SetAntialiasMode
- AFXRENDERTARGET/CRenderTarget::SetDpi
- AFXRENDERTARGET/CRenderTarget::SetTags
- AFXRENDERTARGET/CRenderTarget::SetTextAntialiasMode
- AFXRENDERTARGET/CRenderTarget::SetTextRenderingParams
- AFXRENDERTARGET/CRenderTarget::SetTransform
- AFXRENDERTARGET/CRenderTarget::VerifyResource
- AFXRENDERTARGET/CRenderTarget::m_lstResources
- AFXRENDERTARGET/CRenderTarget::m_pRenderTarget
- AFXRENDERTARGET/CRenderTarget::m_pTextFormatDefault
dev_langs:
- C++
helpviewer_keywords:
- CRenderTarget class
ms.assetid: 30d1607d-68d3-4d14-ac36-fdbd0ef903a1
caps.latest.revision: 17
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
ms.translationtype: Machine Translation
ms.sourcegitcommit: 0e0c08ddc57d437c51872b5186ae3fc983bb0199
ms.openlocfilehash: 6f77d482e7ee3bf0798ad488067893b3712aac62
ms.contentlocale: ja-jp
ms.lasthandoff: 02/24/2017

---
# <a name="crendertarget-class"></a>CRenderTarget クラス
ID2D1RenderTarget のラッパーです。  
  
## <a name="syntax"></a>構文  
  
```  
class CRenderTarget : public CObject;  
```  
  
## <a name="members"></a>メンバー  
  
### <a name="public-constructors"></a>パブリック コンストラクター  
  
|名前|説明|  
|----------|-----------------|  
|[CRenderTarget::CRenderTarget](#crendertarget)|CRenderTarget オブジェクトを構築します。|  
|[CRenderTarget:: ~ CRenderTarget](#crendertarget__~crendertarget)|デストラクターです。 レンダー ターゲット オブジェクトが破棄されるときに呼び出されます。|  
  
### <a name="public-methods"></a>パブリック メソッド  
  
|名前|説明|  
|----------|-----------------|  
|[CRenderTarget::Attach](#attach)|既存の接続は、ターゲット オブジェクトのインターフェイスをレンダリングします。|  
|[CRenderTarget::BeginDraw](#begindraw)|このレンダー ターゲット上に描画を開始します。|  
|[CRenderTarget::Clear](#clear)|指定された色の描画領域をクリアします。|  
|[CRenderTarget::COLORREF_TO_D2DCOLOR](#colorref_to_d2dcolor)|GDI カラーとアルファ値を D2D1_COLOR_F オブジェクトに変換します。|  
|[CRenderTarget::CreateCompatibleRenderTarget](#createcompatiblerendertarget)|現在のレンダー ターゲットと互換性がある中間のオフスクリーン描画中に使用するため、新しいビットマップ レンダー ターゲットを作成します。|  
|[CRenderTarget::Destroy](#destroy)|1 つまたは複数のリソースを削除します。|  
|[CRenderTarget::Detach](#detach)|レンダー ターゲット インターフェイス オブジェクトからのデタッチします。|  
|[CRenderTarget::DrawBitmap](#drawbitmap)|指定した IDWriteTextLayout オブジェクトによって記述されたフォーマットされたテキストを描画します。|  
|[CRenderTarget::DrawEllipse](#drawellipse)|指定した線のスタイルを使用して、指定された楕円のアウトラインを描画します。|  
|[CRenderTarget::DrawGeometry](#drawgeometry)|指定した線のスタイルを使用して指定された geometry の輪郭を描画します。|  
|[CRenderTarget::DrawGlyphRun](#drawglyphrun)|指定したグリフを描画します。|  
|[CRenderTarget::DrawLine](#drawline)|指定した線のスタイルを使用して指定した点を結ぶ直線を描画します。|  
|[CRenderTarget::DrawRectangle](#drawrectangle)|指定した寸法と線のスタイルを持つ四角形のアウトラインを描画します。|  
|[CRenderTarget::DrawRoundedRectangle](#drawroundedrectangle)|指定した線のスタイルを使用して、指定した角の丸い四角形のアウトラインを描画します。|  
|[CRenderTarget::DrawText](#drawtext)|IDWriteTextFormat オブジェクトによって提供される形式の情報を使用して、指定したテキストを描画します。|  
|[CRenderTarget::DrawTextLayout](#drawtextlayout)|指定した IDWriteTextLayout オブジェクトによって記述されたフォーマットされたテキストを描画します。|  
|[CRenderTarget::EndDraw](#enddraw)|レンダー ターゲットに対して描画操作を終了し、現在のエラー状態と関連付けられているタグを示します。|  
|[CRenderTarget::FillEllipse](#fillellipse)|指定された楕円の内部を描画します。|  
|[CRenderTarget::FillGeometry](#fillgeometry)|指定された geometry の内部を描画します。|  
|[CRenderTarget::FillMesh](#fillmesh)|指定したメッシュの内部を描画します。|  
|[CRenderTarget::FillOpacityMask](#fillopacitymask)|ブラシへの指定したビットマップが示す不透明度マスクを適用し、そのブラシを使用して、レンダー ターゲットの領域を描画します。|  
|[CRenderTarget::FillRectangle](#fillrectangle)|指定された四角形の内部を描画します。|  
|[CRenderTarget::FillRoundedRectangle](#fillroundedrectangle)|指定した角の丸い四角形の内部を描画します。|  
|[CRenderTarget::Flush](#flush)|すべての保留中の描画コマンドを実行します。|  
|[CRenderTarget::GetAntialiasMode](#getantialiasmode)|テキスト以外の描画操作の現在の (アンチエイリアシング) モードを取得します。|  
|[CRenderTarget::GetDpi](#getdpi)|レンダリング ターゲットのドット/インチ (DPI) を返します|  
|[CRenderTarget::GetMaximumBitmapSize](#getmaximumbitmapsize)|レンダー ターゲットでサポートされている任意の&1; つのビットマップ ディメンションのデバイスに依存しない単位 (ピクセル単位) で最大サイズを取得します。|  
|[CRenderTarget::GetPixelFormat](#getpixelformat)|レンダー ターゲットのピクセル形式とアルファ モードを取得します。|  
|[CRenderTarget::GetPixelSize](#getpixelsize)|デバイス ピクセル単位で、レンダー ターゲットのサイズを返します|  
|[CRenderTarget::GetRenderTarget](#getrendertarget)|返します。 ID2D1RenderTarget インターフェイス|  
|[CRenderTarget::GetSize](#getsize)|デバイスに依存しないピクセル単位で、レンダー ターゲットのサイズを返します|  
|[CRenderTarget::GetTags](#gettags)|以降の描画操作のラベルを取得します。|  
|[CRenderTarget::GetTextAntialiasMode](#gettextantialiasmode)|テキストとグリフが描画操作の現在の (アンチエイリアシング) モードを取得します。|  
|[CRenderTarget::GetTextRenderingParams](#gettextrenderingparams)|レンダー ターゲットの現在のテキストのレンダリング オプションを取得します。|  
|[CRenderTarget::GetTransform](#gettransform)|既存の変換を置き換える、レンダー ターゲットを指定した変換を適用します。 後続のすべての描画操作は、変換された空間で発生します。|  
|[CRenderTarget::IsSupported](#issupported)|レンダー ターゲットが指定されたプロパティをサポートするかどうかを示します|  
|[CRenderTarget::IsValid](#isvalid)|リソースの有効性のチェック|  
|[CRenderTarget::PopAxisAlignedClip](#popaxisalignedclip)|レンダー ターゲットから最後の軸に沿ったクリップを削除します。 このメソッドが呼び出された後、クリップが以降の描画操作に適用されていません。|  
|[CRenderTarget::PopLayer](#poplayer)|最後の PushLayer で指定されているレイヤーの描画操作のリダイレクトを停止を呼び出します。|  
|[CRenderTarget::PushAxisAlignedClip](#pushaxisalignedclip)|レンダー ターゲットから最後の軸に沿ったクリップを削除します。 このメソッドが呼び出された後、クリップが以降の描画操作に適用されていません。|  
|[CRenderTarget::PushLayer](#pushlayer)|PopLayer が呼び出されるまでは、後続のすべての描画操作を受信できるように、レンダー ターゲットに指定したレイヤーを追加します。|  
|[CRenderTarget::RestoreDrawingState](#restoredrawingstate)|指定した ID2D1DrawingStateBlock のレンダー ターゲットの描画状態を設定します。|  
|[CRenderTarget::SaveDrawingState](#savedrawingstate)|指定した ID2D1DrawingStateBlock に現在の描画状態を保存します。|  
|[CRenderTarget::SetAntialiasMode](#setantialiasmode)|レンダー ターゲットの (アンチエイリアシング) モードを設定します。 アンチ エイリアス処理モードは、テキストおよびグリフが描画操作を除く、すべての後続描画操作に適用されます。|  
|[CRenderTarget::SetDpi](#setdpi)|ドット/インチ (DPI) のレンダー ターゲットを設定します。|  
|[CRenderTarget::SetTags](#settags)|以降の描画操作のラベルを指定します。|  
|[CRenderTarget::SetTextAntialiasMode](#settextantialiasmode)|後続のテキストおよびグリフの描画操作を使用する (アンチエイリアシング) モードを指定します。|  
|[CRenderTarget::SetTextRenderingParams](#settextrenderingparams)|すべての後続のテキストとグリフが描画操作に適用するテキストのレンダリング オプションを指定します。|  
|[CRenderTarget::SetTransform](#settransform)|オーバーロードされます。 既存の変換を置き換える、レンダー ターゲットを指定した変換を適用します。 後続のすべての描画操作は、変換された空間で発生します。|  
  
### <a name="protected-methods"></a>プロテクト メソッド  
  
|名前|説明|  
|----------|-----------------|  
|[CRenderTarget::VerifyResource](#verifyresource)|CD2DResource オブジェクトの有効性; を検証します。存在しない場合は、オブジェクトを作成します。|  
  
### <a name="public-operators"></a>パブリック演算子  
  
|名前|説明|  
|----------|-----------------|  
|[CRenderTarget::operator ID2D1RenderTarget *](#operator_id2d1rendertarget_star)|返します。 ID2D1RenderTarget インターフェイス|  
  
### <a name="protected-data-members"></a>プロテクト データ メンバー  
  
|名前|説明|  
|----------|-----------------|  
|[CRenderTarget::m_lstResources](#m_lstresources)|CD2DResource のオブジェクトへのポインターのリスト。|  
|[CRenderTarget::m_pRenderTarget](#m_prendertarget)|ID2D1RenderTarget オブジェクトへのポインター。|  
|[CRenderTarget::m_pTextFormatDefault](#m_ptextformatdefault)|既定のテキスト形式を格納している CD2DTextFormat のオブジェクトへのポインター。|  
  
## <a name="inheritance-hierarchy"></a>継承階層  
 [CObject](../../mfc/reference/cobject-class.md)  
  
 [CRenderTarget](../../mfc/reference/crendertarget-class.md)  
  
## <a name="requirements"></a>要件  
 **ヘッダー:** afxrendertarget.h  
  
##  <a name="_dtorcrendertarget"></a>CRenderTarget:: ~ CRenderTarget  
 デストラクターです。 レンダー ターゲット オブジェクトが破棄されるときに呼び出されます。  
  
```  
virtual ~CRenderTarget();
```  
  
##  <a name="attach"></a>CRenderTarget::Attach  
 既存の接続は、ターゲット オブジェクトのインターフェイスをレンダリングします。  
  
```  
void Attach(ID2D1RenderTarget* pRenderTarget);
```  
  
### <a name="parameters"></a>パラメーター  
 `pRenderTarget`  
 既存のレンダー ターゲットのインターフェイスです。 NULL にすることはできません。  
  
##  <a name="begindraw"></a>CRenderTarget::BeginDraw  
 このレンダー ターゲット上に描画を開始します。  
  
```  
void BeginDraw();
```  
  
##  <a name="clear"></a>CRenderTarget::Clear  
 指定された色の描画領域をクリアします。  
  
```  
void Clear(D2D1_COLOR_F color);
```  
  
### <a name="parameters"></a>パラメーター  
 `color`  
 描画領域をクリアする色。  
  
##  <a name="colorref_to_d2dcolor"></a>CRenderTarget::COLORREF_TO_D2DCOLOR  
 GDI カラーとアルファ値を D2D1_COLOR_F オブジェクトに変換します。  
  
```  
static D2D1_COLOR_F COLORREF_TO_D2DCOLOR(
    COLORREF color,  
    int nAlpha = 255);
```  
  
### <a name="parameters"></a>パラメーター  
 `color`  
 RGB 値。  
  
 `nAlpha`  
  
### <a name="return-value"></a>戻り値  
 D2D1_COLOR_F 値です。  
  
##  <a name="createcompatiblerendertarget"></a>CRenderTarget::CreateCompatibleRenderTarget  
 現在のレンダー ターゲットと互換性がある中間のオフスクリーン描画中に使用するため、新しいビットマップ レンダー ターゲットを作成します。  
  
```  
BOOL CreateCompatibleRenderTarget(
    CBitmapRenderTarget& bitmapTarget,  
    CD2DSizeF sizeDesired = CD2DSizeF(0., 0.), 
    CD2DSizeU sizePixelDesired = CD2DSizeU(0, 0), 
    D2D1_PIXEL_FORMAT* desiredFormat = NULL,  
    D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS options = D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_NONE);
```  
  
### <a name="parameters"></a>パラメーター  
 `bitmapTarget`  
 このメソッドが戻るときに、新しいビットマップ レンダリング ターゲットへのポインターのアドレスを格納します。 このパラメーターは初期化せずに渡されます。  
  
 `sizeDesired`  
 目的のサイズ (ピクセル) の場合は、元のさまざまなことがデバイスに依存しない新しいレンダー ターゲットのでは、レンダリング ターゲット、または NULL。 詳細については、「解説」を参照してください。  
  
 `sizePixelDesired`  
 ピクセルの場合は、元のさまざまなことがで新しいレンダー ターゲットの目的のサイズは、レンダリング ターゲット、または NULL。 詳細については、「解説」を参照してください。  
  
 `desiredFormat`  
 目的のピクセル形式と、新しいアルファ モードは、レンダリング ターゲット、または NULL。 DXGI_FORMAT_UNKNOWN にピクセル形式が設定されている場合、またはこのパラメーターが null の場合は、新しいレンダー ターゲットは、元のレンダー ターゲットとして同一のピクセル形式を使用します。 アルファ モードは D2D1_ALPHA_MODE_UNKNOWN、またはこのパラメーターが NULL、D2D1_ALPHA_MODE_PREMULTIPLIED が新しいレンダー ターゲットのアルファ モードに既定値です。 サポートされているピクセル形式については、ピクセル形式のサポートとアルファ モードを参照してください。  
  
 `options`  
 新しいレンダー ターゲットは、GDI と互換性があるかどうかを指定する値。  
  
### <a name="return-value"></a>戻り値  
 メソッドが成功した場合、TRUE を返します。 それ以外の場合、FALSE を返します。  
  
##  <a name="crendertarget"></a>CRenderTarget::CRenderTarget  
 CRenderTarget オブジェクトを構築します。  
  
```  
CRenderTarget();
```  
  
##  <a name="destroy"></a>CRenderTarget::Destroy  
 1 つまたは複数のリソースを削除します。  
  
```  
BOOL Destroy(BOOL bDeleteResources = TRUE);
```  
  
### <a name="parameters"></a>パラメーター  
 `bDeleteResources`  
 BDeleteResources が TRUE の場合は、m_lstResources にあるすべてのリソースを自動的に破棄されます。  
  
### <a name="return-value"></a>戻り値  
 メソッドが成功した場合、TRUE を返します。 それ以外の場合は FALSE を返します  
  
##  <a name="detach"></a>CRenderTarget::Detach  
 レンダー ターゲット インターフェイス オブジェクトからのデタッチします。  
  
```  
ID2D1RenderTarget* Detach ();
```  
  
### <a name="return-value"></a>戻り値  
 デタッチされたへのポインターは、対象のインターフェイスをレンダリングします。  
  
##  <a name="drawbitmap"></a>CRenderTarget::DrawBitmap  
 指定した IDWriteTextLayout オブジェクトによって記述されたフォーマットされたテキストを描画します。  
  
```  
void DrawBitmap(
    CD2DBitmap* pBitmap,  
    const CD2DRectF& rectDest,  
    float fOpacity = 1.0,  
    D2D1_BITMAP_INTERPOLATION_MODE interpolationMode = D2D1_BITMAP_INTERPOLATION_MODE_LINEAR,  
    const CD2DRectF* pRectSrc = NULL);
```  
  
### <a name="parameters"></a>パラメーター  
 `pBitmap`  
 レンダリングするビットマップ。  
  
 `rectDest`  
 サイズとデバイスに依存しないピクセルのビットマップが描画される領域のレンダー ターゲットの座標空間内の位置。 かどうかは、四角形はありませんがよく整理された、何も描画されると、レンダー ターゲットではエラー状態が入力されていません。  
  
 `fOpacity`  
 ビットマップに適用する不透明度の値を指定する 0.0 f ~ 1.0 f を含んでいるため、値この値は、ビットマップの内容のアルファ値に乗算します。  
  
 `interpolationMode`  
 ビットマップを拡大縮小または描画操作で回転する場合に使用する補間モードです。  
  
 `pRectSrc`  
 サイズと位置を描画するビットマップ内の領域のビットマップの座標空間内のデバイスに依存しないピクセルで。  
  
##  <a name="drawellipse"></a>CRenderTarget::DrawEllipse  
 指定した線のスタイルを使用して、指定された楕円のアウトラインを描画します。  
  
```  
void DrawEllipse(
    const CD2DEllipse& ellipse,  
    CD2DBrush* pBrush,  
    FLOAT fStrokeWidth = 1.0,  
    ID2D1StrokeStyle* strokeStyle = NULL);
```  
  
### <a name="parameters"></a>パラメーター  
 `ellipse`  
 位置とデバイスに依存しない (ピクセル単位) を描画する楕円の半径。  
  
 `pBrush`  
 楕円のアウトラインを描画するブラシ。  
  
 `fStrokeWidth`  
 楕円のストロークの太さ。 ストロークの中心は、楕円のアウトラインになります。  
  
 `strokeStyle`  
 楕円のアウトライン で、または線の描画に NULL を適用する線のスタイル。  
  
##  <a name="drawgeometry"></a>CRenderTarget::DrawGeometry  
 指定した線のスタイルを使用して指定された geometry の輪郭を描画します。  
  
```  
void DrawGeometry(
    CD2DGeometry* pGeometry,  
    CD2DBrush* pBrush,  
    FLOAT fStrokeWidth = 1.0,  
    ID2D1StrokeStyle* strokeStyle = NULL);
```  
  
### <a name="parameters"></a>パラメーター  
 `pGeometry`  
 描画するジオメトリ。  
  
 `pBrush`  
 ジオメトリのストロークを描画するブラシ。  
  
 `fStrokeWidth`  
 ジオメトリのストロークの太さ。 ストロークの中心は、ジオメトリのアウトラインになります。  
  
 `strokeStyle`  
 ジオメトリのアウトライン で、または線の描画に NULL を適用する線のスタイル。  
  
##  <a name="drawglyphrun"></a>CRenderTarget::DrawGlyphRun  
 指定したグリフを描画します。  
  
```  
void DrawGlyphRun(
    const CD2DPointF& ptBaseLineOrigin,  
    const DWRITE_GLYPH_RUN& glyphRun,  
    CD2DBrush* pForegroundBrush,  
    DWRITE_MEASURING_MODE measuringMode = DWRITE_MEASURING_MODE_NATURAL);
```  
  
### <a name="parameters"></a>パラメーター  
 `ptBaseLineOrigin`  
 グリフの基準のデバイスに依存しないピクセル単位での元です。  
  
 `glyphRun`  
 表示するグリフ。  
  
 `pForegroundBrush`  
 指定したグリフを描画するブラシ。  
  
 `measuringMode`  
 グリフのメトリックを使用してフォーマットされているときにテキストを測定する方法を示す値です。 既定値は、DWRITE_MEASURING_MODE_NATURAL です。  
  
##  <a name="drawline"></a>CRenderTarget::DrawLine  
 指定した線のスタイルを使用して指定した点を結ぶ直線を描画します。  
  
```  
void DrawLine(
    const CD2DPointF& ptFrom,  
    const CD2DPointF& ptTo,  
    CD2DBrush* pBrush,  
    FLOAT fStrokeWidth = 1.0,  
    ID2D1StrokeStyle* strokeStyle = NULL);
```  
  
### <a name="parameters"></a>パラメーター  
 `ptFrom`  
 デバイスに依存しないピクセルで、行の開始点。  
  
 `ptTo`  
 デバイスに依存しないピクセルで、行の終了点です。  
  
 `pBrush`  
 直線のストロークを描画するブラシ。  
  
 `fStrokeWidth`  
 ストロークの幅を指定する 0.0 f 以上の値です。 このパラメーターが指定されていない場合の既定値は 1.0f です。 ストロークは、線上の中央に配置します。  
  
 `strokeStyle`  
 ペイントまたは実線の描画に NULL に線のスタイル。  
  
##  <a name="drawrectangle"></a>CRenderTarget::DrawRectangle  
 指定した寸法と線のスタイルを持つ四角形のアウトラインを描画します。  
  
```  
void DrawRectangle(
    const CD2DRectF& rect,  
    CD2DBrush* pBrush,  
    FLOAT fStrokeWidth = 1.0,  
    ID2D1StrokeStyle* strokeStyle = NULL);
```  
  
### <a name="parameters"></a>パラメーター  
 `rect`  
 デバイスに依存しないピクセルで、描画する四角形の寸法  
  
 `pBrush`  
 四角形のストロークを描画するブラシ  
  
 `fStrokeWidth`  
 四角形のストロークの幅を指定する 0.0 f 以上の値です。 ストロークの中心は、四角形のアウトラインになります。  
  
 `strokeStyle`  
 ペイント、または線の描画に NULL に線のスタイル。  
  
##  <a name="drawroundedrectangle"></a>CRenderTarget::DrawRoundedRectangle  
 指定した線のスタイルを使用して、指定した角の丸い四角形のアウトラインを描画します。  
  
```  
void DrawRoundedRectangle(
    const CD2DRoundedRect& rectRounded,  
    CD2DBrush* pBrush,  
    FLOAT fStrokeWidth = 1.0,  
    ID2D1StrokeStyle* strokeStyle = NULL);
```  
  
### <a name="parameters"></a>パラメーター  
 `rectRounded`  
 デバイスに依存しないピクセルで、描画する角の丸い四角形の寸法。  
  
 `pBrush`  
 角の丸い四角形のアウトラインを描画するブラシ。  
  
 `fStrokeWidth`  
 角の丸い四角形のストロークの幅。 ストロークの中心は、角の丸い四角形のアウトラインになります。 既定値は、1.0 f です。  
  
 `strokeStyle`  
 角の丸い四角形のストローク、または線の描画に NULL のスタイル。 既定値は NULL です。  
  
##  <a name="drawtext"></a>CRenderTarget::DrawText  
 IDWriteTextFormat オブジェクトによって提供される形式の情報を使用して、指定したテキストを描画します。  
  
```  
void DrawText(
    const CString& strText,  
    const CD2DRectF& rect,  
    CD2DBrush* pForegroundBrush,  
    CD2DTextFormat* textFormat = NULL,  
    D2D1_DRAW_TEXT_OPTIONS options = D2D1_DRAW_TEXT_OPTIONS_NONE,  
    DWRITE_MEASURING_MODE measuringMode = DWRITE_MEASURING_MODE_NATURAL);
```  
  
### <a name="parameters"></a>パラメーター  
 `strText`  
 描画する Unicode 文字の配列へのポインター。  
  
 `rect`  
 サイズと、テキストが描画される領域の位置。  
  
 `pForegroundBrush`  
 テキストの描画に使用するブラシ。  
  
 `textFormat`  
 描画するテキストのフォント、フォント サイズ、フローの方向などの詳細を書式設定を説明するオブジェクト。  
  
 `options`  
 ピクセルの境界にテキストをスナップするかどうかと、レイアウト四角形にテキストをクリップするかどうかを示す値です。 既定値は、D2D1_DRAW_TEXT_OPTIONS_NONE で、テキストは、ピクセルの境界にスナップする必要があり、レイアウト四角形にクリップすることがないことを示します。  
  
 `measuringMode`  
 グリフのメトリックを使用してフォーマットされているときにテキストを測定する方法を示す値です。 既定値は、DWRITE_MEASURING_MODE_NATURAL です。  
  
##  <a name="drawtextlayout"></a>CRenderTarget::DrawTextLayout  
 指定した IDWriteTextLayout オブジェクトによって記述されたフォーマットされたテキストを描画します。  
  
```  
void DrawTextLayout(
    const CD2DPointF& ptOrigin,  
    CD2DTextLayout* textLayout,  
    CD2DBrush* pBrushForeground,  
    D2D1_DRAW_TEXT_OPTIONS options = D2D1_DRAW_TEXT_OPTIONS_NONE);
```  
  
### <a name="parameters"></a>パラメーター  
 `ptOrigin`  
 TextLayout で記述されるテキストの左上隅が描画されるデバイスに依存しないピクセル単位で説明されている点です。  
  
 `textLayout`  
 描画する書式設定されたテキスト。 ID2D1Resource から継承しないすべての描画効果が無視されます。 描画の効果 ID2D1Resource から継承するブラシではない場合は、このメソッドは失敗し、レンダー ターゲットがエラー状態にします。  
  
 `pBrushForeground`  
 (IDWriteTextLayout::SetDrawingEffect メソッドで指定)、描画効果とそれに関連付けられているブラシない textLayout に入力されたテキストを描画するブラシ。  
  
 `options`  
 ピクセルの境界にテキストをスナップするかどうかと、レイアウト四角形にテキストをクリップするかどうかを示す値です。 既定値は、D2D1_DRAW_TEXT_OPTIONS_NONE で、テキストは、ピクセルの境界にスナップする必要があり、レイアウト四角形にクリップすることがないことを示します。  
  
##  <a name="enddraw"></a>CRenderTarget::EndDraw  
 レンダー ターゲットに対して描画操作を終了し、現在のエラー状態と関連付けられているタグを示します。  
  
```  
HRESULT EndDraw();
```  
  
### <a name="return-value"></a>戻り値  
 メソッドが成功した場合は S_OK を返します。 それ以外の場合、HRESULT エラー コードを返します。  
  
##  <a name="fillellipse"></a>CRenderTarget::FillEllipse  
 指定された楕円の内部を描画します。  
  
```  
void FillEllipse(
    const CD2DEllipse& ellipse,  
    CD2DBrush* pBrush);
```  
  
### <a name="parameters"></a>パラメーター  
 `ellipse`  
 位置とデバイスに依存しない (ピクセル単位) を描画する楕円の半径。  
  
 `pBrush`  
 楕円の内部を描画するブラシ。  
  
##  <a name="fillgeometry"></a>CRenderTarget::FillGeometry  
 指定された geometry の内部を描画します。  
  
```  
void FillGeometry(
    CD2DGeometry* pGeometry,  
    CD2DBrush* pBrush,  
    CD2DBrush* pOpacityBrush = NULL);
```  
  
### <a name="parameters"></a>パラメーター  
 `pGeometry`  
 描画するジオメトリ。  
  
 `pBrush`  
 ジオメトリの描画に使用されるブラシの内部をします。  
  
 `pOpacityBrush`  
 不透明度マスクのジオメトリ; に適用するにはない不透明度マスクの場合は NULL です。 不透明度マスク (opacityBrush パラメーター) を指定すると、ブラシは D2D1_EXTEND_MODE_CLAMP に設定されている、x および y 拡張モードのある ID2D1BitmapBrush をする必要があります。 詳細については、「解説」を参照してください。  
  
##  <a name="fillmesh"></a>CRenderTarget::FillMesh  
 指定したメッシュの内部を描画します。  
  
```  
void FillMesh(
    CD2DMesh* pMesh,  
    CD2DBrush* pBrush);
```  
  
### <a name="parameters"></a>パラメーター  
 `pMesh`  
 描画にメッシュです。  
  
 `pBrush`  
 メッシュの描画に使用するブラシ。  
  
##  <a name="fillopacitymask"></a>CRenderTarget::FillOpacityMask  
 ブラシへの指定したビットマップが示す不透明度マスクを適用し、そのブラシを使用して、レンダー ターゲットの領域を描画します。  
  
```  
void FillOpacityMask(
    CD2DBitmap* pOpacityMask,  
    CD2DBrush* pBrush,  
    D2D1_OPACITY_MASK_CONTENT content,  
    const CD2DRectF& rectDest,  
    const CD2DRectF& rectSrc);
```  
  
### <a name="parameters"></a>パラメーター  
 `pOpacityMask`  
 位置とデバイスに依存しない (ピクセル単位) を描画する楕円の半径。  
  
 `pBrush`  
 DestinationRectangle で指定されたレンダー ターゲットの領域を描画するブラシ。  
  
 `content`  
 コンテンツの不透明度マスクの種類が含まれています。 値を使用してを不透明度マスクがブレンドされる色空間を判断します。  
  
 `rectDest`  
 デバイスに依存しないピクセル単位での描画にレンダー ターゲットの領域。  
  
 `rectSrc`  
 デバイスに依存しないピクセル単位での不透明度マスクとして使用するビットマップのリージョンです。  
  
##  <a name="fillrectangle"></a>CRenderTarget::FillRectangle  
 指定された四角形の内部を描画します。  
  
```  
void FillRectangle(
    const CD2DRectF& rect,  
    CD2DBrush* pBrush);
```  
  
### <a name="parameters"></a>パラメーター  
 `rect`  
 デバイスに依存しないピクセルで、描画する四角形のディメンションです。  
  
 `pBrush`  
 四角形を描画するブラシの内部をします。  
  
##  <a name="fillroundedrectangle"></a>CRenderTarget::FillRoundedRectangle  
 指定した角の丸い四角形の内部を描画します。  
  
```  
void FillRoundedRectangle(
    const CD2DRoundedRect& rectRounded,  
    CD2DBrush* pBrush);
```  
  
### <a name="parameters"></a>パラメーター  
 `rectRounded`  
 デバイスに依存しないピクセルで、描画する角の丸い四角形の寸法。  
  
 `pBrush`  
 角丸四角形の内部を描画するブラシ。  
  
##  <a name="flush"></a>CRenderTarget::Flush  
 すべての保留中の描画コマンドを実行します。  
  
```  
void Flush(
    D2D1_TAG* tag1 = NULL,  
    D2D1_TAG* tag2 = NULL);
```  
  
### <a name="parameters"></a>パラメーター  
 `tag1`  
 エラーがない場合は、エラーまたは 0 を原因となった操作を描画するためのタグが含まれています。 このパラメーターは初期化せずに渡されます。  
  
 `tag2`  
 エラーがない場合は、エラーまたは 0 を原因となった操作を描画するためのタグが含まれています。 このパラメーターは初期化せずに渡されます。  
  
##  <a name="getantialiasmode"></a>CRenderTarget::GetAntialiasMode  
 テキスト以外の描画操作の現在の (アンチエイリアシング) モードを取得します。  
  
```  
D2D1_ANTIALIAS_MODE GetAntialiasMode() const;  
```  
  
### <a name="return-value"></a>戻り値  
 テキスト以外の描画操作の現在の (アンチエイリアシング) モード。  
  
##  <a name="getdpi"></a>CRenderTarget::GetDpi  
 レンダリング ターゲットのドット/インチ (DPI) を返します  
  
```  
CD2DSizeF GetDpi() const;  
```  
  
### <a name="return-value"></a>戻り値  
 レンダー ターゲットのドット/インチ (DPI)。  
  
##  <a name="getmaximumbitmapsize"></a>CRenderTarget::GetMaximumBitmapSize  
 レンダー ターゲットでサポートされている任意の&1; つのビットマップ ディメンションのデバイスに依存しない単位 (ピクセル単位) で最大サイズを取得します。  
  
```  
UINT32 GetMaximumBitmapSize() const;  
```  
  
### <a name="return-value"></a>戻り値  
 レンダー ターゲットでサポートされている任意の&1; つのビットマップ ディメンションのピクセル単位の最大サイズ  
  
##  <a name="getpixelformat"></a>CRenderTarget::GetPixelFormat  
 レンダー ターゲットのピクセル形式とアルファ モードを取得します。  
  
```  
D2D1_PIXEL_FORMAT GetPixelFormat() const;  
```  
  
### <a name="return-value"></a>戻り値  
 レンダー ターゲットのピクセル形式とアルファ モード  
  
##  <a name="getpixelsize"></a>CRenderTarget::GetPixelSize  
 デバイス ピクセル単位で、レンダー ターゲットのサイズを返します  
  
```  
CD2DSizeU GetPixelSize() const;  
```  
  
### <a name="return-value"></a>戻り値  
 デバイス ピクセル単位で、レンダー ターゲットのサイズ  
  
##  <a name="getrendertarget"></a>CRenderTarget::GetRenderTarget  
 返します。 ID2D1RenderTarget インターフェイス  
  
```  
ID2D1RenderTarget* GetRenderTarget();
```  
  
### <a name="return-value"></a>戻り値  
 ID2D1RenderTarget インターフェイスまたはオブジェクトがまだ初期化されていない場合は NULL へのポインター。  
  
##  <a name="getsize"></a>CRenderTarget::GetSize  
 デバイスに依存しないピクセル単位で、レンダー ターゲットのサイズを返します  
  
```  
CD2DSizeF GetSize() const;  
```  
  
### <a name="return-value"></a>戻り値  
 デバイスに依存しないピクセルで、レンダー ターゲットの現在のサイズ  
  
##  <a name="gettags"></a>CRenderTarget::GetTags  
 以降の描画操作のラベルを取得します。  
  
```  
void GetTags(
    D2D1_TAG* tag1 = NULL,  
    D2D1_TAG* tag2 = NULL) const;  
```  
  
### <a name="parameters"></a>パラメーター  
 `tag1`  
 以降の描画操作の最初のラベルが含まれています。 このパラメーターは初期化せずに渡されます。 NULL が指定されている場合、このパラメーターの値は取得されません。  
  
 `tag2`  
 以降の描画操作の&2; 番目のラベルが含まれています。 このパラメーターは初期化せずに渡されます。 NULL が指定されている場合、このパラメーターの値は取得されません。  
  
##  <a name="gettextantialiasmode"></a>CRenderTarget::GetTextAntialiasMode  
 テキストとグリフが描画操作の現在の (アンチエイリアシング) モードを取得します。  
  
```  
D2D1_TEXT_ANTIALIAS_MODE GetTextAntialiasMode() const;  
```  
  
### <a name="return-value"></a>戻り値  
 テキストとグリフが描画操作の現在の (アンチエイリアシング) モード。  
  
##  <a name="gettextrenderingparams"></a>CRenderTarget::GetTextRenderingParams  
 レンダー ターゲットの現在のテキストのレンダリング オプションを取得します。  
  
```  
void GetTextRenderingParams(IDWriteRenderingParams** textRenderingParams);
```  
  
### <a name="parameters"></a>パラメーター  
 `textRenderingParams`  
 TextRenderingParamscontains レンダー ターゲットへのポインターのアドレスの現在このメソッドが戻るときにテキストのレンダリング オプション。  
  
##  <a name="gettransform"></a>CRenderTarget::GetTransform  
 既存の変換を置き換える、レンダー ターゲットを指定した変換を適用します。 後続のすべての描画操作は、変換された空間で発生します。  
  
```  
void GetTransform(D2D1_MATRIX_3X2_F* transform);
```  
  
### <a name="parameters"></a>パラメーター  
 `transform`  
 レンダー ターゲットに適用する変換です。  
  
##  <a name="issupported"></a>CRenderTarget::IsSupported  
 レンダー ターゲットが指定されたプロパティをサポートするかどうかを示します  
  
```  
BOOL IsSupported(const D2D1_RENDER_TARGET_PROPERTIES& renderTargetProperties) const;  
```  
  
### <a name="parameters"></a>パラメーター  
 `renderTargetProperties`  
 レンダー ターゲットのプロパティをテストするには  
  
### <a name="return-value"></a>戻り値  
 このレンダー ターゲットである、指定されたレンダー ターゲットのプロパティがサポートされている場合は TRUE。それ以外の場合は FALSE  
  
##  <a name="isvalid"></a>CRenderTarget::IsValid  
 リソースの有効性のチェック  
  
```  
BOOL IsValid() const;  
```  
  
### <a name="return-value"></a>戻り値  
 リソースが無効である場合は TRUE。それ以外の場合は FALSE。  
  
##  <a name="m_lstresources"></a>CRenderTarget::m_lstResources  
 CD2DResource のオブジェクトへのポインターのリスト。  
  
```  
CObList m_lstResources;  
```  
  
##  <a name="m_prendertarget"></a>CRenderTarget::m_pRenderTarget  
 ID2D1RenderTarget オブジェクトへのポインター。  
  
```  
ID2D1RenderTarget* m_pRenderTarget;  
```  
  
##  <a name="m_ptextformatdefault"></a>CRenderTarget::m_pTextFormatDefault  
 既定のテキスト形式を格納している CD2DTextFormat のオブジェクトへのポインター。  
  
```  
CD2DTextFormat* m_pTextFormatDefault;  
```  
  
##  <a name="operator_id2d1rendertarget_star"></a>CRenderTarget::operator ID2D1RenderTarget *  
 返します。 ID2D1RenderTarget インターフェイス  
  
```  
operator ID2D1RenderTarget*();
```   
  
### <a name="return-value"></a>戻り値  
 ID2D1RenderTarget インターフェイスまたはオブジェクトがまだ初期化されていない場合は NULL へのポインター。  
  
##  <a name="popaxisalignedclip"></a>CRenderTarget::PopAxisAlignedClip  
 レンダー ターゲットから最後の軸に沿ったクリップを削除します。 このメソッドが呼び出された後、クリップが以降の描画操作に適用されていません。  
  
```  
void PopAxisAlignedClip();
```  
  
##  <a name="poplayer"></a>CRenderTarget::PopLayer  
 最後の PushLayer で指定されているレイヤーの描画操作のリダイレクトを停止を呼び出します。  
  
```  
void PopLayer();
```  
  
##  <a name="pushaxisalignedclip"></a>CRenderTarget::PushAxisAlignedClip  
 レンダー ターゲットから最後の軸に沿ったクリップを削除します。 このメソッドが呼び出された後、クリップが以降の描画操作に適用されていません。  
  
```  
void PushAxisAlignedClip(
    const CD2DRectF& rectClip,  
    D2D1_ANTIALIAS_MODE mode = D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);
```  
  
### <a name="parameters"></a>パラメーター  
 `rectClip`  
 サイズとクリッピング領域のデバイスに依存しないピクセル位置。  
  
 `mode`  
 使用してサブピクセル境界があるクリップ四角形のエッジを描画し、シーンの内容でクリップを調和させるアンチ エイリアス処理モードです。 ブレンドに対して実行されるときに PopAxisAlignedClip メソッドが呼び出され、そのレイヤー内の各プリミティブには適用されません。  
  
##  <a name="pushlayer"></a>CRenderTarget::PushLayer  
 PopLayer が呼び出されるまでは、後続のすべての描画操作を受信できるように、レンダー ターゲットに指定したレイヤーを追加します。  
  
```  
void PushLayer(
    const D2D1_LAYER_PARAMETERS& layerParameters,  
    CD2DLayer& layer);
```  
  
### <a name="parameters"></a>パラメーター  
 `layerParameters`  
 コンテンツの境界、幾何学模様マスク、不透明度、不透明度マスク、および、レイヤーのアンチ エイリアス処理オプション。  
  
 `layer`  
 以降の描画操作を受信するレイヤー。  
  
##  <a name="restoredrawingstate"></a>CRenderTarget::RestoreDrawingState  
 指定した ID2D1DrawingStateBlock のレンダー ターゲットの描画状態を設定します。  
  
```  
void RestoreDrawingState(ID2D1DrawingStateBlock& drawingStateBlock);
```  
  
### <a name="parameters"></a>パラメーター  
 `drawingStateBlock`  
 レンダー ターゲットの新しい状態を描画します。  
  
##  <a name="savedrawingstate"></a>CRenderTarget::SaveDrawingState  
 指定した ID2D1DrawingStateBlock に現在の描画状態を保存します。  
  
```  
void SaveDrawingState(ID2D1DrawingStateBlock& drawingStateBlock) const;  
```  
  
### <a name="parameters"></a>パラメーター  
 `drawingStateBlock`  
 このメソッドが戻るとき、レンダー ターゲットの現在の描画状態を格納します。 このパラメーターは、メソッドに渡す前に初期化する必要があります。  
  
##  <a name="setantialiasmode"></a>CRenderTarget::SetAntialiasMode  
 レンダー ターゲットの (アンチエイリアシング) モードを設定します。 アンチ エイリアス処理モードは、テキストおよびグリフが描画操作を除く、すべての後続描画操作に適用されます。  
  
```  
void SetAntialiasMode(D2D1_ANTIALIAS_MODE antialiasMode);
```  
  
### <a name="parameters"></a>パラメーター  
 `antialiasMode`  
 将来の描画操作 (アンチエイリアシング) モード。  
  
##  <a name="setdpi"></a>CRenderTarget::SetDpi  
 ドット/インチ (DPI) のレンダー ターゲットを設定します。  
  
```  
void SetDpi(const CD2DSizeF& sizeDPI);
```  
  
### <a name="parameters"></a>パラメーター  
 `sizeDPI`  
 レンダー ターゲットの水平方向/verticalDPI を指定する&0; 以上の値です。  
  
##  <a name="settags"></a>CRenderTarget::SetTags  
 以降の描画操作のラベルを指定します。  
  
```  
void SetTags(
    D2D1_TAG tag1,  
    D2D1_TAG tag2);
```  
  
### <a name="parameters"></a>パラメーター  
 `tag1`  
 以降の描画操作に適用するラベルです。  
  
 `tag2`  
 以降の描画操作に適用するラベルです。  
  
##  <a name="settextantialiasmode"></a>CRenderTarget::SetTextAntialiasMode  
 後続のテキストおよびグリフの描画操作を使用する (アンチエイリアシング) モードを指定します。  
  
```  
void SetTextAntialiasMode(D2D1_TEXT_ANTIALIAS_MODE textAntialiasMode);
```  
  
### <a name="parameters"></a>パラメーター  
 `textAntialiasMode`  
 後続のテキストおよびグリフが描画操作を使用する (アンチエイリアシング) モード。  
  
##  <a name="settextrenderingparams"></a>CRenderTarget::SetTextRenderingParams  
 すべての後続のテキストとグリフが描画操作に適用するテキストのレンダリング オプションを指定します。  
  
```  
void SetTextRenderingParams(IDWriteRenderingParams* textRenderingParams = NULL);
```  
  
### <a name="parameters"></a>パラメーター  
 `textRenderingParams`  
 すべての後続のテキストとグリフが描画操作に適用するテキストのレンダリング オプション現在のテキストのレンダリング オプションをオフにする場合は NULL です。  
  
##  <a name="settransform"></a>CRenderTarget::SetTransform  
 既存の変換を置き換える、レンダー ターゲットを指定した変換を適用します。 後続のすべての描画操作は、変換された空間で発生します。  
  
```  
void SetTransform(const D2D1_MATRIX_3X2_F* transform);  
void SetTransform(const D2D1_MATRIX_3X2_F& transform);
```  
  
### <a name="parameters"></a>パラメーター  
 `transform`  
 レンダー ターゲットに適用する変換です。  
  
##  <a name="verifyresource"></a>CRenderTarget::VerifyResource  
 CD2DResource オブジェクトの有効性; を検証します。存在しない場合は、オブジェクトを作成します。  
  
```  
BOOL VerifyResource(CD2DResource* pResource);
```  
  
### <a name="parameters"></a>パラメーター  
 `pResource`  
 CD2DResource オブジェクトへのポインター。  
  
### <a name="return-value"></a>戻り値  
 有効である場合は、オブジェクトの場合は TRUEそれ以外の場合は FALSE。  
  
## <a name="see-also"></a>関連項目  
 [クラス](../../mfc/reference/mfc-classes.md)
