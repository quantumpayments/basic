# basic

## basic payment workflow

- setup storage
- setup wallet
- setup setup webcredits
- setup tables
- setup coinbase
- test


## setup storage

Storage is provided via Solid using ldnode or gold, the root is set to localhost

External wallets may be used, alter as necessary

## setup wallet

`wallet` goes to https://localhost/wallet/basic#this

```
<#this>
    <http://purl.org/dc/terms/description> "Basic Wallet" ;
    a <https://w3id.org/cc#Wallet> ;
    <https://w3id.org/cc#inbox> <inbox/> ;
    <https://w3id.org/cc#tx> <tx/> .
```

Add folders `tx` and `inbox`

## setup webcredits

    sudo npm install -g webcredits

## setup tables

    credit create [-d database]

Normally you will have mysql installed, with a database webcredits

## setup coinbase

    credit genesis [-d database] [-w wallet]

## testing

Testing balance

    credit balance "https://w3id.org/cc#coinbase" [-w wallet]

Should give 1000000

Testing transaction

    credit insert https://w3id.org/cc#coinbase 100000 '' 'https://workbot.databox.me/card/profile#me' [-d database] [-w wallet]

Add more transactions for basic ledger functionality
