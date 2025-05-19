# Solana Pump.fun Trader

> [!CAUTION] 
> Do not use your main wallet with this script! Always use a trading wallet with your trading budget. Don't be lazy! Create a wallet for this now!

Solan Pump.fun Trader is a library to execute buy and sell orders for SPL tokens that were created on pump.fun.

## Installation

Just install it with npm or yarn or whatever.

```bash
npm install "@degenfrends/solana-pumpfun-trader"
```

## Configuration & Usage

```typescript
import PumpFunTrader from '@degenfrends/solana-pumpfun-trader';

const pumpFunTrader = new PumpFunTrader();
this.pumpFunTrader.setSolanaRpcUrl('https://yoursolanarpc.com');

await this.pumpFunTrader.buy(
        privateKey: '12123423434234', // your private key
        tokenAddress: 'ejddjsldjsdlks', // the address of the token you want to buy
        amount: 0.5, // amount in solana
        priorityFee: 0, // (optional) you should increase the priority fee when you want to make sure that transactions are always succesfull.
        slippage: 0.25, // (optional) 0.25 equals 25% slippage.
        isSimulation: false // (optional) 
);

await this.pumpFunTrader.sell(
    privateKey: '12123423434234', // your private key
    tokenAddress: 'ejddjsldjsdlks', // the address of the token you want to sell
    tokenBalance: 10000000 // the amounts of token you want to sell, you need to multiply the amount you want to sell by 1000000 since pump.fun tokens have 6 digits,
    priorityFee: 0, // (optional) you should increase the priority fee when you want to make sure that transactions are always succesfull.
    slippage: 0.25, // (optional) 0.25 equals 25% slippage.
    isSimulation: false // (optional) 
);
```

There are functions to build sell and buy transaction instructions too, which you can use to bundle transactions.

If you have any questions or suggestions, Contact me via [Telegram](https://t.me/trust4120)
