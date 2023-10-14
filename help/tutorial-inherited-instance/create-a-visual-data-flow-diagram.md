---
title: 視覚的なデータフロー図を作成して、マーケティングテクニカルスタックを理解する
description: 「リードとデータソース」の図を作成してデータウィンドウを理解し、インスタンスを効率的に監査および整理する方法を説明します。
feature: Administration
role: Admin
level: Intermediate, Experienced
doc-type: Tutorial
last-substantial-update: 2023-10-03T00:00:00Z
jira: KT-13877
thumbnail: KT-13877.jpeg
hide: true
source-git-commit: e7fe8da128a1c46620484d9b92823ba51791a671
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 0%

---


# 視覚的なデータフロー図を作成して、マーケティングテクニカルスタックを理解する

を引き継ぐ管理者として [!DNL Marketo Engage] 何年もの間生きてきたインスタンスは、インスタンスを効率的に監査し、整理するのが不可能なミッションのようです。 WhenAdobe [!DNL Marketo Champion]ケリー・ジョ・ホートンは、長年の経験を踏みにじり、この挑戦に取り組みました。 [「リードとデータソース」の図の作成](https://nation.marketo.com/t5/employee-blogs/understand-your-marketing-technology-and-data-create-this/ba-p/296774){target="_blank"} データウィンドウに慣れるために このチュートリアルでは、Kelly Jo Horton が共有する例を基に、独自のデータフロー図を作成する方法を学びます。 MarTech エコシステムについてお知らせします。

## 継承されたインスタンスのアーキテクチャ図を作成するのはなぜですか？

1. **ライブインスタンスから継承したマーケティングテクニカルスタックに慣れてください。** マーケティング操作マネージャー/プラットフォーム操作マネージャーは、新しい会社に入社する際に、この演習を実行することをお勧めします。 この作成プロセスにより、管理者ユーザーは、外部統合からに送信されたデータおよびアクティビティの全体像を確認できます。 [!DNL Marketo Engage] API エラーのトラブルシューティングを容易に行う。
2. **外部統合を管理する主要な関係者に慣れてください。** Kelly Jo Horton が、関係者をすばやく特定するために使用するヒントは、API ユーザーのリストを参照することです。
   1. **「管理者」セクションの「統合/LaunchPoint」タブに移動します。** 「LaunchPoint」タブに移動する方法の詳細を説明します。 [REST API で使用するカスタムサービスの作成](https://experienceleague.adobe.com/docs/marketo/using/product-docs/administration/additional-integrations/create-a-custom-service-for-use-with-rest-api.html){target="_blank"}.
   2. 「 API 呼び出し情報」セクションの統合/「Web サービス」タブで、API ユーザー別の API 使用統計を見つけます。 API 呼び出し番号をクリックすると、各ユーザーによっておこなわれた特定の個々の呼び出しを表示できます。

## このビジュアルデータフロー図の実習方法

### 手順 1：現在の状態の図

「現在の状態」図を作成します。 次に例を示します。

![現在の状態図](/help/tutorial-inherited-instance/_assets/data-flow-diagram/Current_State_Lead_Data_Sources_KellyJo_Horton.png){align="center"}


### 手順 2：将来の状態図

技術以外の関係者に対して技術とシステムのロードマップを提示する際に使用できる「未来の状態」図を作成します。 次に例を示します。

![将来の状態図](/help/tutorial-inherited-instance/_assets/data-flow-diagram/Future-State-Lead-Data-Sources-KellyJo-Horton.png){align="center"}

### 手順 3：技術バージョン

各統合の API ユーザー名や、にプッシュされるデータのタイプの短い説明などの詳細を示す技術バージョンを作成します。 [!DNL Marketo Engage] または引き出された [!DNL Marketo Engage]、およびミドルウェアのフローとトリガーの詳細な図。  次に例を示します。

![技術版](/help/tutorial-inherited-instance/_assets/data-flow-diagram/Lead-Data-Source-Diagram-KellyJo-Horton.png){align="center"}


## 次の手順

**使用の手引き：**
サンプルのデータフロー図の 1 つをダウンロードして、マーケティング技術スタック、人物およびデータフローの現在の状態をマッピングしたり、インスタンスを監査する際にデータウィンドウの図を一から作成したりします。


<table style="table-layout:fixed">
   <tr>  
      <td style="border: 0;">
      <div style="text-align: center;">
          <a href="./_assets/downloads/Current_Future_State_Lead_Data_Sources.zip">
            <strong>現在の状態と将来の状態</strong>
         </a>
      </div>
      </td>
      <td style="border: 0;">
      <div style="text-align: center;">
         <a href="./_assets/downloads/Detailed_Layers_by_Functional_Category_Stacked_Technologies.zip">
         <strong>機能カテゴリ別の詳細レイヤ </strong>   
         </a>
      </div>
      </td>
      <td style="border: 0;">
         <div style="text-align: center;">
         <a href="./_assets/downloads/Lead_Data_Source.zip">
           <strong>リードとデータソースのフロー </strong>  
         </a>
         </div>
       </td> 
       <td style="border: 0;">
         <div style="text-align: center;">
         <a href="./_assets/downloads/Simple_World_Class_Stage_Stack.zip">
          <strong>簡易図</strong>  
         </a>
         </div>
        </td>  
   </tr>
   <tr>
    <td style="border: 0;">
         <div>
          <img alt="現在の状態と将来の状態の図" src="./_assets/Thumbnail_Current-Future State Lead_Data Sources_KellyJo_Horton.png"/>
         </a>
      </div>
      </td>
      <td style="border: 0;">
         <div>
         <a href="./_assets/downloads/Detailed_Layers_by_Functional_Category_Stacked_Technologies.zip">
         <img alt="機能カテゴリ別の詳細レイヤ図" src="./_assets/Thumbnail_Detailed_Layers_by_Functional_Category_Stacked_Technologies_KellyJo_Horton.png" />
       </a>
         </div>
      </td>
       <td style="border: 0;">
         <div>
            <a href="./_assets/downloads/Lead_Data_Source.zip">
         <img alt="リードとデータソースのフロー図" src="./_assets/Thumbnail_Lead-Data Source Diagram_KellyJo_Horton.png" />
         </a>
         </div>
      </td>
     <td style="border: 0;">
         <div>
            <a href="./_assets/downloads/Simple_World_Class_Stage_Stack.zip">
             <img alt="簡易図" src="./_assets/Thumbnail_Simple_World_Class_Stage_Stack.png" />
         </a>
         </div>
      </td>
</table>

以下のツールを使用できます： draw.io (Google Docs)、Adobe XD、Figma、Gliffy (Confluence)

**アーキテクチャ図が既に存在する場合はどうなりますか？** 新しいチームメンバーは、異なる視点を持つことができます。 新しい [!DNL Marketo Engage] 管理者は、オンボーディングプロセスの一部としてこの演習をおこない、他のユーザーと共有します。

## 発言者

**ケリージョホートン**\
AdobeMarketoチャンピオンの同窓生
*Etumos のシニアクライアントパートナー*

![ケリージョホートン](/help/tutorial-inherited-instance/_assets/authors/Customer_Author_Kelly_Jo_Horton.png){width="30%"}

**エイミーチウ**
*導入とリテンションマーケティングマネージャ、Adobe*

![エイミーチウ](/help/tutorial-inherited-instance/_assets/authors/Adobe_Author_Amy_Chiu.png){width=30%}
