# simpletoken-cairo


Ethereum-based standard tokens that can be traded and transferred on the Ethereum network.  EOA wallet has no state and code storage, and the Starknet wallet is different, it's defult smart contract wallet.

we think the token contract should be simpler, more functions are taken care of by the smart contract wallet.

Our proposal is to design a simpler token asset based on the smart contract wallet, 

It aims to achieve the following goals:

1. Keep the token asset contract simple, only need to be responsible for the transaction function
2. approve and allowance functions are not managed by the token contract , approve and allowance should be configured at the user level instead of controlled by the asset contract, increasing the user's more playability , while avoiding part of the SNRC-2 contract risk.
3. Remove the transferForm function, and a better way to call the other party's token assets is to access the other party's own contract instead of directly accessing the token asset contract.
4. Forward compatibility with SNRC-2 means that all fungible tokens can be compatible with this proposal.
