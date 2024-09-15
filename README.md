# How to get Azure resource cost by using Az_Cost_management API call - grouped by Tags  

#### Params
	api-version: 2023-11-01
	scope: /subscriptions/<your_subs_id>/
#### Authorisation
	Bearer Token: <>
#### Headers
	Content-Type: application/json
	SubscriptionId: 3a56c060-2d3e-431f-824a-23c67c266e14
#### Body
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
</code>

#### RESPONSE
<code>
{
    "id": "subscriptions/<sub_id>/providers/Microsoft.CostManagement/query/ae7b891d-b5f1-4ba0-9f59-16b6113c7a3a",
    "name": "ae7b891d-b5f1-4ba0-9f59-16b6113c7a3a",
    "type": "Microsoft.CostManagement/query",
    "location": null,
    "sku": null,
    "eTag": null,
    "properties": {
        "nextLink": null,
        "columns": [
            {
                "name": "PreTaxCost",
                "type": "Number"
            },
            {
                "name": "TagKey",
                "type": "String"
            },
            {
                "name": "TagValue",
                "type": "String"
            },
            {
                "name": "Currency",
                "type": "String"
            }
        ],
        "rows": [
            [
                169.5230799485,
                "mytag1",
                null,
                "USD"
            ]
        ]
    }
}

</code>
