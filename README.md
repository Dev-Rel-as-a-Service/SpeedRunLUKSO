# 🏗 SpeedRunLUKSO Challenges

**Learn how to use 🏗 Scaffold-ETH 2 to create decentralized applications on LUKSO. 🚀**

**Learn the new NFT and Token standards (LSP8 + LSP7) and discover the superpowers of Universal Profiles. 🆙**

---

## 🚩 Challenge 0: 🎟 Simple NFT Example using LSP8 on LUKSO

🎫 Create a simple NFT using LSP8 on LUKSO. You'll use 👷‍♀️ HardHat to compile and deploy your first LSP8 smart contract learning the differences between an LSP8 (new NFT standard) and an ERC721 (old standard). Then, you'll use a template React app full of important Ethereum components and hooks. Finally, you'll deploy an NFT to the public LUKSO testnet network to share with friends! 🚀

https://github.com/Dev-Rel-as-a-Service/SpeedRunLUKSO/tree/challenge-0-simple-nft

---

## 🚩 Challenge 1: 🔏 Decentralized Staking App with LYX

🦸 A superpower of Ethereum is allowing you, the builder, to create a simple set of rules that an adversarial group of players can use to work together. In this challenge, you create a decentralized application where users can coordinate a group funding effort. If the users cooperate, the money is collected in a second smart contract. If they defect, the worst that can happen is everyone gets their money back. The users only have to trust the code.

https://github.com/scaffold-eth/se-2-challenges/tree/challenge-1-decentralized-staking

---

## 🚩 Challenge 2: 🏵 Token Vendor

🤖 Smart contracts are kind of like "always on" vending machines that anyone can access. Let's make a decentralized, digital currency. Then, let's build an unstoppable vending machine that will buy and sell the currency. We'll learn about the "approve" pattern for ERC20s and how contract to contract interactions work.

https://github.com/scaffold-eth/se-2-challenges/tree/challenge-2-token-vendor

---

## 🚩 Challenge 3: 🎲 Dice Game

🎰 Randomness is tricky on a public deterministic blockchain. In this challenge you will explore creating random numbers using block hash and how that may be exploitable. Attack the dice game with your own contract by predicting the randomness ahead of time to always roll a winner!

https://github.com/scaffold-eth/se-2-challenges/tree/challenge-3-dice-game

---

## 🎉 Checkpoint: Eligible to submit your own build on speedrunLUKSO.com

A place to show off your builds and meet other builders. Start crafting your Web3 portfolio by submitting your DEX, Multisig or SVG NFT build and shipping them on lukso netowork! 

https://speedrunlukso.com/

---

## 💡 Contributing: Guide and Hints to create New Challenges

- We'd use the [base-challenge-template](https://github.com/scaffold-eth/se-2-challenges/tree/base-challenge-template) as a starting point for each challenge.
- UI wise, we'll try to use the https://speedrunethereum.com/ design vibe.

Check out already migrated Challenges to get a better idea of the structure and how to create new ones.

A quick start guide.

### 1. Branch from [base-challenge-template](https://github.com/scaffold-eth/se-2-challenges/tree/base-challenge-template)

At `base-challenge-template` branch we will be adding the latest updates from Scaffold ETH 2. We'll also include the learnings we acquire during the Challenges we are adding, as well as the code that may be common to all the Challenges.

### 2. Edit `pages/index.tsx`

The main page should have a banner image (ask for it!) + the Challenge description.

> {challengeHeroImage}
>
> A {challengeDescription}.
>
> 🌟 The final deliverable is an app that {challengeDeliverable}.
> Deploy your contracts to a testnet then build and upload your app to a public web server. Submit the url on [SpeedRunLUKSO.com](https://speedrunlukso.com)!

### 3. Implement the Challenge

- Add the contract(s)
- Add pages / components as you need (UI following the [SpeedRunLUKSO.com](https://speedrunlukso.com/) design vibe)
- Create the test for the Smart Contract(s). The best starting point is to copy the tests from the SE1 Challenge you are migrating. The "envvar" logic there is used by the autograder, so don't remove them.

### 4. Adapt Header / MetaHeader component

Update the site title on `Header.tsx` and title and description of your challenge in `MetaHeader.tsx`.

### 5. Image assets for your Challenge

You will need to add the following image assets in `packages/nextjs/public` folder (ask the designers for it):

- **Thumbnail.** `thumbnail.png`
  Will be shown in your link previews when shared to others in chat or in social media.
- **Hero image.** `hero.png`
  It's a wider version of the Thumbnail with SRE logo at the bottom right. Used as README header, and as `pages/index.tsx` hero image.

### 6. Edit README adapting the [base template](https://github.com/scaffold-eth/se-2-challenges/tree/base-challenge-template#readme)

Adapt the base template README using the SE-1 version as a reference.

### 7. Create a PR against the challenge branch

We can iterate and test there.
