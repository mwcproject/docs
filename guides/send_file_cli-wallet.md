# Send via File using the CLI Wallet

## Contents : 
  * [Requirements](#requirements)
  * [Send via File using the CLI Wallet](#send-via-file-using-the-cli-wallet-1)
 
------ 

## Requirements
To follow this tutorial, you will need the following:

- Up-to-date mwc-wallet Software: https://github.com/mwcproject/mwc-wallet/releases
- Up-to-date mwc-node Software: https://github.com/mwcproject/mwc-node/releases
- An active Internet Connection

------

## Send via File using the CLI Wallet

 
 First let's lay out the overall procedure, a Detailed description with Images is below.
 
 1) Start your Node and **wait for it to Sync**
 2) Open a Commandline or Shell and navigate to your Wallet's Folder
 3) Create a Transactionfile by typing the send Command
 4) Confirm typing your password
 6*) If you have registered HODL Coins you will see a Dialog to doublecheck the Outputs that are spent.   <br /> 
 If you want to spend those Outputs confirm clicking 
 8) Exchange your Transactionfile with the recipient or Upload it to your Exchange
 9) Download the Anwserfile from your recipient or exchange 
 10) Finalize the transaction by using the finalize command
 11) Confirm Typing your password and wait for the transaction to confirm
 
  
  
  - **Start your Node and make sure it is fully snychronised before continuing!**
  
  ![nodesynced](/static/img/nodesynced.png "Node Fully Synced")  
  
  <br />
  <br /> 
  <br /> 
  
  - Open a Commandline or shell in your Walletfolder and use the following command: 
  
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
   
- **Once the transaction is confirmed and sent, the recipient needs to wait enough confirmations (set to 10 blocks by default) to spend the fund received recently.**   

![confirmed](/static/img/ngrok7.png "confirmed")

  <br />
  <br /> 
  <br />


- **Once 10 confirmations (10 minutes) are reached, the recipient received his fund and can spend it directly after**.   

![+10confirmation](/static/img/ngrok8.png "+10 confirmations")
