# How to get Azure resource cost by using Az_Cost_management API call - grouped by Tags  

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
