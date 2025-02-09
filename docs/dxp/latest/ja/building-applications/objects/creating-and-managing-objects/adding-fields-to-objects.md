# オブジェクトへのフィールドの追加

フィールドは、データベースの列を表すデータ定義です。 Liferay Objectのさまざまな [タイプの値](#field-type-reference) を格納します。 システムオブジェクトとカスタムオブジェクトの両方を含む、公開済みオブジェクトまたは未公開オブジェクトにフィールドを追加できます。

オブジェクトが [公開](./creating-objects.md#publishing-object-drafts) されると、ドラフトのデータ定義を使用して初期データベーステーブルが作成されます。 このテーブルには、公開時に存在するすべてのオブジェクトフィールドと関係が含まれます。 公開後にオブジェクトに追加されたフィールドと関係は、サイドテーブルに追加されます（つまり、 `[Initial_Table_Name]_x`）。

```{important}
フィールドがオブジェクトドラフトに保存されている場合は、その設定と値を編集できます。 ただし、フィールドが公開されるか、公開されたオブジェクトに保存されると、そのラベルのみを編集できます。 他のすべての値と設定は変更できません。 

オブジェクトドラフトのフィールドは削除できます。 ただし、最初の公開後、最初の公開後に追加されたフィールドを除いて、フィールドを削除することはできません。これらのフィールドはサイドテーブルに追加されたためです。
```

次の手順に従って、オブジェクトに新しいフィールドを追加します。

1. **オブジェクト** ポートレットを開きます。

1. 目的のオブジェクトを選択します。

1. ［**Fields**］ タブをクリックし、 **追加** ボタン（![Add Button](../../../images/icon-add.png)）をクリックします。

   ![［Fields］タブで、追加ボタンをクリックし、必要な詳細を入力します。](./adding-fields-to-objects/images/01.png)

1. **ラベル** と **項目名** を入力します。

   **ラベル** ：この値は、オブジェクトUIでフィールドを識別し、フィールドの作成後にローカライズできます。

   **項目名** ：この値は、バックエンドでのフィールドの名前を決定し、キャメルケースを使用します。 フィールドが公開されると、この値は変更できません。

   ```{important}
   次のフ項目名はLiferayによって予約されており、カスタムフィールドには使用できません： `companyId`、` createDate`、 `groupId`、` id`、 `lastPublishDate`、` ModifiedDate`、 `status`、` statusByUserId`、 `statusByUserName `、` statusDate`、 `userId`、` userName`。 ユーザーがこれらの項目名のいずれかを使用してフィールドを作成しようとすると、Liferayはエラーメッセージを表示します。
   ```

1. フィールドの **タイプ** を選択します。 詳細については、 [Field Type Reference](#field-type-reference) を参照してください。

1. フィールドが ［**Mandatory**］ かどうかを決定します。

1. ［**保存**］ をクリックします。

フィールドをオブジェクトドラフトに保存した後、フィールドを選択して、検索可能かどうかを定義できます。 デフォルトでは、すべてのフィールドが検索可能です。

![フィールドを保存した後、検索可能かどうかを決定します。](./adding-fields-to-objects/images/02.png)

<a name="field-type-reference" />

## フィールドタイプリファレンス

| タイプ                   | 説明                                         |
| --------------------- | ------------------------------------------ |
| BigDecimal            | 計算に使用される小数点付きの高精度数値                        |
| ブール値                  | **true** または **false** の論理的なバイナリ値                 |
| 日付                    | 特定の日、月、年を示す値                               |
| 二重線                   | 浮動小数点を含む64ビットの数値                           |
| 整数                    | 浮動小数点を含まない32ビットの数値                         |
| Long (Automatic Copy) | 浮動小数点を含まない64ビットの数値                         |
| 選択リスト                 | [選択リスト](../using-picklists.md)に格納されている文字列値 |
| 文字列                   | 文字のシーケンス（文字、数字、句読点など）                      |

<a name="additional-information" />

## 追加情報

* [オブジェクトの作成](./creating-objects.md)
* [オブジェクトリレーションの定義](./defining-object-relationships.md)
* [オブジェクトレイアウトの設計](./designing-object-layouts.md)
* [オブジェクトの管理](./managing-objects.md)
