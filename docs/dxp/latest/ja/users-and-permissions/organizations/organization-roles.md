# 組織ロール

Liferay [組織](./understanding-organizations.md) は、分散したユーザー管理を実装する便利な方法を提供します。 これらのロールを使用して、組織のすべてのメンバーに標準的な権限を割り当てたり、ユーザーの特定の責任に基づいてより専門的な権限を割り当てたりすることができます。 そうすることで、時間の節約にもなりますし、ポータルデザインが実際の階層に対応しているかどうかを確認することもできます。

<a name="understanding-organization-roles" />

## 組織ロールを理解する

組織ロールパーミッションは、グローバルレベルで定義され、割り当てられた特定の組織に適用されます。 [組織サイト](./organization-sites.md)での対応する暗黙的の権利もユーザーに付与します。 ただし、一部の組織ロールは、子組織およびそのサイトに対する権限を付与します。 必要に応じて、サイトロールを使用し、 [サイトチーム](../../site-building/building-sites/site-membership/creating-teams-for-sites.md) を作成して、組織サイト内のユーザーに追加のロールを明示的に割り当てることができます。 詳細については、 [ロールと権限について](../roles-and-permissions/understanding-roles-and-permissions.md) を参照してください。

```{note}
   デフォルトでは、組織ロールはコントロールパネルへのアクセスを許可しません。 ただし、組織の管理者やオーナーは、ドロップダウンの［個人用メニュー］から［私の組織］をクリックすることで、自分が管理する組織にアクセスできます。
```

Liferay DXPでは、以下のデフォルトの組織ロールが用意されています。

### 組織 ユーザー

このロールは、組織内での基本的な権限を与えるもので、すべてのメンバーに自動的に割り当てられます。 組織にサイトが併設されている場合、このロールはユーザーにサイトの基本メンバーシップを付与します。

```{note}
   子組織のメンバーは、親組織のメンバーとなります。 これは、例えば、子組織のメンバーが親組織のプライベートページにアクセスできることを意味します。 この動作は、portal-ext.properties <https://learn.liferay.com/reference/latest/en/dxp/propertiesdoc/portal.properties.html#Organizations>`_ファイルの``組織``セクションでカスタマイズすることができ、組織に特有のプロパティが記載されています。
```

### 組織管理者

このロールは、組織とそのサイト、および子組織とそのサイト内でのスーパーユーザー権限を付与します。 これには、子組織の作成と削除、既存の組織メンバーの子組織への割り当て、組織サイトの作成と削除、組織所属の新しいポータルユーザーの作成などの機能が含まれます。 組織サイトでは、［サイト］メニューのほか、グローバルメニューの［アプリケーション］タブにある［コンテンツ］、［アカウント］、［検索調整］、［コミュニケーション］、［App Builder］、［カスタムアプリ］へのアクセスが許可されます。 ただし、このロールでは組織管理者や組織オーナーを割り当てたり、削除したりすることはできません。

### 組織所有者

このロールは、組織管理者ロールで付与されたすべての権限と、組織管理者および組織所有者を割り当てたり削除したりする機能を与えます。 ただし、組織オーナーの権限は、その権限が与えられた組織と、その子組織や付属サイトにも適用されます。

<a name="assigning-organization-roles" />

## 組織ロールの割り当て

以下の手順で、既存の組織ユーザーに組織ロールを割り当てます。

1. **グローバルメニュー** を開き、 ［**コントロールパネル**］ &rarr; ［**ユーザー**］ &rarr; ［**ユーザーと組織**］ に行きます。 そして、 **組織** タブをクリックします。

1. 既存の組織の ［**アクション**］ ボタン（![Actions Button](../../images/icon-actions.png)）をクリックし、 ［**組織ロールの割当て**］ を選択します。

    ![［組織ロールの割当て］を選択します。](./organization-roles/images/01.png)

1. ユーザーに割り当てたい **組織ロール** をクリックします。

    ![ユーザーに割り当てたい組織ロールをクリックします。](./organization-roles/images/02.png)

1. **チェックボックス** を使って、どのユーザーにロールを割り当てるかを選択します。

    ![チェックボックスを使って、どのユーザーにそのロールを割り当てるかを選択します。](./organization-roles/images/03.png)

1. 終了したら ［**関連性の更新**］ をクリックします。

<a name="additional-information" />

## 追加情報

* [組織について](./understanding-organizations.md)
* [組織の作成と管理](./creating-and-managing-organizations.md)
* [組織へのユーザーの追加](./adding-users-to-organizations.md)
* [組織サイト](./organization-sites.md)
