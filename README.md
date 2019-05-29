# blue011consume
Example of consuming revertible DASH address. This withdraws funds from revertible address by using "Message and PIN".

The wallet address into which DASH coin is deposited is mentioned in below line of ./blue011consumemessage5.json file.

``` bash

  "target": "yVdmyRn9WKBdyK71JUPWzX2Q2aRpHqs8dz",

```

This example uses testnet.

To get access to use this. Contact puppipay team (puppipay01@gmail.com).

## Content of ./blue011consumemessage5.sh

``` bash
curl -X POST -H "Content-Type: application/json" -H "Authorization: ApiKey eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjVjZTY4MThjNWIyMmMxMzlkZGJiZDAxNCIsImlhdCI6MTU1ODYxMDMxOX0.lPzOyj3jrbNhsv--gOkKXKxdTA-vMJnVc2X0pMt8iZs" \
 -d @blue011consumemessage5.json \
 https://dashrevert.belavaditech.com/blue011/consumemessage

```
~                                                        


## Content of ./blue011consumemessage5.json

``` bash

{
  "message": "eyJjcmMiOiI1YmE0OTgiLCJ1aWQiOiIwMjdjOTg5YTBmOTdkMGFiZjE4MTE4ZjNhZmRjMjJkN2VkNDJhOThiY2MyMWU1ZDRlZjljN2NiNzhmMTczMDBjOTYiLCJwaW5kYXRhIjp7ImlkIjoiVEVTMTU1NTc1Nzg5NTE2NiIsImRhdGUiOiIxNTU5MTE5ODk2NDkxIiwicGluIjoiIn19",
  "pin": "PIN_4PENW2EQ3",
  "target": "yVdmyRn9WKBdyK71JUPWzX2Q2aRpHqs8dz",
  "network": "testnet",
  "type": "BLUE011"
}

```

## Output of command execution of ./blue011consumemessage5.sh

``` bash
./blue011consumemessage5.sh
{
  "amount": 216505,
  "fromaddress": "8pUwBaHuj76YYg5aLHRU3f2XnaPnoiHj6n",
  "toaddress": "yVdmyRn9WKBdyK71JUPWzX2Q2aRpHqs8dz",
  "txid": "ebb130e2ac0bcffcf87ac0ab3ec987ee3bb24467bf96538062833854ab74bc86"
}


```

## To check balance in address use below example

https://testnet-insight.dashevo.org/insight-api/addr/8pUwBaHuj76YYg5aLHRU3f2XnaPnoiHj6n

``` bash
{"addrStr":"8pUwBaHuj76YYg5aLHRU3f2XnaPnoiHj6n","balance":0,"balanceSat":0,"totalReceived":0,"totalReceivedSat":0,"totalSent":0,"totalSentSa
t":0,"unconfirmedBalance":0,"unconfirmedBalanceSat":0,"unconfirmedTxApperances":0,"unconfirmedAppearances":0,"txApperances":0,"txAppearan
ces":0,"transactions":[]}

```
       

