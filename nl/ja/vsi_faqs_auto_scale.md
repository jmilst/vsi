---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-13"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# FAQ: オート・スケール
{: #faqs-auto-scale}

## ベア・メタル・オート・スケール・インスタンスはオート・スケールでサポートされますか?
{: faq}

現時点では、ベア・メタル・オート・スケール・インスタンスはオート・スケールでサポートされません。

## オート・スケールはロード・バランサーと連動しますか?
{: faq}

はい。現在、オート・スケールはローカル・ロード・バランサーに対して有効であり、ロード・バランサー API の一部を使用します。 詳しくは、[スケール・ロード・バランサー](/docs/vsi?topic=virtual-servers-auto-scale-terminology)を参照してください。

## オート・スケール終了ポリシーにはどのような種類がありますか?
{: faq}

オート・スケール終了ポリシーには、「最新」、「最古」、「次回課金が最も近づいている」の 3 つがあります。 これらは、グループのスケールダウン時に削除するメンバーを選択する方法を表しています。 詳しくは、[終了ポリシー](/docs/vsi?topic=virtual-servers-auto-scale-terminology)を参照してください。

## オート・スケール・ポリシーとは何ですか？
{: faq}

ポリシーとは、一連のアクションと一連のトリガーをまとめたものです。 通常、ポリシーは、名前、クールダウン、アクション、トリガーという要素から構成されます。 詳しくは、[ポリシー](/docs/vsi?topic=virtual-servers-auto-scale-terminology)を参照してください。

## オート・スケール・トリガーとは何ですか？
{: faq}

トリガーとは、(グループがアクティブな場合のみ) 満たされる可能性がある条件のことです。 トリガーには、「1 回」、「繰り返し」、「リソース使用量」の 3 つのタイプがあります。 詳しくは、[トリガー](/docs/vsi?topic=virtual-servers-auto-scale-terminology)を参照してください。

## 最大 VSI メンバー数とは何ですか？
{: faq}

グループに存在できる最多メンバー数のことです。 詳しくは、[最大 VSI メンバー数](/docs/vsi?topic=virtual-servers-auto-scale-terminology)を参照してください。

## 最小 VSI メンバー数とは何ですか？
{: faq}

グループに存在できる最少メンバー数のことです。 詳しくは、[最小 VSI メンバー数](/docs/vsi?topic=virtual-servers-auto-scale-terminology)を参照してください。

## オート・スケール資産とは何ですか？
{: faq}

資産とは、メンバー数に寄与せず、自動制御を受けない、グループ内の固定メンバーのことです。 資産は、ポリシー・トリガーに追加情報を提供するために存在します。 例えば、CPU パーセンテージをトリガーとして使用する場合に、資産をグループ全体の CPU パーセンテージに加えることができます。 現在、グループには仮想ゲスト資産のみを設定できます。その数に制限はありません。 また、グループは必須ではありません。

## オート・スケール・グループとは何ですか？
{: faq}

グループ (スケール・グループ) とは、資産、メンバー、スケール・ロード・バランサー、VLAN、ポリシーで構成される集合であり、グループに固有のものです。 メンバー数の境界、スケーリングする仮想サーバー・インスタンスのメンバーのテンプレートなど、スケーリングに関するすべてのパラメーターはグループに設定します。

## オート・スケール・メンバーとは何ですか？
{: faq}

メンバーとは、グループ内のスケーリング単位です。 メンバーは、ポリシー・アクションに基づいて自動的にプロビジョンまたは回収されます。 現在、すべてのメンバーは仮想サーバー・インスタンスです。 アクティブ・グループでは、メンバー数が最小値より少なくなることも、最大値より多くなることもありません。 通常、メンバーはポリシーのアクションによって追加されますが、ユーザーが手動で追加することもできます。