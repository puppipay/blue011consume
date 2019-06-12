# blue011consume
Example of receiving (consuming) funds from DASH revertible-address. It takes input of "Locking-Message and PIN". It also needs target address (optional) to direct funds to target address.

If target address is not specified, the funds get deposited with account holder. (Not shown in example)

In the example provided, the wallet address into which DASH coin is deposited is mentioned in below line of ./blue011consumemessage5.json file.

``` bash

  "target": "yVdmyRn9WKBdyK71JUPWzX2Q2aRpHqs8dz",

```

This example uses testnet.

To get individual-access. Contact puppipay team (puppipay01@gmail.com).

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
# Images of steps to receive fund

## Assume you have received Locking-message and PIN as follows


The Locking-message is 
 ``` bash
 
 "message":  "eyJjcmMiOiIyMGUwNjEiLCJ1aWQiOiIwMjEyOGM1OTAzMDNkMTMwZTFmZWMxZWQyNDUzMjE3MGE5OThkOGIxNGYyZWNjNDRiOWY5OTE4MjIyMWVhZGM0MjQiLCJwaW5kYXRhIjp7ImlkIjoiVEVTMTU1NTc1Nzg5NTE2NiIsImRhdGUiOiIxNTYwMjIwNDgyMjIxIiwicGluIjoiIn19"
 
 ``` 
 
 The PIN to unlock is
 ``` bash
 
  "pin": "PIN_6HGPPNB21",
  
  ``` 
  
  The DASH revertible-address having fund is
 
 ``` bash
 
 "address": "92wN1HFM2qmarbxwN25EeeTC4iiF1dZzcx",
 
   ``` 
## Get your testnet wallet address. 

This is needed to receive funds from reveritible-address.

In below image, the testnet address is created in https://testnet1.puppipay.com/#/WelcomePage

<img src="workingimages/walletadd.png" alt="alt text" width="400">

The wallet address is yVdmyRn9WKBdyK71JUPWzX2Q2aRpHqs8dz

## Download consume script to receive funds from DASH revertible-address

<img src="workingimages/redeemscriptget.png" alt="alt text" width="400">

## Update target field in blue011consumemessage5.json 

The target fields should have the "wallet address" into which the funds should be deposited, when fund is received from DASH revertible-address.

<img src="workingimages/updatetarget.png" alt="alt text" width="400">


## Execute the blue011consumemessage5.sh to receive fund

<img src="workingimages/consumedanddisplayed.png" alt="alt text" width="400">

On the left image see the command is executed. It shows fromaddress, toaddress. On Right side of image you see fund received in wallet.

## Reverting feature 

While updating blue011consumemessage5.json, if the target field specifies your wallet(sender), the funds return back to your wallet address.

``` 

       

