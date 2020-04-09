
# Restore CLI-Wallet from Seedphrase 


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
 * Create recovery directory
 * Copy Node api secret into your recovery Directory
 * Switch into your Recovery Directory
 * Recover Wallet from Seed 
 
 Usually this does the trick, here are the needed Commmands: 
 
 #### Linux
	mkdir recovery 
	cd recovery  
	cp ~/.mwc/main/.api_secret .
	mwc-wallet init -h -r 
	<enter recovery phrase> 
 
 Make sure to always executes commands from this new recovery Directory! All your Wallet Data will be stored here now!
 
 #### Windows
 
	mkdir recovery 
	cd recovery  
	copy C:\Users\%username%\.mwc\main\.api_secret %cd%  
	mwc-wallet.exe init -h -r  
	<enter recovery phrase> 
 
  Make sure to always executes commands from this new recovery Directory! All your Wallet Data will be stored here now!
 
------

 ### Restore and Wipe Chaindata 
 
 * Create a new recovery directory
 * Copy Node api secret into your new recovery Directory
 * Switch into your new Recovery Directory
 * Wipe Chaindata 
 * Recover Wallet from Seed 
 
 
  Here are the needed Commmands: 
 **Make sure your Node is stopped for this**

 #### Linux
	rm -rf ~/.mwc/main/chain_data
	start node and **Wait for it to sync**
	mkdir recovery2
	cd recovery2
	cp ~/.mwc/main/.api_secret .
	mwc-wallet init -h -r
	<enter recovery phrase>

 
  Make sure to always executes commands from this new recovery Directory! All your Wallet Data will be stored here now!
 
 
 #### Windows
 
	rmdir /S /Q C:\Users\%username%\.mwc\main\chain_data
	start node and **Wait for it to sync**
	mkdir recovery2
	cd recovery2
	copy C:\Users\%username%\.mwc\main\.api_secret %cd%
	mwc-wallet.exe init -h -r
	<enter recovery phrase>
 
  Make sure to always executes commands from this new recovery Directory! All your Wallet Data will be stored here now!
 

 
  


