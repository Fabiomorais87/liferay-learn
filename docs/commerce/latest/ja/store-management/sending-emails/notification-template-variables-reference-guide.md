# 通知テンプレート変数リファレンスガイド

電子メール通知テンプレートを作成するときに、電子メールコンテンツの **電子メール設定** および **ボディ** フィールドにキー値の代わりとして変数を挿入できます。 キーの値には、顧客の名前、注文ID、配送先と請求先の住所、注文のアイテムのリストが含まれます。

![これらの変数を「Eメール本文」フィールドで使用します。](./notification-template-variables-reference-guide/images/02.png)

使用可能な変数を表示するには、最初に通知テンプレートタイプを選択して有効にします。

![最初に通知テンプレートのタイプを選択します。](./notification-template-variables-reference-guide/images/01.png)

テンプレートタイプを選択したら、［**用語の定義**］ドロップダウンメニューを展開します。

<a name="email-settings" />

## メール設定

![これらの変数を「Eメール設定」フィールドで使用します。](./notification-template-variables-reference-guide/images/03.png)

次の変数を使用して、送信者と受信者の電子メール設定フィールドに入力できます。

| 変数                               | 説明              |
| :--- | :--- |
| [%ACCOUNT_ROLE_ORDER_MANAGER%] | アカウントオーダーマネージャー |
| [%ORDER_CREATOR%]                | 注文を作成したユーザー     |
| [%ACCOUNT_ROLE_ADMINISTRATOR%] | アカウント管理者        |
| [%USER_GROUP_NAME%]            | ユーザーグループ名       |

<a name="orders" />

## ［注文］

![これらの変数Orders emailsを使用します。](./notification-template-variables-reference-guide/images/05.png)

次の変数は、注文タイプの電子メール通知テンプレートで使用できます。

| 変数                           | 説明                |
| :--- | :--- |
| [%ORDER_ITEMS%]              | 注文に含まれるすべてのアイテムの表 |
| [%ORDER_SHIPPING_ADDRESS%] | 注文の配送先住所          |
| [%ORDER_BILLING_ADDRESS%]  | 注文の請求先住所          |
| [%ORDER_ID%]                 | 注文ID              |

<a name="subscription" />

## サブスクリプション

![この変数をサブスクリプションに使用します。](./notification-template-variables-reference-guide/images/04.png)

次の変数は、サブスクリプションタイプの電子メール通知テンプレートで使用できます。

| 変数               | 説明  |
| :--- | :--- |
| [%PRODUCT_NAME%] | 商品名 |

<a name="additional-information" />

## 追加情報

* [通知テンプレートの使用](./using-notification-templates.md)
