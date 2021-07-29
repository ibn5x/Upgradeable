# Upgradable
An implementation of an upgradable smart contract.  

One of the fundamental properties of blockchain technology is it’s immutability. There are strong arguments against any form of diluting a so-called decentralized applications immutability, but the facts remain that when there is such a high cost of failure one must plan for it. When you implement a path to upgrade your DApp you lose a degree of its inherent Decentralization, while you gain a way to fix any security threats, bugs, and or add additional functionality to your “Decentralized Application” without sacrificing your DApps data. Your DApps users can also continue interacting with the same contract address they are used to with no further actions taken by the user. To achieve this upgradability while maintaining our accumulated data, and user convenience, we modularize our smart contract code into different components. Our “Functional Contract” Will hold all our DApps functions, our “Proxy Contract” will contain the address of our functional contract, as well as store all of the DApps data, and our “Storage Contract” will contain the data structure that both proxy and functional contract will inherit. This inheritence is important to ensure that no data is overwritten and guarantees each contract knows about the variables and data structure of the other. Now in the event that functionality needs to be changed we can simply deploy a new “functional contract” with all of our DApps “upgrades/fixes” and give that contracts address to our proxy contract which will send and return all user requests to the new contracts location. Effectively performing an upgrade. In this way we are able to evolve our Dapp over time, respond to security threats, and maintain ease of use for users as well as retain all of the DApps data.