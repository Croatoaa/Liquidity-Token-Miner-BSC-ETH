Liquidity-Token-Miner Getting Started
Follow the steps in README.md! 
download, configure, and deploy the Liquidity-Token-Miner smart contract and setup DAPP.



//Getting started and Smart Contract Deployment

1. Download the Zip File
Click on the 'Code' button on the main page of this GitHub repository and select 'Download ZIP'.

2. Extract the Zip File
Extract the contents of the downloaded file to your preferred directory.

3. Edit the Smart Contract
Navigate to the LpMinerCA.sol Solidity file within the extracted folder.
Open this file in your favorite code editor or an IDE that supports Solidity (e.g., Remix IDE).

4. Set the Token Address
Use CTRL+F to search for "0x" within the contract to locate the token address setting.
Replace the current address with the Pancake LP token address or contract address of the token you wish to mine.

5. Configure the Developer Fee Address
Search for "constructor" to find where to set the address to receive the developer fee.
ceoAddress is automatically set as the deployer (ceoAddress = msg.sender;), but you can specify another address for ceoAddress2 to split the fee between two addresses.

6. Set the Developer Fee Percentage
Search for "function devFee" to locate the developer fee function.
Adjust the fee percentage as desired, guided by notes within the contract.

7. Compile the Contract
Make sure to use Solidity compiler version 0.4.26 to compile the contract.

8. Deploy the Contract
Open your chosen Solidity IDE (like Remix).
Set the IDE to use the 'Injected Web3' environment, which will use your MetaMask or similar wallet as the provider.
Select the LpMinerCA contract and click 'Deploy'.

9. Seed Market
Take your newly create contract address and head over to bscscan.com.
Verify the contract.
Once verified you will be able to see the functions on bscscan you must use the seedmarket fuction in order to start the contract.
You can use any amount to seedmarket.
In some cases you may need to trigger an approve tranaction before seeding market if this is the case this can be done by the deployer using the dapps appove function that we are creating in the next steps.



//Configuring the Dapp to match the Smart Contract

1. Open the Liquidity-Token-Miner folder that was extracted earlier using your favorite code editor (I use visual studio code for this).
open the "js" folder and click on "interface.js"
At the top of this file you can set the Address of the Contract "(var minersAddr = 'MINER_CONTRACT_ADDRESS';)" and the Address of the Token being staked/mined "(var tokenAddr = 'TOKEN_CONTRACT_ADDRESS';)"
I strongly suggest not changing anything else here unless you know what you are doing as it is very likely to break if anything else is changed.

3. Edit the index.html to fit your project
Change name of the site, links and details as fits your project.

4. Change images to suit your project
Change images within the "images" folder to suit the needs of your project
Ensure image sizes and names match what is in place right now or to change the names within the code if you know how.

5. Local host or however you would like to host the dapp
I use Python to local host while making changes to the sites index.html. 
With Python installed on your pc you can simply open CMD and CD to "Liquidity-Token-Miner" folder use this command "python -m https.server 8000" to local host while making changes to the code.
From this point you can now interact with the smart contract using the website via local host or upload to your hosting provider.


If you need help with anything dont hesitate to contact me on telegram
Telegram Contact:
@BlockNessMonster