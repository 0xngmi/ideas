# Cool Ideas

Very commonly I notice inefficiencies in the market and come up with protocols that would be really cool to build. However I want to stay very focused on defillama and I don't have time to actually build these other ideas.

Because of this, I'm open sourcing all of them so other people can take them and build them.

## Steal them!
I believe ideas should be free, so feel free to steal any ideas from here without having to give anything back, including credit, token allocation or anything else, just take them and do whatever you want.

If you want, feel free to reach out to me if you want advice or help with building any of these (I won't be able to actually do proper work tho).

## Ideas

### Decentralized Bitcoin bridge based on Eigelayer
https://gist.github.com/0xngmi/432f14411dff5adc98580f4d5b9eb439

### Vault for arbing withdrawals on L2 bridges
Optimistic bridges have long withdrawal times so people that want their money instantly have to use bridges like synapse or hop to cross the gap instantly, and because of the way they work this creates some positive slippage if you bridge in.

This leads to an arbitrage opportunity, where you can bridge 1 ETH and get >1 ETH (eg: 1.01 ETH) on a L2. Afterwards you can withdraw that through the standard bridge, getting you >1 ETH back on ethereum.

Right now if you did this you could be getting 10-20% APY on ETH, which is much higher than on other yield aggregators and the risk profile is much lower (you only need to trust the bridge protocol the moment you are bridging, and apart from that only trust point is that L2 will work correctly, which is a very safe assumption).

The opportunity here is to build a protocol that automates this type of arbitrage, so people just deposit money on ethereum and the vault does everything for them. This opportunity is not open to traditional yield aggregators because they all work under the assumption that positions must be liquid.

Probably the hardest thing to build here is some algorithm that maximizes APY by leaving some money resting on L1 (you want to bridge when most people are exiting in order to maximize arbs).

### Vault for PERP basis trades
Simplifying the concept, PERPs work by paying funding from the less popular position to the most popular one. In other words, if most people are longing bitcoin, they are paying those who are shorting, and the bigger is the difference between longs/shorts, the more they pay. This makes it possible to make money by shorting bitcoin.

You may be thinking that this is not great because you need to short bitcoin, which is a bad trade, however you can arb this while maintaining the exposure that you want.

If you have 100 USD, you can buy 50$ worth of BTC and open a 50x short. Then if bitcoin goes up your short will lose value but your BTC will gain the same amount in value, so your net gain/loss will be 0, therefore whatever happens your position is still equivalent to your intial 100$. However, because you are shorting bitcoin, now you are also collecting funding fees, thus earning a good APY on your USD.

This is not simple tho, you need to avoid getting liquidated and if the mark price moves against you and you sell, you'll realize a loss. This means that your money may be locked during some time and that this strategy is not well suited to have deposits/withdraws that are triggered by users (otherwise a user could make you lose money), so it can't be implemented on the vaults of traditional yield aggregators.

### Vtuber setup as a service
I've met many people in the cryptocurrency space that would like to have a vtuber, in order to be able to join calls while staying anon, but don't have the time to set it up.

A bussiness could set up everything for them (artist commission, software setup...) and they'd just pay in exchange.

This makes it very efficient for all parties, atm if you want to get a vtuber you need to learn how they work, search for an artist, learn how to setup the software (and pick it) and get the right hardware. But you only need to do this once, so it scales very well.

One way to sell this would be to just directly ship a computer loaded with everything to their address. That would minimize the time the clients need to spend on setup while also lowering trust assumptions (asking them to run software provided by you on their computers requires a lot of trust since they are likely to be moving a lot of money that could be hacked). You could easily charge >5k/setup, with 2k spent on costs (buying hardware and shipping it) so profit margin would be 3k/sale.

Discussion: https://twitter.com/0xngmi/status/1454713199039758341

### NFT AMM that works like raydium over serum (os instead)
https://twitter.com/0xngmi/status/1448157331422859266

### NFT lending
https://github.com/0xngmi/nft-collateral#lending-pools

### DCA vaults
Might be too late since there are already some very good teams working on this idea

https://github.com/0xngmi/dca

### Very low gas dex
https://twitter.com/0xngmi/status/1443498971649949698

### MEV front-running as a service
https://twitter.com/0xngmi/status/1447003709532213248

### Good counterfactual NFT minting
https://twitter.com/0xngmi/status/1447015858925195268

### Better Protocol-owned-liquidity bonds
https://twitter.com/0xngmi/status/1503023026522238985

### Protocol that optimizes emissions
https://twitter.com/0xngmi/status/1503017784317562885

### Tranched product with personalized risk profiles
WIP

### Vault for Ruler
Revive ruler but build a vault where people can just deposit money and it lends it out

## Research
- Classify all tokens by tags like "veTokenomics", "low float+high fdv", "offers staking"... and then look at their perfomance over time (controling for factors like bull/bear market) to do a data-based analysis of different tokenomics

## How have I been drained?
Users input their address and it tells them how they got drained and what to do as next steps to stay safe.
