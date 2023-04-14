---
title: "Building a NFT Ticketing app with Paper and Next.js"
datePublished: Fri Apr 14 2023 07:41:05 GMT+0000 (Coordinated Universal Time)
cuid: clgg8puo6000009le5t1raf1w
slug: building-a-nft-ticketing-app-with-paper-and-nextjs
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1681325604249/72f6a87c-1c5c-4cdb-b52e-10533d54e1b1.png
tags: programming, web-development, web3

---

NFT ticketing is a new method of selling tickets for various events such as concerts, sports games, and festivals. In this system, tickets are represented as NFTs (non-fungible tokens) which are unique digital assets that cannot be duplicated or exchanged for anything else.

When attendee purchases an NFT ticket, they are essentially acquiring a one-of-a-kind digital asset. These tickets are minted on blockchains such as Ethereum, which makes it simple to track ownership and securely transfer them between ticket holders. This means, attendees no longer have to be concerned about fake tickets or scams.

## Why companies are moving towards NFT ticketing

NFT ticketing is gaining traction among companies due to several significant reasons, including:

* Improved Security: NFT ticketing offers a high level of security and authenticity that traditional paper or digital tickets cannot match. Each NFT is unique and recorded on a blockchain, making it almost impossible to counterfeit or duplicate.
    
* Potential for Increased Revenue: NFTs are digital assets that can be bought, sold, and traded on secondary markets, creating the potential for ticket resales at higher prices.
    
* Enhancing the Fan Experience: NFTs can grant access to exclusive content, such as backstage meet-and-greets or VIP lounges, improving the fan experience. Additionally, fans can hold onto their NFT tickets as collectibles, providing a memorable experience.
    
* Environmental Sustainability: NFT ticketing can reduce environmental impact by eliminating the need for paper tickets, which is becoming increasingly important for environmentally conscious consumers.
    

## What is [Paper](https://withpaper.com/?utm_source=suhail)?

[Paper](https://withpaper.com/?utm_source=suhail) is a developer platform for NFT commerce. It allows you to accept credit card payments for NFTs, enable users to “connect” to your app with just their email, and airdrop NFTs at scale.

In this tutorial, we will be building an NFT ticketing application with [Paper](https://withpaper.com/?utm_source=suhail). You can find the final code of the application **here**.

Here is what the application would look like:

<iframe src="https://lvpr.tv?v=b5e9r2gzxm5yojto" width="100%" height="500" sandbox="allow-scripts"></iframe>

## **Prerequisites**

Before you start with the tutorial make sure you have the latest version of [Node.js](https://nodejs.org/en/) installed on your machine.

## **Setting up Next.js App**

The first step is to set up a next.js app and install the required dependencies. In order to do that, you would need to run the below command in your terminal.

```plaintext
mkdir nft-ticketing && cd nft-ticketing && npx create-next-app .
```

The above command creates a new directory named `nft-ticketing` then navigates to that directory and creates a next.js app.

> While creating the next application, you will be prompted if you would like to use Tailwind, make sure to choose "yes", as we will be using Tailwind in this tutorial as well.

## The Smart Contract

You can write and deploy a smart contract using Solidity or thirdweb. thirdweb is a platform that provides a suite of tools for creators, artists, and developers to easily build, launch and manage a Web3 project.

In this tutorial, we will do both. Using solidity and also thirdweb.

### Using thirdweb

If you prefer to use Solidity, you can safely skip this step. We can use thirdweb to create and deploy an NFT drop. Head over to thirdweb.com and connect your wallet.  
Once connected, you will be navigated to the explore page below.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1681329679043/425d617b-ad32-4998-9137-174a395810cd.png align="center")

Here choose the NFT Drop and click on Deploy

> Make sure you are on the Polygon Mumbai network. If you aren't you can update the network by clicking on the Metamask logo on the top right.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1681329776240/afcea660-58cf-474a-8a55-a4cdfdc5997e.png align="center")

A sidebar will pop up, and you can add information about your NFT, i.e image, name, symbol, description, royalties and many other fields.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1681329853772/469d93a9-cee9-4994-939e-610fe92ba05d.png align="center")

Once you have filled it in, you can scroll down and click on "Deploy". Once the contract has been deployed, you should see it inside your third web dashboard.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1681330063665/fffdd3d4-6e17-4e70-ba47-aab68ccfe36f.png align="center")

Next, navigate to the NFT tab to upload your NFT metadata.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1681330115430/ac0be821-d5cf-47a9-9bad-02653ee634c8.png align="center")

You can either batch update multiple NFT metadata or single upload. In this tutorial, we will be using single upload. Click on the single upload button and a sidebar should pop up. Fill in your NFT metadata and then press 'Lazy Mint NFT

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1681330281305/5e55c9fb-5753-4df8-bf92-da2269a83e68.png align="center")

Finally, navigate to "Claim Conditions" by pressing the second option on the sidebar and create a new phase for your NFT's claim conditions. Here, you can control when the NFTs get dropped, how much they cost, and more.

Once you have added information about your NFT, press "Save Phase". This will trigger a transaction and after completing it, you should be able to see a success message.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1681330432793/1bceebea-2eb8-4852-846d-12700abef996.png align="center")

And that is it! copy your contract address from the dashboard as we will need it later.

### Using Solidity

If you would like to use Solidity to create an NFT drop contract, I would recommend checking out a great tutorial from [QuickNode](https://www.quicknode.com/guides/ethereum-development/nfts/how-to-create-and-deploy-an-erc-721-nft/) that will help you create an ERC721 contract, and deploy it.

### Registering the Contract

If you have deployed your smart contract with thirdweb or manually using Solidity and Remix, you now have the contract address on Polygon Mumbai. The next step is to register the contract on the [Paper](https://withpaper.com/?utm_source=suhail) dashboard.

Start by signing up for [Paper](https://withpaper.com/?utm_source=suhail). Once you have successfully created an account, go to Checkouts, navigate to Contracts, and click on Register Contract. Fill in the required information. If you deployed with thirdweb, choose "thirdweb" under the contract type; otherwise, choose "custom". Finally, click on "Register"."

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1681334591039/c22e49a1-99e4-4ae9-acb3-153008ee6395.png align="center")

Once the contract is registered, copy its ID as we will need it later.

## The Frontend

Now that we have completed the smart contract section, we can move into the front-end. The first step is to set up authentication.

### Authentication

Authentication plays a vital role in web3 applications. There are different authentication SDKs such as WalletConnect, and RainbowKit which allow us to add authentication to our app and handles, connect wallet and sign messages. However, this post will be using [Paper's](https://withpaper.com/?utm_source=suhail) Embedded Wallet Service.

#### [**Paper's**](https://withpaper.com/?utm_source=suhail) **Embedded Wallet**

[Paper's](https://withpaper.com/?utm_source=suhail) embedded wallet service is a simple yet powerful wallet infrastructure that enables apps to create, manage, and control their users' wallets. It is quite different from other wallet services because

* 💬 **Delightfully simple UX:** No passwords, jargon, or downloads.
    
* 🎉 **Recoverable:** Users can always access their wallets on other authenticated devices.
    
* 🔐 **Extensible:** Email login, social login, and bring-your-own auth.
    
* 💸 **Gas-less:** Users do not require any crypto to interact with the blockchain.
    
* 😌 **They are non-custodial:** Private keys cannot be reconstructed by Paper or any developer of Paper without user authentication. The only owner of the wallet is your end user
    

On the [Paper](https://withpaper.com/?utm_source=suhail) dashboard, under Embedded Wallets, press Auth Settings and fill in your app info. Then press save.

Copy the client ID as we'll need it later.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1681332338788/fe2ac30f-0e27-4017-aeff-9fd307b01c45.png align="center")

Next, in your terminal run the following command to install [Paper's](https://withpaper.com/?utm_source=suhail) embedded wallet service JavaScript SDK.

```plaintext
yarn add @paperxyz/embedded-wallet-service-sdk
```

Next, remove everything inside of `pages/index.jsx` and instead add the following code to it.

```javascript
import { PaperEmbeddedWalletSdk } from "@paperxyz/embedded-wallet-service-sdk";
import React, { useEffect, useState } from "react";

export default function Home() {
  const [paper, setPaper] = useState();

  useEffect(() => {
    const paper = new PaperEmbeddedWalletSdk({
      clientId: "YOUR_CLIENT_ID",
      chain: "Mumbai",
    });
    setPaper(paper);
  }, []);

  return (
    <div className="m-10">
      <button
        className="bg-blue-400 text-white p-2 rounded-md "
        onClick={() => paper.auth.loginWithPaperModal()}
      >
        Authenticate
      </button>
    </div>
  );
}
```

In the above snippet, we are importing the [Paper](https://withpaper.com/?utm_source=suhail) SDK, initialize it with our API key and then in the return function, call the `loginWithPaperModal` method on button click.

> Make sure to replace `YOUR_CLIENT_ID`, with your client id that you copied earlier from the [Paper](https://withpaper.com/?utm_source=suhail) Dashboard.

Save the file, navigate to your browser and open your app on localhost (Make sure to start the Next.js development server by running `npm run dev`).

Click on Authenticate button, and you should be able to see a modal from [Paper](https://withpaper.com/?utm_source=suhail) SDK that would allow users to log in to our app. The good part is users can easily signup with their email or 1 account and [Paper](https://withpaper.com/?utm_source=suhail) will automatically create a wallet for them.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1681333257795/0737d895-a804-4b23-bf46-adf7e5e538cd.png align="center")

The SDKs support many methods which won't be covering this tutorial, but you can refer to them [here](https://docs.withpaper.com/reference/embedded-wallet-service-integration).

### **NFT Minting**

Now that we have completed the authentication, we can move to NFT minting part.

First, we need to create a shareable checkout link, to do that add the following function inside of `pages/index.jsx`

```javascript
  const createCheckoutLink = () => {
    const options = {
      method: "POST",
      headers: {
        accept: "application/json",
        "content-type": "application/json",
        Authorization: "Bearer YOUR_API_KEY",
      },
      body: JSON.stringify({
        contractId: "YOUR_CONTRACT_ID",
        title: "Image Dragon is back!",
        description: "The multi-platinum, Grammy-winning band Imagine Dragons...",
        imageUrl: "https://texxandthecity.com/wp-content/uploads/2022/06/unnamed-1.jpg",
        limitPerTransaction: 5,
        redirectAfterPayment: false,
        mintMethod: {
          name: "claimTo",
          args: { _to: "$WALLET", _quantity: "$QUANTITY", _tokenId: 0 },
          payment: { currency: "MATIC", value: "0.001 * $QUANTITY" },
        },
        hideNativeMint: false,
        hidePaperWallet: false,
        hideExternalWallet: false,
        hidePayWithCard: false,
        hidePayWithCrypto: false,
        hidePayWithIdeal: false,
        sendEmailOnTransferSucceeded: true,
        brandDarkMode: false,
        brandButtonShape: "full",
        brandColorScheme: "blue",
      }),
    };

    fetch(
      "https://withpaper.com/api/2022-08-12/shareable-checkout-link",
      options
    )
      .then((response) => response.json())
      .then((response) => {
        const link = JSON.parse(response.data.checkoutUrl);
        openCheckout(response.data.checkoutUrl);
      })
      .catch((err) => console.error(err));
  };

  const openCheckout = (link) =>
    renderPaperCheckoutLink({
      checkoutLinkUrl: `${link}`,
    });
```

In the above code, we use the [Paper](https://withpaper.com/?utm_source=suhail) API to create a checkout link. The `createCheckoutLink` function sends a POST request to the [Paper](https://withpaper.com/?utm_source=suhail) API with parameters such as the contract ID, title, description, image URL, and payment options.

The `openCheckout` function takes the checkout link returned by the API and uses the `renderPaperCheckoutLink` function to display it.

Once the link is created, users can click on it to complete the checkout process.

> Please make sure to replace the contract ID and API key in the code with your own values.

You can also add the following button to call the createCheckoutLink function.

```javascript
 //...     <button className="bg-blue-400 text-white p-2 rounded-md " onClick={() => paper.auth.loginWithPaperModal()}> Authenticate </button>

      <button
        className="bg-red-400 text-white p-2 rounded-md ml-5 "
        onClick={() => createCheckoutLink()}
      >
        Checkout
      </button>
```

Save the file, and click on the Checkout button in your app. This will open a sidebar using the [Paper](https://withpaper.com/?utm_source=suhail) SDK, allowing users to purchase NFT tickets.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1681335780688/04a8fc86-9a4a-4155-995c-d40df3dcac92.png align="center")

Now that you have understood the process of creating an NFT ticketing app, we can update the hero section to an event page, specifically for the Imagine Dragons concert. Replace the following code in the return function of your component

```javascript
  return (
    <div class="relative pt-48 pb-12 bg-black xl:pt-60 sm:pb-16 lg:pb-32 xl:pb-48 2xl:pb-56">
      <div class="absolute inset-0">
        <img
          class="object-cover w-full h-full opacity-40"
          src="https://images.hdqwalls.com/wallpapers/imagine-dragons-2017-ib.jpg"
          alt=""
        />
      </div>
      <div class="relative">
        <div class="px-6 mx-auto sm:px-8 lg:px-12 max-w-7xl">
          <div class="w-full lg:w-2/3 xl:w-1/2">
            <h1 class="font-sans text-base font-normal tracking-tight text-white text-opacity-70">
              Join the thousands of fans who will be singing and dancing along to the music
            </h1>
            <p class="mt-6 tracking-tighter text-white">
              <span class="font-sans font-normal text-7xl">Image Dragon</span>
              <br />
              <span class="font-serif italic font-normal text-8xl">
                is back!
              </span>
            </p>
            <p class="mt-12 font-sans text-base font-normal leading-7 text-white text-opacity-70">
              The multi-platinum, Grammy-winning band Imagine Dragons is known for their high-energy performances, hit songs, and impressive stage presence. From "Radioactive" to "Believer," their music has been topping charts and entertaining fans all around the world.
            </p>
            <div class="flex items-center mt-5 space-x-3 sm:space-x-4">
              <button
                onClick={() => createCheckoutLink()}
                class=" inline-flexitems-center justify-center px-5 py-2 font-sans text-base font-semibold transition-all duration-200 border-2 border-transparent rounded-full sm:leading-8 bg-white sm:text-lg text-black hover:bg-opacity-90"
              >
                Book Tickets
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  );
```

Save the file, and this is how your application should look like:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1681341814673/cb299a45-9473-4dd9-85e6-091cfa75568d.png align="center")

## **What’s Next?**

So, you've made it this far! That's awesome and it tells me that you're enthusiastic about creating Web3 apps. This tutorial was just to help you get started, now I recommend you turn this into a real-world application. Don't be afraid to get creative and have fun with it!

## Conclusion

That's all for this article. I hope you found it useful. If you need any help, feel free to leave a comment or send me a dm on [Twitter](https://twitter.com/SuhailKakar).

Let's connect on [**Twitter**](https://twitter.com/suhailkakar) and [**LinkedIn**](https://linkedin.com/in/suhailkakar/).

👋 Thanks for reading! See you next time.