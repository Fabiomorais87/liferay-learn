# ユーザーデータの無害化

一般的なデータ保護規制（GDPR）の技術的に厳しい要件の1つが、 **忘れられる権利** です。 ここでは、この要件の詳細に関する説明ではなく、その要件を満たすのに役立つ2つの機能（個人データ抹消とデータ匿名化）について説明します。

ソフトウェアによって **忘れられる** ということは、個人データが消去または匿名化されたユーザーの身元を知ることにつながる情報を、管理者でさえも得ることができなくなるということです。

概念的には、ユーザーを忘れるということは、少なくとも次の2つのことを意味します。

* システムからユーザーの識別情報を消去します。 Liferay DXPでは、データベーステーブルと検索インデックスからユーザーを削除することになります。
* ユーザーが操作したコンテンツを消去または匿名化して、実際の人物に追跡されないようにします。

``` tip::
   `ユーザーの非アクティブ化と削除は十分ではありませんか？`

   削除すると、データベース内のユーザーのテーブルからユーザーが削除されます。 しかし、ユーザーの情報は別の場所に保存されています。 標準的なユーザー削除シナリオでは、ユーザーが個人的に作成したすべてのコンテンツは、システムの識別子（ユーザーIDとユーザー名）によってユーザーに割り当てられたままであり、コンテンツの隣にあるUIに表示されます。 このようにユーザーを特定できるデータが意図せずに保存されてしまうことは、GDPRのいくつかの要件を満たすためには不十分であり、データ消去機能が追加された主な理由でもあります。
```

<a name="the-personal-data-erasure-screen" />

## 個人データ抹消画面

ユーザーデータの削除と匿名化は、どちらも［個人データ抹消］画面で行います。

1. アプリケーションメニュー（![Applications Menu](../../images/icon-applications-menu.png)）を開き、［コントロールパネル］ &rarr; ［ユーザー］ &rarr; ［ユーザーと組織］を開きます。

1. ユーザーのアクションボタン（![Actions](../../images/icon-actions.png)）をクリックし、 ［**個人データの削除**］ を選択します。 ユーザーを無効化していない場合は、無効化するように求められます。

   ユーザーの個人データ抹消画面が表示されます。

ユーザーがシステムに投稿したすべてのデータを閲覧できます。 ［**個人サイト**］ をクリックして、そのサイトのデータを閲覧します。

![ここから、ユーザーが自分の個人サイトに投稿したすべてのデータを閲覧できます。](./sanitizing-user-data/images/01.png)

通常のLiferayサイトに投稿されたデータを閲覧するには、 ［**標準サイト**］ をクリックします。

![管理者が作成したサイトにユーザーが投稿したすべてのデータを閲覧するには、［標準サイト］を選択します。](./sanitizing-user-data/images/02.png)

ユーザーのデータを確認するには、そのデータをクリックします。 たとえば、Pepperさんが自分の個人サイトにブログエントリーを投稿したようです。 そのエントリをクリックすると、そのブログエントリーのタイトルが表示されます。

![Pepperさんのブログエントリーはレビューが必要かもしれません。](./sanitizing-user-data/images/03.png)

エントリをレビューするには、それをクリックします。 アプリケーションの編集モード（この場合はブログ）が表示され、必要なコンテンツに変更を加えることができます。

アプリケーションのすべてのアイテムを一度に管理（匿名化または削除）するには、

1. アプリケーションのアクションボタン（![Actions](../../images/icon-actions.png)）をクリックします。

1. アプリケーションのすべてのアイテムを確実に安全に削除できる場合は、 ［**Delete**］ を選択します。

1. アプリケーションのすべてのアイテムを単に匿名化するだけで十分な場合は、 ［**匿名化**］ を選択します。

インターフェイスを使用して、サイト、アプリケーション、およびデータを閲覧します。

<a name="delete-the-user" />

## ユーザーの削除

すべてのデータが必要に応じて確認、削除、編集、または匿名化されたら、ユーザーを削除します。 ［個人データ抹消］画面が終了すると、ダイアログボックスが自動的にポップアップします。 この手順は簡単です。 ［**OK**］ をクリックするだけです。

![データ消去プロセスを終了するには、ユーザーを削除します。](./sanitizing-user-data/images/04.png)

これで、ユーザーのデータが匿名化または削除され、ユーザーも削除されます。

<a name="manual-anonymization" />

## 手動による匿名化

多くの場合、ユーザーのIDフィールドだけを匿名化し、ユーザーを削除するだけでは不十分です。 例えば、John Smithというユーザーが個人を特定できる情報をフォームに入力した場合、そのテキスト入力フィールドはUADフレームワークによって匿名化されません。

![ユーザーは、識別可能な情報を入力テキストフィールドに入力します。](./sanitizing-user-data/images/05.png)

匿名化後、 **Author** フィールドはサニタイズされていますが、ユーザーの入力テキストは残っているため、手動で削除する必要があります。

![ユーザーの入力テキストは匿名化されていません。](./sanitizing-user-data/images/06.png)

このようなユーザー生成コンテンツは、手動で識別し、個人を特定する情報を削除するために編集する必要があります。