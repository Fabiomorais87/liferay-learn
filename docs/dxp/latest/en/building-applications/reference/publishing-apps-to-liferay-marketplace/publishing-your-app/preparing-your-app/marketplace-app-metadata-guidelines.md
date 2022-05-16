# Marketplace App Metadata Guidelines

The following app metadata guidelines ensure that apps are submitted with important and necessary supporting information. The metadata that you submit with your app serves both as necessary information for your app’s buyers (e.g., your contact info) and as promotional assets (e.g., description, screenshots, etc.) that can help drive traffic to and downloads of your app.

Think of a good name and description for your app. If you haven’t already done so, take some screenshots, design an icon, and create a website for your app. The table below helps you address the Marketplace app metadata requirements and produce an appealing app advertisement.

Marketplace App Metadata Guidelines:

| Required Metadata | Description |
| --- | --- |
| App Name | This is probably the most important branding element of your app, so be creative! Some important things to keep in mind: 1. In some views within the Marketplace, app titles longer than 18 characters are shortened with an ellipsis. 2. Titles must not be longer than 50 characters. 3. App title may contain the word "Liferay" to describe its use or intent as long as the name does not imply official certification or validation from Liferay, Inc. (For example, names such as "Exchange Connector for Liferay" or "Integration Connector Kit for Liferay" would be allowed, while "Liferay Mail Portlet," "Liferay Management Console," or "Liferay UI Kit" would not be permissible without explicit approval). Please refer to our [trademark policy](https://www.liferay.com/pt/trhttps://www.liferay.com/pt/trademarkademark) for details. 4. Please try to conform the app name as closely as possible to the actual plugin (portlet, module, theme, etc.) name. |
| Support Information | Please include an email address, contact information, and/or website URL for the "Support" field. If there's an issue with your app, they should be a way to contact you. If you choose not to offer Support Services (by unchecking "Offer Support" during the app submission process), you must provide support contact information so that buyers can ask you general questions about your app. |
| Description | Using English as the default language, you must provide a description for your app. After providing the description in English, you can provide other translations of the text. At a minimum, the description should provide a concise overview of what the app does. Great descriptions also list key functionality and what customers can expect to gain by deploying your app. For a good description example, see the [Audience Targeting](https://web.liferay.com/marketplace/-/mp/application/43707761) app on the [Marketplace](https://web.liferay.com/marketplace). |
| What's New?* | Using English as the default language, describe what's new and improved in your app. After this, you can provide other translations of the text. This field is shown on updating an app that you've already submitted, regardless of whether the app has been published. |
| Compatibility with Future Minor Releases of Liferay | Please include a "+" at the end of the latest version when specifying version constraints in your liferay-plugin-package.properties file (e.g., "liferay-versions=7.2.1+, 7.2.20+"). This ensures that the app continues to be deployable to future Liferay Portal versions within a minor release. If, in the future, you discover your app does NOT work with a particular version, you can modify the list to exclude that version. |
| Increase Your Potential User Base | In most cases, an app compatible with Liferay Portal CE also runs on Liferay Digital Experience Platform (DXP) (or Liferay Portal EE), and vice versa. Specifying compatibility with both DXP/EE and CE versions of Liferay ensures a wider audience for your app! You can [request a Developer License](https://web.liferay.com/web/developer/marketplace/license) to support testing and confirm compatibility. |
| Icon | App icons must be exactly 90 pixels in both height and width in PNG, JPG, or GIF format. The image size cannot exceed 512kb. Animated images are prohibited. The use of the Liferay logo, including alternate versions of the Liferay logo, is permitted only with Liferay's explicit approval. Please refer to our [trademark policy](https://www.liferay.com/pt/trademark) for details.|
| Screenshots | App screenshots must not exceed 1080 pixels in width x 678 pixels in height and must be in the JPG format. Each screenshot's file size must not exceed 384KB. Each screenshot should be the same size (each is automatically scaled to match the aspect ratio of the above dimensions), and it is preferable to name screenshots sequentially, for example fluffy-puppies-01.jpg, fluffy-puppies-02.jpg, and so on.|

Make sure your icons, images, descriptions, and tags are free of profanity or other offensive material.

During the publication process, you upload your app’s individual plugin WAR files and module JAR files along with the app’s metadata (name, description, version, icon, etc.).

## Additional Requirements for Themes/Site Templates

Themes and Site Templates must include sample content and optionally link to a demo website that provides context. This ensures a uniform experience for Marketplace users: they download a Theme or Site Template from Marketplace, install it, go to Sites or Site Templates in the Control Panel, and immediately see the Theme or Site Template in action.

```{important}
Demo sites must be valid. Demo website, Theme, and Site Template sample content must not plagiarize or infringe on copyrights.
```

The Resources Importer includes files and web content that imports automatically into Liferay on Theme and Site Template deployment. Use the Resources Importer to include files/web content to provide a sample context for your Theme or Site Template. The Themes tutorials provide details.