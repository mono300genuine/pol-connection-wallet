
# PolconnectKit

PolconnectKit - Your Seamless Polkadot Wallet Connector 👩🏻‍💻


| ![Static Badge](https://img.shields.io/badge/polkadot-blue) | ![Static Badge](https://img.shields.io/badge/substrate-red) | ![Static Badge](https://img.shields.io/badge/typescript-fuchsia) | ![Static Badge](https://img.shields.io/badge/npm-red) |
| --- | --- | --- | --- |





- 🔥 Out-of-the-box wallet management
- ✅ Easily customizable
- 💪🏼Built on top of polkadot api
- 👌🏻 Cross Chain Support
- 🦄 Supports All wallets


## Motivition


In the Polkadot ecosystem, you can utilize the web3Enable function to access all injected extensions in a user's browser and the web3Accounts() method to retrieve user addresses. 

While this approach may seem functional, it comes with its own set of challenges. Imagine a scenario where a user has multiple Polkadot-wallets extensions installed in their browser. When web3Enable() is initialized, all these installed wallets pop up, significantly disrupting the user interface and leading to a less-than-optimal user experience.

Take a look at the image below, 


![polkadot Image](https://i.ibb.co/MnZT9bQ/photo-2023-10-09-12-25-29.jpg)


Not only does this lead to a compromised user experience, but it also places a burden on developers who need to write extensive code to manage these wallet interactions.

Polconnect, your solution to these challenges. With Polconnect, all it takes is a single line of code. Users can easily select their preferred wallets, manage chains, and seamlessly connect to retrieve user addresses,



## Installation

Install  with npm
```bash
  npm install polconnect @polkadot/api
```
 or Install  with yarn
```bash
  yarn add  polconnect @polkadot/api
```
    
## Usage/Examples

```javascript
// nextjs example

// Wrap your entire application in PolkitProvider  the  provider  takes 3  props

// them :  dark or light theme
// defaultChain : the default chain you want conect to   you can get supported  chans from polconnect
// appName : the name of your  application

 
// import  PolkitProvider and astar network from polconnect
import {PolkitProvider, astar} from 'polconnect'

function App({ Component, pageProps }: AppProps) {
  return(
      <PolkitProvider theme='dark' defaultChain={astar} appName='testing'>
       <Component {...pageProps} />
</PolkitProvider>     
  ) 
}

// Import ConnectButton from 'polconnect'

import {ConnectButton} from 'polconnect'

export default function Home() {
  //  Use  ConnectButton in your component   it  takes 3 props 
   // label: this  is the label of your button
   // showChain : it takes boolean value   if you want to display the switch chain button  add a true value  otherwise add false
   // backaground : this s the background of  the connectButtton
  return(
<ConnectButton label='connect wallet' showChain={true} backGround='blue'   />
 )
}
```

## Documentation

Learn more, from this technical tutorial.  [tutorial](https://abdulkabugu.hashnode.dev/how-to-achieve-seamless-wallet-integration-in-your-polkadot-dapps-with-polconnect)






