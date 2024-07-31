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

![Key-value pair demonstration from [Solana](https://solana.com/docs/core/accounts) ](/notes/week1/images/accounts.svg)

> [!IMPORTANT]
> Accounts can store up to **10MB** of data, which can consist of either _executable program code_ or _program state_.
