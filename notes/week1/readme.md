# Class 1

---

We have covered basics of the solana environment in that class and at the end of the class, `spl-token` is used to demonstrate creating a fungible token.

- [Account](#account)
- [Programs](#program)
- [Transaction](#transaction)
- [IDL](#idl)
- [SPL Token](#spl-token)

### [Account](#account)

---

All data is stored in `accounts` on Solana. You can think of it like a **key-value** pair on the database and each entry is called as **account**

![accounts](/notes/week1/images/accounts.svg)

_Key-value pair demonstration from [Solana](https://solana.com/docs/core/accounts)_

> [!IMPORTANT]
> Accounts can store up to **10MB** of data, which can consist of either _executable program code_ or _program state_.

> [!WARNING]
> Accounts require a **rent** deposit in SOL, proportional to the amount of data stored, which is fully refundable when the account is closed.

There is an `ownership terminology` in Solana which an account can only be created by the **System Program**. That is, owner of the account is actually System Program but it gives ownership to the related address that call that system program.

How an account info object looks like👇

```js
{
key: number,
lamports: number,
data: Uint8Array,
is_executable: boolean,
owner: PublicKey,
}
```

### How can we reach those accounts? 🤔

Each account is identifiable by its unique address, represented as 32 bytes in the format of an [**Ed25519**](https://cryptography.io/en/latest/hazmat/primitives/asymmetric/ed25519/) `PublicKey`. You can think of the address as the unique identifier for the account.

![accounts](/notes/week1/images/account-address.svg)

_Account address demonstration from [Solana](https://solana.com/docs/core/accounts) Docs_

### [Programs](#programs)
