# コンテンツページでのウィジェットの使用

ウィジェットセクションは、ウィジェットページ</a>の
**Add** メニューと同じように機能します。 使用可能なウィジェットの完全なリストが表示され、それらをページに追加できます。 主な違いは、コンテンツページではウィジェットの主な構成オプションしか使用できないことです。</p> 



## コンテンツページにウィジェットを追加する

次の手順に従って、ウィジェットをコンテンツページに追加します。

1.  [がコンテンツページ](./building-content-pages.md)構築している間に [ウィジェットパネル](./content-pages-overview.md#widgets) を開き、必要なウィジェットが見つかるまで利用可能なウィジェットのカテゴリを参照するか、ウィジェットを名前で検索できます。
2.  ウィジェットを配置したいレイアウトの列と行にドラッグします。

ウィジェットは、WikiディスプレイまたはAsset Publisherのような動的パブリッシングツールです。 ウィジェットを使用して表示するコンテンツは、長文のテキストや画像ギャラリーなど、その中間のものにすることができます。



## コンテンツページでのウィジェットの構成

次の手順に従って、コンテンツページでウィジェットを構成します。

1.  ウィジェットにカーソルを合わせます。

2.  [オプション]メニュー（![Options Menu](../../../images/icon-app-options.png)）を開き、[**構成**]を選択します。 ここからは、ウィジェットに応じていくつかのオプションがあります。
   
   ![コンテンツメニューのウィジェットは、オプションメニューから設定できます。](./using-widgets-on-content-pages/images/01.png)

3. [**保存**] をクリックして変更を適用します。

<!-- end list -->

```{note}
Since Liferay Portal CE 7.3 GA2, you also configure permissions for the widget by selecting *Permissions* from the widget's Options Menu.
```




## コンテンツページでのウィジェット権限の構成

LiferayポータルCE 7.3 GA2以降、コンテンツページからウィジェットの権限を構成できます。 次の手順に従って、コンテンツページでウィジェットの権限を構成します。

1.  ウィジェットにカーソルを合わせます。
2.  [オプション]メニュー（![Options Menu](../../../images/icon-app-options.png)）を開き、[**権限]を選択します** 。
3.  表示される新しいウィンドウで、役割の権限をオンまたはオフにします。
4. [**保存**] をクリックして変更を適用します。

![コンテンツメニューのウィジェットの権限は、オプションメニューから設定できます。](./using-widgets-on-content-pages/images/02.png)



```{note}
When you create a page based on a [page template](../adding-pages/creating-a-page-template.md), the permissions are copied too. Permissions for a Master Page are set in the [Master Page](../defining-headers-and-footers/managing-master-pages.md), not in the pages.
```




## ウィジェットのコンテンツページの制限

コンテンツページのウィジェットの基本的な設定オプションと権限には引き続きアクセスできますが、ウィジェットページのウィジェットでのみ使用できるオプションがいくつかあります。

  - **ネストされたアプリケーション** ：ネストされたアプリケーション（ウィジェット内のウィジェット）は、ウィジェットページでのみサポートされます。
  - **ウィジェットルック & フィール** ：ウィジェットページでは、ウィジェットの設定メニューからルックアンドフィールメニューにアクセスでき、CSSをきめ細かく制御できます。 コンテンツのルックアンドフィールはテーマで、またはフラグメントを使用して定義されているため、コンテンツページのウィジェットでは使用できません。
  - **構成テンプレート** ：ウィジェットの構成設定をテンプレートに保存する構成テンプレートは、ウィジェットページでのみ使用できます。
  - **エクスポート/インポート** ：ウィジェットページのウィジェットのアプリケーションデータのみをエクスポート/インポートできます。
