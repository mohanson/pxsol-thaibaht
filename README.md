# Pxsol Thai Baht

A hand-crafted "Thai Baht" program implemented on Solana, allowing minting and transfer of tokens.

Features provided:

0. The owner of the program has the right to **mint new tokens**.
0. Transfer tokens.

Note: It is not an SPL, but a hand-crafted SPL-like program for teaching purposes.

## Accounts

You can use the following two accounts for testing. Note that this is not a hard requirement, it is just for convenience.

| Name |               Prikey               |                     Pubkey                     |
| ---- | ---------------------------------- | ---------------------------------------------- |
| Ada  | `11111111111111111111111111111112` | `6ASf5EcmmEHTgDJ4X4ZT5vT6iHVJBXPg5AN5YoTCpGWt` |
| Bob  | `11111111111111111111111111111113` | `8pM1DN3RiT8vbom5u1sNryaNT1nyL8CTTW3b5PwWXRBH` |

## Usage

```sh
$ python make.py deploy
# 2025/06/01 16:15:51 main: deploy program pubkey="CkSGpiGxUxoMKgraghA7s8zoxWEFvW8RC4TkMhqYbd8E"

# Mint 21000000 Thai Baht for Ada
$ python make.py mint 21000000

# Show ada's balance
$ python make.py balance 6ASf5EcmmEHTgDJ4X4ZT5vT6iHVJBXPg5AN5YoTCpGWt
# 21000000

# Transfer 100 Thai Baht to Bob
$ python make.py transfer 100 8pM1DN3RiT8vbom5u1sNryaNT1nyL8CTTW3b5PwWXRBH

# Show ada's balance
$ python make.py balance 6ASf5EcmmEHTgDJ4X4ZT5vT6iHVJBXPg5AN5YoTCpGWt
# 20999900
# Show bob's balance
$ python make.py balance 8pM1DN3RiT8vbom5u1sNryaNT1nyL8CTTW3b5PwWXRBH
# 100
```

# License

MIT.
