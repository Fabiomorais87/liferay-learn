# OAuth2アプリケーションの作成

OAuth 2.0を使用して承認できるアプリケーションがある場合、Liferayがそれを認識できるように、そのアプリケーションを登録する必要があります。 これを行うには、 [**Control Panel**] → [**Configuration**] → [**OAuth2 Administration**] にアクセスします。

1. **追加**（![add](../../images/icon-add.png)）ボタンをクリックします。

2.  フォームに記入します（ [以下の説明](#oauth2-administration-reference) ）。

3. [**保存**] をクリックしてアプリケーションを保存します。

    ![アプリケーションを追加すると登録され、ユーザーが自分のデータへのアクセスを承認できるようになります。](./creating-oauth2-applications/images/01.png)

アプリケーションのOAuth2認証をLiferay Portalに追加する方法をマスターしました。 次に、アプリケーションがアクセスできるユーザーデータのスコープを定義する必要があります。

<a name="oauth2-administration-reference" />

<a name="oauth2-administration-reference" />

## OAuth2管理リファレンス

**Name：** アプリケーションにわかりやすいタイトルを付けます。

**Website URL：** アプリケーションのWebサイトへのリンクを追加します。

**Callback URIs：** ユーザーがアカウントへのアクセスを承認（または承認を拒否）した後にリダイレクトするURIを、少なくとも1つ（行区切り） 入力します。 これにより、サポートしている許可された承認タイプのハンドラーにリンクされます（以下を参照）。

**Client Profile：** そのプロファイルに適切な（安全な）承認タイプをフィルタリングするテンプレートを選択します。 たとえば、アプリケーションがWebアプリケーションの場合、 [**Web Application**] を選択すると、次の承認タイプが利用可能になり、自動的に選択されます：[Authorization Code]、[Client Credentials]、[Refresh Token]、および[Resource Owner Password Credentials]。 これらは、 [OAuth2 RFC 6749標準ドキュメント](https://tools.ietf.org/html/rfc6749) に記載されているOAuth 2の「フロー」です。 承認タイプを手動で選択する場合は、 [**Other**] を選択します。

**Allowed Authorization Types：** アプリケーションがサポートする定義済みのOAuth 2 [プロトコルフロー](https://tools.ietf.org/html/rfc6749#section-1.2) を選択します。 上記のさまざまなクライアントプロファイルで、いくつかの一般的な組み合わせが定義されています。

フォームを保存すると、追加のフィールドが表示されます。

**Client ID：** これはシステムによって生成されます。これはアプリケーションの識別子なので、@product@はユーザーデータへのアクセスを許可されているアプリケーションを認識します。

**Client Secret：****鉛筆** アイコンをクリックして、クライアントシークレットを生成します。 シークレットは、承認プロセス中にクライアントを識別します（上記の図1を参照）。 一部のクライアントプロファイルは秘密を保持できないため、すべてのクライアントプロファイルがクライアントシークレットを必要とするわけではありません。 これは、前述のPKCEコードのチャレンジと検証ツールが必要な場合です。

**Icon：** アプリケーションのユーザーがアプリケーションで識別するアイコンをアップロードします。 認証画面に表示されます。

**Privacy Policy URL：** アプリケーションのプライバシーポリシーへのリンクを追加します。

**Token Introspection：** @product@からリクエストすることで、アプリケーションがトークンからメタデータを取得できるようにします。 これは [RFC 7662](https://tools.ietf.org/html/rfc7662) を実装します。
