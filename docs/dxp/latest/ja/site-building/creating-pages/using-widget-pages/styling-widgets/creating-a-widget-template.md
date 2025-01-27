# ウィジェットテンプレートの作成

ウィジェットテンプレートは、ウィジェットの外観をカスタマイズするために使用されます。 ウィジェットの表示用テンプレートを作成し、どのテンプレートをアクティブにするかを選択することができます。 ウィジェットテンプレートを作成するには、以下の手順で行います。

1.  サイト管理から、 **Site Selector** ボタン (![Compass](../../../../images/icon-compass.png))をクリックして、ウィジェットテンプレートを作成するサイトを選択します。

    ![コンパスのアイコンをクリックして、ウィジェットテンプレートを作成するサイトを選択します。](./creating-a-widget-template/images/01.png)

1. ［**Design**］ &rarr; ［**Widget Templates**］ を開きます。

    ![デザインとウィジェットのテンプレートをクリックします。](./creating-a-widget-template/images/02.png)

グローバルコンテキストを選択した場合、このページには、アプリで利用可能なサンプルテンプレートのリストが表示されます。 これらのサンプルテンプレートは、すでにアプリに設定されているデフォルトのテンプレートとは異なります。 テンプレートをホストするサイトを選択した場合、そのサイトのアプリ用にカスタムテンプレートを作成する必要があります。

![デザインとウィジェットのテンプレートをクリックします。](./creating-a-widget-template/images/03.png)

1. **追加** ボタン (![Add Button](../../../../images/icon-add.png)) をクリックすると、作成するテンプレートの種類を選択するように求められます。

1.  ウィジェットの名前を入力します。

    **Optional** により ［**Details**］ を開いて、説明と使用する小さな画像を指定します。 テンプレートの言語の種類を選択することができます。

1. ［**詳細**］ 内で、使用するスクリプト言語を選択します。 FreeMarkerまたはVelocityを使用することができます。 FreeMarkerをお勧めします。

1. **スクリプト** セクションを使用して、ウィジェットテンプレートを作成します。

1. ［**保存**］ をクリックします。

<a name="the-template-editor" />

## テンプレートエディター

テンプレートエディターの左側には、テンプレートの作成によく使われる変数がパレットで表示されています。 テンプレートを作成する際の参考にしてください。 テンプレートエディターに変数を配置するには、配置したい場所にテキストカーソルを置き、変数名をクリックします。

また、各変数には、詳細な説明を表示するツールチップがあります。 ウィジェットテンプレートには複数の種類があるため、ウィジェットテンプレートごとに異なる変数も存在します。 したがって、各テンプレートには、その特定のテンプレートにのみ適用可能な異なる変数のセットがあります。

![Liferayは、ウィジェットテンプレートをカスタマイズするための多機能なスクリプトエディターを提供します。](./creating-a-widget-template/images/04.png)

また、オートコンプリート機能を使って、テンプレートに変数を追加することもできます。 **${** と入力すると、利用可能な変数のドロップダウンメニューが表示され、呼び出すことができます。 変数の一つをクリックすると、エディターにその変数が挿入されます。

また、同じ種類のテンプレートを他のテンプレートに埋め込むことも可能です。 例えば、既存のWikiウィジェットテンプレートがあり、同様のWikiウィジェットテンプレートをもう1つ作成したいとします。 ゼロから始めるのではなく、既存のWikiウィジェットテンプレートを新しいものにインポートして、それを元に構築することができます。 つまり、システム内のVelocityやFreeMarkerのテンプレートから再利用可能なコードを取り込むことができる汎用テンプレートとして、ウィジェットテンプレートを活用することができます。

<a name="configuring-widget-templates" />

## ウィジェットテンプレートの設定

ウィジェットテンプレートを保存した後は、 **アクション** ボタン (![Actions Button](../../../../images/icon-actions.png)) から管理することが可能です。 これにはいくつかのオプションがあります。

- **編集** : ウィジェットテンプレートの設定プロパティを変更することができます。
- **権限設定** : ウィジェットテンプレートの **アップデート** 、 **権限設定** 、 **削除** 、そして **表示** を管理することができます。
- **コピー** : ウィジェットテンプレートのコピーを作成します。
- **削除** : ウィジェットテンプレートを削除します。

さらに、ウィジェットテンプレートは、静的URLとWebDAV URLを生成します。 これらの値は、テンプレートのXMLソースにアクセスします。 これらのURLは、メニューからウィジェットテンプレートをクリックし、 **Details** セクションを展開することで見つけることができます。 WebDAV URLにより、サイト管理者はリモートサーバー上のウィジェットテンプレートを追加、参照、編集、削除することができます。 WebDAVのURLで何ができるかを詳しく知りたい方は、 [WebDAVを使用したドキュメントへのアクセス](../../../../content-authoring-and-management/documents-and-media/publishing-and-sharing/accessing-documents-with-webdav.md)の記事をご覧ください。

```{note}
ウィジェットテンプレートにウィジェットを埋め込むことは可能ですが、他のウィジェットとの競合や予期せぬ動作（例：パンくずリストへのデータ集計ウィジェットの埋め込み）を引き起こす可能性があるため、推奨されません。 ウィジェットテンプレートにウィジェットを埋め込むしかない場合、他のウィジェットと干渉しないことを確認してください。
```

次に、新しいウィジェットテンプレートを使用するようにウィジェットを設定します。

1.  修正したいウィジェットの ［**Configuration**］ ページを開き、 ［**表示設定**］ を開いてください。

1. ［**表示テンプレート**］ で、ドロップダウンメニューからウィジェットテンプレートを選択します。

また、アプリのサイト固有の表示テンプレートも管理できます。これを行うには、 **表示テンプレート** の横の **Manage Display Templates for [SPECIFIC_SITE**] をクリックしてください。 設定されたテンプレートのリストが表示され、新しいテンプレートを追加したり、既存のテンプレートを編集したりすることができます。

![アプリの **設定** メニューをクリックすると、利用可能なウィジェットテンプレートを編集・管理することができます。](./creating-a-widget-template/images/05.png)

<a name="additional-information" />

## 追加情報

- [ウィジェットテンプレートの例](./using-a-widget-template-example.md)