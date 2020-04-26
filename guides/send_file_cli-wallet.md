# Send via File using the CLI Wallet

## Contents : 
  * [Requirements](#requirements)
  * [Send via File using the CLI Wallet](#send-via-file-using-the-cli-wallet-1)
 
------ 

## Requirements
To follow this tutorial, you will need the following:

- Up-to-date mwc-wallet Software: https://github.com/mwcproject/mwc-wallet/releases
- Up-to-date mwc-node Software: https://github.com/mwcproject/mwc-node/releases

------

## Send via File using the CLI Wallet

 
 First let's lay out the overall procedure, more detailed instructions with screenshots are below:
 
 1) Start your Node and **wait for it to Sync**
 2) Open a Commandline or Shell and navigate to your Wallet's Folder
 3) Create a Transactionfile by typing the send Command
 4) Confirm typing your password
 5) Exchange your Transactionfile with the recipient or Upload it to your Exchange
 6) Download the Anwserfile from your recipient or exchange 
 7) Finalize the transaction by using the finalize command
 8) Confirm Typing your password and wait for the transaction to confirm
 
  
  
- **Start your Node and make sure it is fully snychronised before continuing!**
  
  ![nodesynced](/static/img/nodesynced.png "Node Fully Synced")  
  
  <br />
  <br /> 
  <br /> 
  
- **Open a Commandline or shell in your Walletfolder and use the following command:** 
  
   #### Linux

	mwc-wallet send -m file -d Mytransactionfile.tx %Amount%
	<enter password>
 
 #### Windows
 
	mwc-wallet.exe send -m file -d Mytransactionfile.tx %Amount%
	<enter password>


  Where you will need to Replace %Amount% with the Amount to send.
  Also make sure that the File "Mytransactionfile.tx" doesn't exist yet, choose a new Filename everytime!
  
   ![sendcommandfile](/static/img/sendcommandfile.png "Send Command Example")  
   
   <br />
   <br /> 
   <br /> 
   
- **Once the transaction is confirmed and sent, the recipient needs to wait for enough confirmations (set to 10 blocks by default) to spend the fund received recently.**   
