# NeoHackathon_2023
Project Made for Neo APAC Hackathon 2023. 

## Try it out
https://neo-hackathon-2023.vercel.app/

## Inspiration
Government/Private banks provide interest rates which is fixed and is not related to inflation rates of the country. Problem with this approach is that users while earning interest might still suffer loss if the inflation rates become higher than the interest rate that banks provides. For eg, if the interest rate provided by bank is 3% and the inflation rate is 6%, user suffer a loss. We solve this problem using inflation rate data provided by Truflation per day. We give interest to users on daily basis by fetching latest inflation rate automatically every 24hr. Users also have the ability to withdraw automatically on reaching certain profit.
## What it does
Decentralized investing platform where users can deposit their verse tokens(VTEST). Users will get interest every day equal to inflation rate provided by Truflation. Users can also access a graph feature for every deposit which will depict the trend of amount of tokens on daily bases. Users can choose to invest their money in the following 2 ways:
1) Fixed Deposit
user can deposit tokens and can withdraw them only after the maturity period. User can fill maturity period during the deposit
2) Dynamic Deposit
Once user deposits his/her tokens can withdraw them anytime. Additonal feature for dynamic deposit is that user can choose for autmatic withdrawal. Just fill out the token amount and as soon as the token amount reaches tha value, tokens will be automatically credited to the user's metamask wallet. For example: user deposits 50 VTEST and enters withdrawal amount as 60 VTEST. When the amount reaches 60 all of the tokens will be credited to user's wallet. This feature was implemented with the help of chainlink automation tool using time based trigger.<br>
## Flow of the dapp
https://drive.google.com/file/d/1-gNA6WMzFTSMc_l0qn5OiKjlYI_z7ACD/view?usp=sharing


## How we built it
Fronted was built using Reactjs. Smart contracts were written in solidity. Truflation helps us to fetch inflation rate( using Chainlink oracle which is used to provide interest to users per day. Deployed our frontend on stackOS.
## Contracts structure
https://drive.google.com/file/d/1uNl8QjRPZbqmUpUatfjrfTsCDRqOjrLU/view?usp=sharing

verse.sol - VERSE token contract on goerli testnet provided by VERSE team.<br>
mintVerse.sol - Contains some added functionalities on top of verse.sol (0xA3A8F2B4DcCB6c9a9Ff60A205aD8A142B31a5c88)<br>
Truflation.sol - Fetches inflation rate(int) from chainlink oracles. (0x25Cb70c92A1FA078E4A9b918c6Ea51376889a15a)<br>
dVest.sol - Uses mintVerse.sol and Truflation.sol and contains the dapp logic(0xE1A66553e4834caE35eBbFd4cd70Cf7D84f53432). (Deployed on NEO EVM Testnet)


## Challenges we ran into
Integrating stackOS into our dapp as we were completely new to docker so we faced issues while installations. Also, NEO faucet was not working, so we were falling short of GAS tokens for deployment. But the team has been quite helpful for sending us tokens everytime it was needed.
## Accomplishments that we're proud of
We were able to make our dapp running with all the main features. Users can now be saved from daily inflation rate and can protect their money.
## What we learned
Docker basics, how to integrate stackOS and NEO EVM. 
## What's next for dVest
1) Providing loans to users. Adding this feature will make the dapp more reliable.
2) Improving the UI/UX.
3) Giving interest to users based on the countries they live in.
