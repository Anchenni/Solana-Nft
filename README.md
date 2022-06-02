# Solana-Nft (Description)
In this project, we will create a website to mint Nfts using the Candy machine V2 and Solana network.
# Installation of all the pakages we need.
- Candy machine v2.
- Solana Cli.
- Node js.
- Yarn.
- Git.
- Vs code, or any other code editor.

# How to install Solana Cli 
## MacOS & Linux

Open your favorite Terminal application

Install the Solana release v1.10.19 on your machine by running:
```
 sh -c "$(curl -sSfL https://release.solana.com/v1.10.19/install)"
```
You can replace v1.10.19 with the release tag matching the software version of your desired release, or use one of the three symbolic channel names: stable, beta, or edge.

The following output indicates a successful update:
```
downloading v1.10.19 installer
Configuration: /home/solana/.config/solana/install/config.yml
Active release directory: /home/solana/.local/share/solana/install/active_release
* Release version: v1.10.19
* Release URL: https://github.com/solana-labs/solana/releases/download/v1.10.19/solana-release-x86_64-unknown-linux-gnu.tar.bz2
Update successful
```
Depending on your system, the end of the installer messaging may prompt you to
```
Please update your PATH environment variable to include the solana programs:
```
If you get the above message, copy and paste the recommended command below it to update PATH
Confirm you have the desired version of solana installed by running:
```
solana --version
```
After a successful install, solana-install update may be used to easily update the Solana software to a newer version at any time.

## For Windows 
Got to [Solana cli docs](https://docs.solana.com/cli/install-solana-cli-tools) 

# How to install Nodejs
Go to [Nodejs website](https://nodejs.org/en/)

# How to install Ts-node
Got the [Ts-node website](https://www.npmjs.com/package/ts-node)

In my case i choose to install it as globally with the command bellows:
```
npm install -g ts-node
```
# How to install Yarn
Go to [Yarn website](https://classic.yarnpkg.com/lang/en/docs/install/#mac-stable)

I did the same for Yarn with the command bellows:
```
npm install --global yarn
```
# How to install Git 
Go to the [Git website](url) and follow the instructions.

# Code editor 
I use visualcode as code editor, if you want to use an other code editor , you can choose what ever you need.
Ex: Nodepath...etc
## How to install Visual Studio Code
Go to [Visual Studio Code Website](https://code.visualstudio.com/) 

# How to verify if everything has been installed correctly 

## For Solana cli type this commande:
```
solana --version
```

<img width="457" alt="Screenshot 2022-05-26 at 18 46 06" src="https://user-images.githubusercontent.com/58232633/170535276-5b1981e4-9c69-4da5-af29-1eed6fa77ca3.png">

## For Node js type this commande:
```
node --version
```

<img width="439" alt="Screenshot 2022-05-26 at 18 48 40" src="https://user-images.githubusercontent.com/58232633/170535556-d089fffb-4c4f-443c-a34b-ecf12e48d3f0.png">

## For Ts-node type this commande:
```
ts-node --version
```

<img width="462" alt="Screenshot 2022-05-26 at 18 50 43" src="https://user-images.githubusercontent.com/58232633/170535995-9651a072-1897-4d8c-b8eb-0b020a2eb9c2.png">

## For Yarn type this commande:

```
yarn --version
```

<img width="441" alt="Screenshot 2022-05-26 at 18 52 02" src="https://user-images.githubusercontent.com/58232633/170536585-0e857868-5a53-4e04-8a26-3125dd355c2c.png">

## For Git type this commande:

```
git --version
```

<img width="445" alt="Screenshot 2022-05-26 at 18 57 16" src="https://user-images.githubusercontent.com/58232633/170537260-26450894-a1fa-41f0-9e5b-d9f7351e663a.png">


Ps: If there is any problems above,so you have to fix them, if you have everything in order dan you can start the project.

# How to create a Solana wallet 

## Create a File System Wallet

```
mkdir solana-nft
solana-keygen new --outfile ./keypair.json
```
After click on enter , the programme will ask you passphrase you kan skap that or set up a password.

If verytyhing is ok you will see:

```
Generating a new keypair

For added security, enter a BIP39 passphrase

NOTE! This passphrase improves security of the recovery seed phrase NOT the
keypair file itself, which is stored as insecure plain text

BIP39 Passphrase (empty for none): 

Wrote new keypair to ./keypair.json
==========================================================================
pubkey: G16aCw2b8EQodL6mNxTJMjF35xkH7Dkovg4uDDXFX55T
==========================================================================
Save this seed phrase and your BIP39 passphrase to recover your new keypair:
truth acquire local weapon spot effort busy copy fringe narrow aware goose
```

Save your pubkey

# Download the Metaplex project 

```
git clone https://github.com/metaplex-foundation/metaplex.git

```

## now we gonna install the metaplax package with yarn 

```
yarn install --cwd ~/Solana-project/solana-nft-test/metaplex/js/
```

Now we gonna configure the solana network and the keypair tha json file for solana wallet

```
solana config set --url https://api.devnet.solana.com
```
```
Config File: ~/.config/solana/cli/config.yml
RPC URL: https://api.devnet.solana.com 
WebSocket URL: wss://api.devnet.solana.com/ (computed)
Keypair Path: keypair.json 
Commitment: confirmed 
```
```
solana config set --keypair keypair.json
```
```
Config File: ~/.config/solana/cli/config.yml
RPC URL: https://api.devnet.solana.com 
WebSocket URL: wss://api.devnet.solana.com/ (computed)
Keypair Path: keypair.json 
Commitment: confirmed
```
## To get the balance of your new wallet 

```
address balance
```

## Add 2 solana to the wallet 

```
solana airdrop 2 
```
```
Requesting airdrop of 2 SOL

Signature: 5YxNEqWVAfXjppbFDQhh4XaJEPLaYKkWZ5LwHBxAZeNWpDdi8o1qWwxNvkpKzdEbFNZQ44dYDMeGMJrbj4wznqdG

2 SOL
```
## Now we gonna create a new file config.json
```
touch config.json

```

