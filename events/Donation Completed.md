# Donation Completed

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Donation Completed",
    "donation": {
        "cardType": "<cardType>",
        "donationFrequency": "<donationFrequency>",
        "donationType": "<donationType>",
        "isCardRequested": "<isCardRequested>",
        "item": [
            {
                "donationID": "<donationID>"
            }
        ],
        "profile": {
            "address": {
                "city": "<city>"
            }
        },
        "total": {
            "currency": "<currency>"
        },
        "transactionID": "<transactionID>"
    }
});
```

## Variable Definitions

|Field|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|cardType|string|Describes the type of card requested as part of a donation.|Electronic, Physical|||||||
|city|string|The mailing city associated with the donation payment. |Atlanta, New York, Los Angeles, Chicago|||||||
|currency|string|Currency of the donation payment. ISO 4217 (3 character alpha), uppercase |USD, CAD, GBP, CHF|^[A-Z]{3}$|3|3||||
|donationFrequency|string|Recurrence frequency of donation. |One Time, Monthly|||||||
|donationID|string|Unique identifier of the donation. Max Length 20. Used to prevent duplication.||^[a-zA-Z0-9]{6,20}$|6|20||||
|donationType|string|Type of donation selected. |Tribute, General, Fundraiser|||||||
|isCardRequested|boolean|Boolean flag indicating whether a card was requested as part of a donation.|TRUE, FALSE|||||||
|transactionID|string|Unique identifier of the transaction. Max Length 20. Used as a key for upload of post transaction data. ||^[a-zA-Z0-9]{6,20}$|6|20||||
