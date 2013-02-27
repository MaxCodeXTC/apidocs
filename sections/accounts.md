# Account Endpoints

| Endpoint | Description |
| ---- | ---- |
| [GET /v1/accounts](https://github.com/oanda/apidocs/blob/master/sections/accounts.md#get-v1accounts) | Get a list of accounts belongs to user |
| [GET /v1/accounts/:account_id](https://github.com/oanda/apidocs/blob/master/sections/accounts.md#get-v1accountsaccount_id) | Get detailed balance and holding information for :account_id |

## GET /v1/accounts

#### Request
    http://api-sandbox.oanda.com/v1/accounts?username=test_user_abc

#### Response
    [
        {"id":1, name:"Primary", homecurr:"USD", marginRate:0.20, "accountPropertyName":[]},
        {"id":2, name:"Subaccount 1", homecurr:"CAD", marginRate:0.30, "accountPropertyName":[]},
        {"id":3, name:"Subaccount 2", homecurr:"EUR", marginRate:0.50, "accountPropertyName":[]},
        {"id":4, name:"MT4 Account", homecurr:"EUR", marginRate:0.50, "accountPropertyName":["MT4"]},
        {"id":4, name:"Beginner Account", homecurr:"EUR", marginRate:0.50, "accountPropertyName":["BEGINNER"]}
    ]

#### Query Parameters
**Required**

* **username**: username of accounts holder


## GET /v1/accounts/:account_id
#### Request
    http://api-sandbox.oanda.com/v1/accounts/:account_id

#### Response
    {
	"accountId" : 1,
	"accountName" : "Primary",
	"balance" : 499845,
	"unrealizedPl" : 0,
	"realizedPl" : 0,
	"marginUsed" : 0,
	"marginAvail" : 499845,
	"openTrades" : 0,
	"openOrders" : 0,
	"marginRate" : 0.02,
	"homecurr" : "USD"
    }
