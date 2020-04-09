
# Restore QT-Wallet from Seedphrase 


## Contents : 
  * [Preamble](#preamble)
  * [Restore and keep Chaindata](#Restore-and-keep-Chaindata)
  * [Restore and wipe Chaindata](#Restore-and-wipe-Chaindata)
	
## Preamble
Some errors might require you to restore your Wallet from Seedphrase.
If you have a transaction Error and can't seem to resolve it, restoring from Seed is the way to go!

First, try to keep Chaindata intact to preserve your transactionhistory.
If the Error persists, Go for the second Option and Wipe Chaindata too!

Let's lay out the overall procedure, the needed Commands are below!
 
 ### Restore and keep Chaindata 
 
 * [Create a new Wallet Instance](create_Instance_qt-wallet.md)
 * Make sure to restore an existing Seed instead of creating a new one
 
 Here is a short GIF Illustrating the process:  <br />
![restore_seed_qt](/static/img/restore_seed_qt-wallet.gif "restore_seed_qt")
 
 Usually this does the trick, in Case the Error persists try to wipe Chaindata as shown below.
 
 
------

 ### Restore and Wipe Chaindata 
  
   **Make sure your QT Wallet is stopped for this**
   
 * Delete the Chaindata Directory (Folders/Commands listed below)
 * [Create a new Wallet Instance](create_Instance_qt-wallet.md)
 * Make sure to restore an existing Seed instead of creating a new one
 

 **How to remove the Chaindata Folder:** 
 
 #### Linux

 `rm -rf ~/.mwc/main/chain_data`

 #### Windows
 
 `rmdir /S /Q C:\Users\%username%\.mwc\main\chain_data`

 Make sure your Node is Synced completely before further actions you can see this by a green Circle in the bottom right "Mainnet" Button.
 
 
 


