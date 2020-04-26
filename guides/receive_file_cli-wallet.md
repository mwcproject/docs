# Receive via Files using a CLI Wallet  


## Contents : 
  * [Requirements](#requirements)
  * [Receive via Files using a CLI Wallet](#Receive-via-Files-using-a-CLI-Wallet)
  
## Requirements
To follow this tutorial, you will need the following:
- Up-to-date MWC QT-Wallet Software: https://github.com/mwcproject/mwc-qt-wallet/releases


------

## Receive via Files using a CLI MWC Wallet

 
 First let's lay out the overall procedure, a Detailed description with Images is below.
 
 1) Start your Node and **wait for it to Sync**
 2) Open a Commandline or Shell and navigate to your Wallet's Folder
 3) Receive the Transactionfile and genereate a response 
 4) Upload the response to the Exchange or Sender and wait for him to finalize the transaction

 
  
  <br />
  <br /> 
  
- **Once your Node is running and fully synced you can receive the transactionfile with the following Command:**
 Make sure to replace the path and filename to point to the Transactionfile you want to receive!
	
	  
   #### Linux

	mwc-wallet receive -i $HOME/Downloads/transaction.tx
	<enter password>

 
 #### Windows
 
	mwc-wallet.exe receive -i c:\users\%username%\Downloads\transaction.tx
	<enter password>

  
  <br />
  <br /> 
  <br /> 
  
- **Upload the created Responsefile to your exchange or the Sender and wait for him to finalize the transaction**
  <br />
  <br /> 
  <br /> 

- **To check the current status of the transaction go in the _Transaction_ tab. As we saw before the transaction still have no confirmation yet, you will need at least to wait 2 min to see it as confirmed.**

![unconfirmed](/static/img/gui10.png "Unconfirmed")

  <br />
  <br /> 
  <br />


- **Once the transaction is confirmed and so received, the recipient needs to wait enough confirmations (set to 10 blocks by default) to spend the fund received recently.**   

![confirmed](/static/img/gui11.png "awaiting confirmations")

  <br />
  <br /> 
  <br />


- **Once 10 confirmations (10 minutes) are reached, the recipient received his fund and can spend it directly after**.   

![+10confirmation](/static/img/gui12.png "+10 confirmations")



