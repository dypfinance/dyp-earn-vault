# DYP Earn Vault

## DYP Vaults Specification:

1. Support for the following deposit tokens: ETH, WBTC, USDC, USDT, DAI

2. https://compound.finance/developers Compound Integration - users deposited funds are forwarded to compound for respective cTokens held by smart contract.

3. Users may withdraw their cTokens back to their deposit + interest from compound assuming appropriate liquidity conditions. The setup assumes compound and uniswap has the appropriate amount of liquidity available for the whole setup to work properly.

4. 0.3% withdrawal fee in respective token, 25% used to buy back DYP from uniswap and 75% distributed pro-rata among active vault users.

5. ETH fee equivalent to 400k gas at current gwei gas price for deposits and withdraw, 25% used to buy back DYP from uniswap and 75% distributed pro-rata among active vault users.

6. 5 different lockup durations / pools for each deposit token: 3, 30, 60, 90 and 120 days

7. Fixed APY for each pool, in DYP according to uniswap price of DYP from WETH pool. - admin needs to supply the required amount of DYP to the contract, if the contract runs out of DYP, users cannot withdraw their pending DYP rewards.

8. Uniswap Integration to periodically auto-buy DYP using above 25% fees and send to burn address.

9. Additional Claim button for compound rewards.

10. Re-Invest for DYP rewards with constant staking integration.
