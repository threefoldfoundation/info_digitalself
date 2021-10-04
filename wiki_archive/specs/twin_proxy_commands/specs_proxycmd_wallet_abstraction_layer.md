# Wallet Abstraction Layer

- lives in Twin Proxy = nodejs

## commands

#### wallet.account.register

- wallet.account.register accountname:... privatekey:...

Registers an account given a name and privatekey.

Returns info like in wallet.account.get

#### wallet.account.trustline.add

- wallet.account.trustline.add accountname:... trustlinename:...

Adds a trustline to an account given an accountname and trustline currency / issuer.

Example: wallet.account.trustline.add("my_account", "TFT:ISSUER")

Returns info like in wallet.account.get

#### wallet.account.trustline.info.get

- wallet.account.trustline.info.get accountname:... trustlinename:...

Retrieves info from the trustline as is available on blockchain, will not be available on all blockchains.

Example: wallet.account.trustline.info.get("my_account", "TFT:ISSUER")

Returns trustline information.

```json
{
  "currency": "some_currency_name",
  "issuer": "some_currency_issuer",
  "free_balance": balance,
  "url": "some_issuer_url"
}
```

#### wallet.account.get

- wallet.account.get accountname:..

```json
{
  "name": "some_account_name",
  "trustlines": [array_of_trustlines],
  "free_balance": balance,
  "address": "some_address",
  "signers": [list_of_signer_addresses]
}
```

#### wallet.account.delete

- wallet.account.delete accountname:..

Deletes an account given an accountname.

Returns nothing.

#### wallet.accounts.list

- wallet.accounts.list \*blockchain:tfgrid/stellar

Returns a list of account get responses.

#### wallet.money.send

- wallet.money.send accountname:... amount:100 currency:tft dest:$address

Sends money given:

- accountname: an accountname
- amount: amount in decimal
- currency: currency in string format (TFT)
- destination: destination address

Returns transaction receipt

```json
{
  "blockchain": "tfgrid/stellar",
  "hash": "some_tx_hash"
}
```

#### wallet.transactions.list

- wallet.transactions.list accountname:...

Return a list of transactions for a given account

```json
[
  {
    "blockchain": "tfgrid/stellar",
    "hash": "some_tx_hash",
    "from": "from_someone",
    "to": "to_someone",
    "amount": 0
  }
]
```

#### wallet.account.multisignature.register ...

- wallet.account.multisignature.register accountname:... address_to_add:... weight:...

Add another signer to an account given:

- accountname: account to extend
- address_to_add: signer to add
- weight: weight that the signer has on the account (max: amount_of_signers)

returns account get response.

#### wallet.account.multisignature.remove ...

- wallet.account.multisignature.remove accountname:... address_to_remove:...

Removes signer from an account given:

- accountname: account to extend
- address_to_add: signer to add

returns account get response.

## remarks

> \*: means optional

### return from command

- json
- schema needs to be defined (can be as example per command)
