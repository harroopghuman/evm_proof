
Overview
In this project smart contract operates as a decentralized token management system with capabilities of token creation (minting) and removal (burning). It features public variables for token specifics, a mapping structure to monitor token balances, and methods to adjust token circulation.

Contract Features
Token Name: Meta
Token Abbreviation: mta
Total Supply: 0 (initial state)
Functionalities
1. Mint Function
The mint function augments the aggregate token supply and enhances the balance of a designated address.

function mint(address addr, uint val) public {
    totsupply += val;
    balances[addr] += val;
}
Parameters:
addr: Address for token issuance.
val: Quantity of tokens to mint.
2. Burn Function
The burn function diminishes the total token supply and reduces the balance of a specific address, contingent upon adequate token holdings.

function burn(address addr, uint val) public {
    if (balances[addr] >= val) {
        totsupply -= val;
        balances[addr] -= val;
    }
}
Parameters:
addr: Address from which tokens are eradicated.
val: Quantity of tokens to burn.
Additional Details
Both mint and burn operations modify the overall token supply and address balances as appropriate.
The burn operation integrates a conditional check to confirm the address possesses sufficient tokens for removal.
