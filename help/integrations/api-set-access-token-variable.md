---
title: Marketoの API に関するビデオ – アクセストークンを変数に設定する方法
description: Postman アプリケーションを設定する方法と、変数を活用してデータを変数に保存し、再利用性を確保する方法について説明します。
feature: REST API
role: Admin, Developer
level: Beginner
doc-type: Technical Video
duration: 772
last-substantial-update: 2024-08-06T00:00:00Z
jira: KT-15548
source-git-commit: dfe4f1d9737cb0c69bbd96aedf6c61953315fa9b
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---


# API ヘルプ – 変数にアクセストークンを設定する方法

Postman アプリケーションを設定し、変数を活用して、再利用目的でデータを変数に保存する方法を説明します。 また、アクセストークンを取得するための最初のMarketo Engage REST API 呼び出しを行う方法についても説明します。

>[!PREREQUISITES]
>
>このビデオを開始する前に、AOI の役割を持つ API のみのユーザー名を作成し、Launchpad サービスを作成します。 以下の記事の手順に従います。
>
>* [API のみのユーザーロールの作成 ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/users-and-roles/create-an-api-only-user-role){target="_blank"}
>
>* [API のみのユーザーの作成 ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/users-and-roles/create-an-api-only-user){target="_blank"}
>
>* [REST API で使用するカスタムサービスの作成 ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/additional-integrations/create-a-custom-service-for-use-with-rest-api){target="_blank"}

**このビデオで使用されている参照：**

* Marketo認証エンドポイント：`{{{}base_url{}}}/identity/oauth/token?grant_type=client_credentials&client_id={{{}client_id{}}}&client_secret={{{}client_secret{}}}`

* 応答本文から access_token を取得する JS スクリプト（「Scripts:」タブの下）:

```
var jsonData = pm.response.json();
pm.environment.set("access_token", jsonData.access_token);
```

* [Marketo Engage開発者向けドキュメント ](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/rest/authentication){target="_blank"}

>[!VIDEO](https://video.tv.adobe.com/v/3429275/?learn=on)
