# How to get Azure resource cost by using Az_Cost_management API call - grouped by Tags  

**Params**
	api-version: 2023-11-01
	scope: /subscriptions/<your_subs_id>/
**Authorisation**
	Bearer Token: <>
**Headers**
	Content-Type: application/json
	SubscriptionId: 3a56c060-2d3e-431f-824a-23c67c266e14
**Body**
<code>
{
    "type": "Usage",
    "timeframe": "MonthToDate",
    "dataset": {
        "granularity": "None",
        "aggregation": {
            "totalCost": {
                "name": "PreTaxCost",
                "function": "Sum"
            }
        },
        "grouping": [
            {
                "type": "TagKey",
                "name": "mytag1"
            }
        ]
    }
}
</code>code>
