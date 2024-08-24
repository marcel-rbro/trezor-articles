# What is a UTXO?

An **Unspent Transaction Output (UTXO)** is a term for the amount of cryptocurrency that is owned by a user as a result of previous transactions and that can be spent in future transactions. The total of all UTXOs owned by a user determines the amount of cryptocurrency they own.

For example, when a user wants to send a Bitcoin transaction, they use their UTXOs as the input of the transaction. The output of the transaction is a UTXO that is now owned by the recipient and, if the amount of Bitcoin in the input UTXOs was more than the transaction amount, a UTXO for the remaining difference owned by the sender. These newly created UTXOs can then be used by both users as inputs for other transactions.

> **How does UTXO compare to real currency?**  
>
> If you want to purchase a meal that costs $18.75, but you only have a $20 note to spend, you will get back $1.25 and a receipt that confirms that.
>
> This receipt, which is equivalent to the UTXO in cryptocurrency, determines the total amount you have left to spend after the transaction. When you add up all your UTXOs and calculate the total amount of "change" you have received, this determines the total cash balance you own.
>
> In a way, we can think of each UTXO like a bitcoin note/bill, but it is not limited by denomination. You can own a UTXO for any amount of Bitcoin.
>
> If you have $30 in cash, you will have more than one note as there is no such thing as a $30 note. You can have any combination of notes that total to $30. UTXOs work in a similar way. When you see the total balance of your account, you have UTXOs for different amounts that make up the total balance of your account.
>
> So, if we go to purchase a a new Trezor for $67, you most likely do not have a UTXO for exactly $67. Therefore, you will need to spend a combination of UTXOs because it is not possible to split the UTXOs. If you spend $80 worth of UTXOs, you will get a new UTXO of $13 back as "change" and Trezor will receive a new UTXO of $67 that is added to their total balance.

## Why do UTXOs matter?

UTXOs protected by your Trezor hardware wallet are very important. When paying someone using your Trezor, you have the ability to control which "coins" (individual UTXOs) are you going to use, and if you require "change".

If you’ve spent Bitcoin from your Trezor wallet before and are wondering why you’ve never had to manually select UTXOs, this is because Trezor Suite makes things as simple and user-friendly as possible: the UTXO selection process is automated in order to simplify the transaction process.

The fees paid for each transaction are determined not only by the amount of cryptocurrency that is being sent, but also by the amount of UTXOs. Trezor Suite automatically selects UTXOs to best match the amount of each transaction.

[Coin control](https://trezor.io/learn/a/coin-control-in-trezor-suite) is an advanced feature that allows you to choose which UTXOs you want to spend in a transaction. If used properly, it can improve privacy, though we only recommend that you use it once you are familiar with the principles. You can learn more about coin control in the following video:

[![Coin control video](https://img.youtube.com/vi/WrLjLhHvwhM/0.jpg)](https://www.youtube.com/watch?v=WrLjLhHvwhM)


Manually selecting the UTXOs you use for each transaction can make a difference in two main ways:  

- **Privacy**: The UTXOs you select can determine the information you share with others (e.g., the recipient) about your wallet’s balance and transaction history.
- **Transaction fees**: The number of UTXOs you select can also affect the amount you’ll pay in transaction fees, as mentioned before.