# ユーザーセグメントの作成と管理

**セグメント** を使用すると、ユーザーの **役職** やユーザーの **言語** など、共通のプロパティセットに基づいて、さまざまなユーザーグループを作成できます。 セグメントの定義に使用できるプロパティのリストについては、 [セグメントエディターUIリファレンス](./segments-editor-ui-reference.md) を参照してください。 既存のプロパティに加えて、ユーザーグループと組織グループの[カスタムフィールド](../../../system-administration/configuring-liferay/adding-custom-fields.md)を追加し、セグメント基準でこれらのフィールドを使用できます。

<a name="compound-segments" />

## 複合セグメント

> 対応可能：Liferay DXP/Portal 7.3以降

既存のセグメントを組み合わせて、新しい **複合セグメント** を作成できます。 複合セグメントは、ベースとなるセグメントからプロパティを継承し、メンバーを自動的に更新します。 プロパティを追加して、複合セグメントをさらにカスタマイズできます。

複合セグメントがどのように機能するかを理解するために、次の例を考えてみましょう。 米国からの訪問者とカナダからの訪問者のニーズは異なるため、プロパティが異なる2つのセグメントを作成し、国ごとに1つのセグメントを作成します。 その後、北米からの訪問者用に新しい標準セグメントを作成し、米国とカナダのセグメントのプロパティを手動でコピーします。 米国またはカナダのセグメントのプロパティを変更すると、北米のセグメントはその変更を継承しません。 これらの変更を反映するには、北米のセグメントを手動で更新する必要があります。 ただし、北米セグメントを複合セグメントとして作成した場合、米国またはカナダのセグメントを変更すると、この複合セグメントはその定義とメンバーを自動的に更新します。

```{important}
既存の複合セグメントを使用して新しいセグメントを作成することはできません。
```

![2つ以上のセグメントを組み合わせて、新しい複合セグメントを作成します](./creating-and-managing-user-segments/images/08.png)

<a name="creating-user-segments" />

## ユーザーセグメントの作成

次の手順では、新しいセグメントを作成する方法について説明します。

1. 画面左側のサイトメニューから、 ［**People**］ &rarr; ［**セグメント**］ に移動します。

    ![［People］メニューからユーザーセグメントを追加します。](./creating-and-managing-user-segments/images/01.png)

1. **追加** ボタン（![Add](../../../images/icon-add.png)）をクリックします。

1. 上部のテキスト領域をクリックして、ユーザーセグメントの名前を入力します。

   ```{tip}
   セグメント名の横にあるフラグセレクターを使用して、セグメントの名前を変換できます。
   ```

1. ［**Properties**］ 領域から、グループとプロパティを選択してセグメントを定義します。 **プロパティ** を ［**Conditions**］ 領域にドラッグアンドドロップします。

1. セグメントの条件を設定します（以下の [セグメントの条件の設定](#configuring-segment-conditions) を参照）。

1. ［**保存**］ をクリックします。

<a name="configuring-segment-conditions" />

### セグメント条件の設定

［**条件**］ 領域には、次のオプションがあります。

- 比較ドロップダウンメニュー（A）を使用して、比較基準を編集します。
- 条件の名前（B）の横にあるボタンを使用して、同じ **プロパティ** グループから **条件** を追加または削除します。
- **プロパティ**（C）をドラッグアンドドロップして、別の **プロパティ** グループを使用して条件を追加します。
- **条件を** AND **および** OR*演算子（DおよびE）と組み合わせます。</p>

   ![条件を追加および組み合わせて、セグメント基準を定義します。](./creating-and-managing-user-segments/images/06.png)</li> </ul>

[セッションプロパティ](./segments-editor-ui-reference.md#session-properties) の場合、[セッションプロパティのボキャブラリ](../../../content-authoring-and-management/tags-and-categories/session-property-vocabularies.md)を使用して事前定義された値のリストを構成できます。 このオプションにより、セグメントを定義するタスクが容易になり、手動入力のエラーがなくなります。

編集すると、基準を満たすメンバーの数が［Conditions］領域の上部に表示されます。 ［**View Members**］ をクリックしてリストを表示できます。 これは、セグメントを正しく定義しているかどうかを判断するのに役立ちます。

![セグメントメンバーのリストはいつでも表示できます。](./creating-and-managing-user-segments/images/04.png)

ユーザーセグメントを作成すると、 ［**Segments**］ ページのユーザーセグメントのリストに表示されます。 ここから、アクションメニュー（![Actions](../../../images/icon-actions.png)）を使用して、ユーザーセグメントの管理（編集、削除、 [サイトロールの割り当て](../../../users-and-permissions/roles-and-permissions/assigning-roles-to-user-segments.md)、ユーザーセグメントへのアクセス権を持つユーザーの権限変更）を行うことができます。 ユーザーセグメントの名前をクリックして編集することもできます。

![アクションメニューから権限を編集、削除、または管理できます。](./creating-and-managing-user-segments/images/05.png)

```{note}
エクスペリエンスで使用されているユーザーセグメントは削除できません。
```

<a name="related-information" />

## 関連情報

- [ユーザーセグメントへのロールの割り当て](../../../users-and-permissions/roles-and-permissions/assigning-roles-to-user-segments.md)
- [ユーザーセグメントの分析を取得する](./getting-analytics-for-user-segments.md)
- [コンテンツページのパーソナライゼーション](../experience-personalization/content-page-personalization.md)
- [セッションプロパティのボキャブラリ](../../../content-authoring-and-management/tags-and-categories/session-property-vocabularies.md)
