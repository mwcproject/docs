# Send via File using the CLI Wallet

## Contents : 
  * [Requirements](#requirements)
  * [Send via File using the CLI Wallet](#Send-via-File-using-the-CLI-Wallet)
 
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
  Also make sure that %TransactionFilename% doesn't exist yet, choose a new Filename everytime!
  
   ![sendcommandfile](/static/img/sendcommandfile.png "Send Command Example")  
   
   <br />
   <br /> 
   <br /> 
   

- **To check the current statue of the transaction go in the _Transaction_ tab. As we saw before the transaction still have no confirmation yet, you will need at least to wait 2 min to see it as confirmed.**

![unconfirmed](/static/img/gui10.png "Unconfirmed")

  <br />
  <br /> 
  <br />


- **Once the transaction is confirmed and sent, the recipient needs to wait for enough confirmations (set to 10 blocks by default) to spend the fund received recently.**   

![confirmed](/static/img/gui11.png "awaiting confirmations")

  <br />
  <br /> 
  <br />


- **Once 10 confirmations (10 minutes) are reached, the recipient received his fund and can spend it directly after**.   

![+10confirmation](/static/img/gui12.png "+10 confirmations")



 
  
  
  
  

  
  
  
  
  
  
- **Download [Ngrok](https://ngrok.com/download) with no account on all plateforms** with the link below :  

  > In our example, we'll take Ngrok on windows.  

        https://ngrok.com/download
  <br />

  ![ngrokdls](/static/img/ngrokdl.png "Ngrok Download Page")    

<br />
<br />
<br />

- **Extract the zip file, and double-click on _ngrok.exe_.**  
  
  ![extractlauchngrok](/static/img/ngrokextracted.png "Double-Click on ngrok.exe")  


<br />
<br />

  

- **Then click on ```run``` to launch Ngrok.**    
  
  ![warnlaunchngrok](/static/img/ngrokrun.png "Click on Run")  


<br />
<br />


- **Ngrok have been welly launched as we can see below.**

  ![clingrok](/static/img/ngrokstart.png "The ngrok Terminal ")  

<br />
<br />


- **Type ```ngrok http 3415``` in the ngrok console to expose your local web server and so receive MWC via HTTP(S) payment with your Ngrok address.**   
  - On Windows 7-10 :

        ngrok http 3415  

  - On Mac OSX & Linux : 

        ./ngrok http 3415  

  ![ngrok](/static/img/ngrok3415.png "Type ngrok http 3415")  

<br />
<br />

  - **Now, you are online and as we can see: the link expire in 7 hours and 59 minutes. The arrow points your HTTPS address which is needed to withdraw (typical ngrok address for your withdrawal : ```https://xxxxxx.ngrok.io```), HTTP & HTTP(S) ngrok address are usable to receive MWC. By the way, we highly recommend every user to use the HTTPS link.**   

    _In the example below, Ngrok HTTP(S) payment address are :_   
    ```Ngrok HTTP address : http://f7e57b8c.ngrok.io```  
    ```Ngrok HTTPS address : https://f7e57b8c.ngrok.io```

    > **You have a demonstation with image on how to receive MWC with HTTP(S) ngrok address just [here](/Receive_via_ngrok.md#receive-via-http-with-ngrok) !**    

  ![startlisten](/static/img/ngrokpanel.png "Panel of your https link which is expire in 8 hours")

<br />
<br />

------

## Receive via HTTP with ngrok on mwc-wallet

  > _Your Ngrok link expires after being online 8 hours in a row. You will need to close and launch back the Ngrok sotware to have a new session and as well a new usable link. By the way, make sure to type ```ngrok http 3415``` in the Ngrok terminal to enable the HTTP(S) port 3415 tunnel. Moreover, you need to let the Ngrok Terminal open to be online when you receive your MWC withdrawal. To close Ngrok, you just need to close the Terminal manually or type ```CTRL + C``` . Make sure that QT Wallet recipient wallet is listening and the Ngrok HTTP(S) tunnel port is online and running !_   
  
  - Extract `mwc.exe` and `mwc-wallet.exe`.
  
  ![extract](/static/img/ngrok1.png "Extract `mwc.exe` and `mwc-wallet.exe`")  
  
  <br />
  <br /> 
  <br /> 
  
  - Create a folder named `mwc_base` and move the file named `mwc.exe`,`mwc-wallet.exe`,`ngrok.exe` and `cmd.bat` into the new folder created.
  
   ![mwc_base](/static/img/ngrok2.png "folder `mwc_base`")  
   
   <br />
   <br /> 
   <br /> 
   
  - Double click on `mwc.exe`to start the node.
  > Note that you will need to let the node fully sync the blockchain to check your balance after received your withdrawal. Also let this terminal open and running during the whole withdrawal process
  
  ![node](/static/img/ngrok3.png "run the node")
  
  <br />
  <br /> 
  <br /> 
  
  - Double click on `ngrok.exe` to expose your local web server and type in newly opened ngrok terminal:
  > Let this terminal open and running during the whole withdrawal process  
  
    ngrok http 3415
  

  ![ngrok](/static/img/ngrok4.png "run ngrok")  
  
  <br />
  <br /> 
  <br /> 

  - Double click on the `cmd.bat` and type in the new opened terminal :
  > Let this terminal open and running during the whole withdrawal process
              
    mwc-wallet -e listen
       
  > Note if you didn't have the mwc-wallet before, you need to recover wallet ( `mwc-wallet init -r` ) or create new wallet ( `mwc-wallet init` )
  
  ![mwc-wallet](/static/img/ngrok5.png "run mwc-wallet")  
  
  <br />
  <br /> 
  <br /> 

  - Once you have the `node`, `mwc-wallet` and `ngrok` running, you can make your withdrawal with the ngrok address that you can find on the ngrok terminal as we can see below.
  > Note that a typical ngrok address for withdrawal is : `https://xxxxxx.ngrok.io`
  
   ![withdrawal](/static/img/ngrokaddress.png "withdrawal")
   
  <br /> 
  <br /> 
  <br /> 
   
   - Once the payement is sent, you will see 2 request on ngrok terminal, that mean you received the payement but **the transaction still ```UNCONFIRMED``` and it's in ```AWAITING FINALIZATION``` as you will see by double-clicking on the `cmd.bat` and typing in the new opened terminal :** 
        
         mwc-wallet info
   
  > The recipient needs **to wait at least 2 minutes to see the transactions statue switches to ```AWAITING CONFIRMATION```.**
  
  ![unconfirmed](/static/img/ngrok6.png "unconfirmed")
  
  <br />
  <br /> 
  <br />

- **Once the transaction is confirmed and sent, the recipient needs to wait for enough confirmations (set to 10 blocks by default) to spend the fund received recently.**   

![confirmed](/static/img/ngrok7.png "confirmed")

  <br />
  <br /> 
  <br />


- **Once 10 confirmations (10 minutes) are reached, the recipient received his fund and can spend it directly after**.   

![+10confirmation](/static/img/ngrok8.png "+10 confirmations")
