# PayPal

この記事では、PayPalを支払い方法として有効にする方法について詳しく説明します。

PayPalを使用するようにストアを設定する前に、PayPalクライアントIDとクライアントシークレット番号を生成する必要があります。 詳細は、 [PayPal開発者ダッシュボード](https://developer.paypal.com/developer/applications/create) にアクセスしてください。

1. ［**サイト管理］ → ［コマース］ → ［設定］ → ［支払い方法**］ に移動します。
1. ［**PayPal**］ をクリックします。
1. ［**設定**］ をクリックします。
1. 次のように入力します：
    ***クライアントID**
    ***クライアントシークレット**
1. ライブサイトの場合は ［**Live**］ を、テスト環境の場合は ［**Sandbox**］ を選択します。
1. ［**最大決済試行回数**］ フィールドに、サブスクリプションをキャンセルする前にサブスクリプションの支払いを試行する回数を入力します。
    * 詳細は、PayPalの記事 [「Reattempt failed recurring payments with Subscribe buttons」](https://developer.paypal.com/docs/paypal-payments-standard/integration-guide/reattempt-failed-payment/) を参照してください。 ![PayPalの設定](./paypal/images/01.png)
1. ［**保存**］ をクリックします。
1. ［**PayPal**］ の隣にある **3ドットアイコン** をクリックし、次に ［**有効にする**］ をクリックします。

PayPalがストアで有効になりました。

<a name="additional-information" />

## 追加情報

他の支払い方法の追加に関する詳細は次のとおりです。

* [新しい通貨の追加](../currencies/adding-a-new-currency.md)
* [Authorize.net](./authorize.net.md)
* [Mercanet](./mercanet.md)
* [購読ボタンで失敗した定期的な支払いを再試行する](https://developer.paypal.com/docs/paypal-payments-standard/integration-guide/reattempt-failed-payment/)
