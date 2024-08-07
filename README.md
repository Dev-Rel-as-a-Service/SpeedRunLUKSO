# 🚩 Challenge #0: 🎟 Simple NFT Example using LSP8 on LUKSO

![readme-0](https://github.com/scaffold-eth/se-2-challenges/assets/80153681/375b7797-6839-43cd-abe5-fca94d88e300)

📚 This tutorial is meant for developers that already understand the [ 🖍️ basics ](https://www.youtube.com/watch?v=MlJPjJQZtC8). 

🧑‍🏫 If you would like a more gentle introduction for developers, watch our 15 video [🎥 Web2 to Web3](https://www.youtube.com/playlist?list=PLJz1HruEnenAf80uOfDwBPqaliJkjKg69) series.

📄 If you get get stuck make sure to consult the [LUKSO DOCS](https://docs.lukso.tech/)

---

🎫 Create a simple NFT using LSP8 on LUKSO:

👷‍♀️ You'll compile and deploy your first LSP8 smart contract learning the differences between an LSP8 (new NFT standard) and an ERC721 (old standard). Then, you'll use a template React app full of important Ethereum components and hooks. Finally, you'll deploy an NFT to the public LUKSO testnet network to share with friends! 🚀

🌟 The final deliverable is an app that lets users purchase and transfer NFTs. Deploy your contracts to LUKSO testnet, then build and upload your app to a public web server. Submit the url on [TODO]()!

💬 Meet other builders working on this challenge and get help in the [SpeedRunLUKSO Commonground]()!

🤖 If you have any question during your Challenge, you can try out the [Cookbook.dev ChefGPT](https://www.cookbook.dev/contracts/BurntPunx-BurntPunX), and get answers to your Challenge/Scaffold-ETH questions. Please reach us in Commonground if something feels wrong!

## Checkpoint 0: 📦 Environment 📚

Before you begin, you need to install the following tools:

- [Node (>= v18.17)](https://nodejs.org/en/download/)
- Yarn ([v1](https://classic.yarnpkg.com/en/docs/install/) or [v2+](https://yarnpkg.com/getting-started/install))
- [Git](https://git-scm.com/downloads)

Then download the challenge to your computer and install dependencies by running:

```sh
git clone https://github.com/scaffold-eth/se-2-challenges.git challenge-0-simple-nft
cd challenge-0-simple-nft
git checkout challenge-0-simple-nft
yarn install
```

> in the same terminal, start your local network (a local instance of a blockchain):

```sh
yarn chain
```

> in a second terminal window, 🛰 deploy your contract (locally):

```sh
cd challenge-0-simple-nft
yarn deploy
```

> in a third terminal window, start your 📱 frontend:

```sh
cd challenge-0-simple-nft
yarn start
```

📱 Open [http://localhost:3000](http://localhost:3000) to see the app.

---

## Checkpoint 1: ⛽️ Gas & Wallets 👛

> ⛽️ You'll need to get some funds from the faucet for gas.

![gas&wallet](https://github.com/scaffold-eth/se-2-challenges/assets/80153681/912d0d4b-db34-49d3-bd7d-7ca0ab18eb66)

> 🦊 At first, **don't** connect MetaMask. If you are already connected, click **Disconnect**:

<p>
  <img src="https://github.com/scaffold-eth/se-2-challenges/assets/80153681/2c7a1e40-50ad-4c20-ba3e-a56eff4b892b" width="33%" />
  <img src="https://github.com/scaffold-eth/se-2-challenges/assets/80153681/1bcf9752-e8ae-4db6-a0a6-5dc774abe46c" width="33%" />
</p>

> 🔥 We'll use burner wallets on localhost.

> 👛 Explore how burner wallets work in 🏗 Scaffold-ETH 2 by opening a new incognito window and navigate to http://localhost:3000. You'll notice it has a new wallet address in the top right. Copy the incognito browser's address and send localhost test funds to it from your first browser (using the **Faucet** button in the bottom left):

![icognito&webBrowser](https://github.com/scaffold-eth/se-2-challenges/assets/80153681/fd191447-a31f-4c03-a36f-936bfb70c2a1)

> 👨🏻‍🚒 When you close the incognito window, the account is gone forever. Burner wallets are great for local development but you'll move to more permanent wallets when you interact with public networks.

> 🆙 In fact while burner wallets and 'externally owned accounts' (EOA's) will still work on LUKSO - one of the powerful new primitives that you will learn about are called [Universal Profiles](https://docs.lukso.tech/install-up-browser-extension/). Universal Profiles or 'UP's' are powerful smart contract accounts that support advanced interfaces and features for account abstraction. We will get more familiar with UP's and their benefits and new features later on.

---

## Checkpoint 2: 🖨 Minting

> ✏️ Mint some NFTs! Click the **MINT NFT** button in the `My NFTs` tab.

![image](https://github.com/scaffold-eth/se-2-challenges/assets/80153681/74cf02f2-4c1b-4278-9841-f19f668e0b1e)

👀 You should see your NFTs start to show up:

![image](https://github.com/scaffold-eth/se-2-challenges/assets/80153681/63dabceb-ad42-4c09-8e5d-a0139939e32d)

👛 Open an incognito window and navigate to http://localhost:3000

🎟 Transfer an NFT to the incognito window address using the UI:

![image](https://github.com/scaffold-eth/se-2-challenges/assets/80153681/3b92fb50-d43f-48a8-838c-c45c443b0b71)

👛 Try to mint an NFT from the incognito window.

> Can you mint an NFT with no funds in this address? You might need to grab funds from the faucet to pay for the gas!

🕵🏻‍♂️ Inspect the `Debug Contracts` tab to figure out what address is the owner of YourCollectible?

🔏 You can also check out your smart contract `YourCollectible.sol` in `packages/hardhat/contracts`.

💼 Take a quick look at your deploy script `00_deploy_your_contract.js` in `packages/hardhat/deploy`.

📝 If you want to edit the frontend, navigate to `packages/nextjs/app` and open the specific page you want to modify. For instance: `/myNFTs/page.tsx`. For guidance on [routing](https://nextjs.org/docs/app/building-your-application/routing/defining-routes) and configuring [pages/layouts](https://nextjs.org/docs/app/building-your-application/routing/pages-and-layouts) checkout the Next.js documentation.

---

## Checkpoint 3: 💾 Deploy your contract! 🛰

🛰 Ready to deploy to a public testnet?!?

> Change the defaultNetwork in `packages/hardhat/hardhat.config.ts` to `luksoTestnet`.

![chall-0-hardhat-config](https://github.com/scaffold-eth/se-2-challenges/assets/55535804/f94b47d8-aa51-46eb-9c9e-7536559a5d45)

🔐 Generate a deployer address with `yarn generate`. This creates a unique deployer address and saves the mnemonic locally.

> This local account will deploy your contracts, allowing you to avoid entering a personal private key.

![chall-0-yarn-generate](https://github.com/scaffold-eth/se-2-challenges/assets/2486142/133f5701-e575-4cc2-904f-cdc83ae86d94)

👩‍🚀 Use `yarn account` to view your deployer account balances.

![chall-0-yarn-account](https://github.com/scaffold-eth/se-2-challenges/assets/2486142/c34df8c9-9793-4a76-849b-170fae7fd0f0)

⛽️ You will need to send LYXt to your deployer address with your wallet, or get it from a public faucet for the LUKSO testnet network.

> The LUKSO testnet faucet can be found [here](https://faucet.testnet.lukso.network/). Simply click the button at the bottom of the page to 'tweet' the request for funds and make sure to copy in your deployer address. You will need a twitter/X account to use the faucet.

> ⚔️ Side Quest: Keep a 🧑‍🎤 [punkwallet.io](https://punkwallet.io) on your phone's home screen and keep it loaded with testnet eth. 🧙‍♂️ You'll look like a wizard when you can fund your deployer address from your phone in seconds.

🚀 Deploy your NFT smart contract with `yarn deploy`.

> 💬 Hint: You can set the `defaultNetwork` in `hardhat.config.ts` to `luksoTestnet` **OR** you can `yarn deploy --network sepolia`.

🎉 Congrats! You've just deployed very first contract to LUKSO testnet! There's only one problem... You just deployed an ERC721 contract which is the old NFT standard. LUKSO is a new EVM-layer 1 chain powered by new solidity standards - instead of ERC's they're called LSP's (LUKSO standards Proposals). Continue on in the next section to learn about the new NFT standard LSP8.

---

## Checkpoint 4: 💡 Learn the differences between ERC721 and LSP8! ⚡

#TODO: 
- summarize differences of erc721 and lsp8 
- show how to modify 'YourCollectible.sol' to be an LSP8
- redeploy the final 'YourLSP8Collectible.sol'
- show how to setMetadata.ts for the newly deployed lsp8

---

## Checkpoint 5: 🚢 Ship your frontend! 🚁

> ✏️ Edit your frontend config in `packages/nextjs/scaffold.config.ts` to change the `targetNetwork` to `chains.luksoTestnet` :

![chall-0-scaffold-config](https://github.com/scaffold-eth/se-2-challenges/assets/12072395/ff03bda0-66c6-4907-a9ad-bc8587da8036)

> You should see the correct network in the frontend (http://localhost:3000):

![image](https://github.com/scaffold-eth/se-2-challenges/assets/80153681/50eef1f7-e1a3-4b3b-87e2-59c19362c4ff)

> 🦊 Since we have deployed to a public testnet, you will now need to connect using a wallet you own or use a burner wallet. By default 🔥 `burner wallets` are only available on `hardhat` . You can enable them on every chain by setting `onlyLocalBurnerWallet: false` in your frontend config (`scaffold.config.ts` in `packages/nextjs/`)

![image](https://github.com/scaffold-eth/se-2-challenges/assets/80153681/f582d311-9b57-4503-8143-bac60346ea33)

> 💬 Hint: For faster loading of your transfer page, consider updating the `fromBlock` passed to `useScaffoldEventHistory` in [`packages/nextjs/app/transfers/page.tsx`](https://github.com/scaffold-eth/se-2-challenges/blob/challenge-0-simple-nft/packages/nextjs/app/transfers/page.tsx#L12) to `blocknumber - 10` at which your contract was deployed. Example: `fromBlock: 3750241n` (where `n` represents its a [BigInt](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/BigInt)). To find this blocknumber, search your contract's address on the [LUKSO testnet blockexplorer](https://explorer.execution.testnet.lukso.network/) and find the `Contract Creation` transaction line.

🚀 Deploy your NextJS App

```shell
yarn vercel
```

> Follow the steps to deploy to Vercel. Once you log in (email, github, etc), the default options should work. It'll give you a public URL.

> If you want to redeploy to the same production URL you can run `yarn vercel --prod`. If you omit the `--prod` flag it will deploy it to a preview/test URL.

⚠️ Run the automated testing function to make sure your app passes

```shell
yarn test
```

#### Configuration of Third-Party Services for Production-Grade Apps.

By default, 🏗 Scaffold-ETH 2 provides predefined API keys for popular services such as Alchemy and Etherscan. This allows you to begin developing and testing your applications more easily, avoiding the need to register for these services.  
This is great to complete your **SpeedRunLUKSO**.

For production-grade applications, it's recommended to obtain your own API keys (to prevent rate limiting issues). You can configure these at:

- 🔷`ALCHEMY_API_KEY` variable in `packages/hardhat/.env` and `packages/nextjs/.env.local`. You can create API keys from the [Alchemy dashboard](https://dashboard.alchemy.com/).

- 📃`ETHERSCAN_API_KEY` variable in `packages/hardhat/.env` with your generated API key. You can get your key [here](https://etherscan.io/myapikey).

- 📃`LUKSO-explorer_API_KEY` variable in `packages/hardhat/.env` with your generated API key. You can get your key [here](https://lukso-explorer.eu.auth0.com/u/login?state=hKFo2SB3ZmZsR0hJa2lBbGlLZV9ua3JYU3otamxzMmJIcnBLYqFur3VuaXZlcnNhbC1sb2dpbqN0aWTZIHJiSDlDckVsMlRKQmRiYmE4VkRpU2hqQXdITXMxTDBto2NpZNkgc2lYcUxMMjBWeHdrbnhabnIyMm5KcndIMFZjSVdWWlQ).

> 💬 Hint: It's recommended to store env's for nextjs in Vercel/system env config for live apps and use .env.local for local testing.

---

## Checkpoint 5: 📜 Contract Verification

You can verify your smart contract on LUKSO blockexplorer by running (`yarn verify --network network_name`) :

```shell
yarn verify --network luksoTestnet
```

> It is okay if it says your contract is already verified. Copy the address of YourLSP8Collectable.sol and search it on the LUKSO blockexplorer to find the correct URL you need to submit this challenge.

## Checkpoint 6: 💪 Flex!

👩‍❤️‍👨 Share your public url with a friend and ask them for their address to send them a collectible :)

![gif](https://github.com/scaffold-eth/se-2-challenges/assets/80153681/547612f6-97b9-4eb3-ab6d-9b6d2c0ac769)

## ⚔️ Side Quests

### 🔥 Universal Page

> 🐃 Want to see your new NFTs on a testnet marketplace? Head to [Universal Page testnet]()

> 🎫 Make sure you have minted some NFTs on your Vercel page (in a testnet UP), then connect to Universal Page using that same wallet.

![image](https://github.com/scaffold-eth/se-2-challenges/assets/80153681/c752b365-b801-4a02-ba2e-62e0270b3795)

> You can see your collection of shiny new NFTs on a testnet!

(It can take a while before they show up, but here is an example:) https://testnets.opensea.io/assets/sepolia/0x17ed03686653917efa2194a5252c5f0a4f3dc49c/2

---

> 🏃 Head to your next challenge [here](https://github.com/Dev-Rel-as-a-Service/SpeedRunLUKSO).

> 💬 Problems, questions, comments on the stack? Post them to the [SpeedRunLUKSO developers chat]()
