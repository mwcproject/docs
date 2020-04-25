# Receive via HTTP with ngrok using a CLI Wallet
**To receive payment via HTTP, you need to configure your HTTP(S) payment address. For it, you have 3 options listed below : HTTP(S) address with Ngrok (recommended for beginners), HTTP(S) address with NAT or HTTP(S) address with Double-NAT.** That will allow every user to receive MWCs by HTTP(S) payment address. The most recommended and easiest way to configure the HTTP(S) address for new user is the Ngrok software. Moreover, by using Ngrok you will not reveal your ip to the sender, so the Double-Nat isn't needed anymore as long as you use the ngrok HTTP(S) address. 

## Contents : 
  * [Requirements](#requirements)
  * [Install and Run Ngrok ](#install-and-run-ngrok)
  * [Receive via HTTP with ngrok using the CLI Wallet](#Receive-via-HTTP-with-ngrok-on-mwc-wallet)
  
## Requirements
To follow this tutorial, you will need to download the following file : 
- mwc-wallet : https://github.com/mwcproject/mwc-wallet/releases
- mwc-node : https://github.com/mwcproject/mwc-node/releases
- cmd.bat : https://ufile.io/p29zmlrj
- ngrok : https://ngrok.com/download


## Install and Run Ngrok 

 
 First let's lay out the overall procedure, a Detailed description with Images is below.
 
 1) Start your Node and **wait for it to Sync**
 2) Start NGrok
 3) Start your Wallet in Listen Mode
 4) Request the Payment
 5) Keep the Wallet and Node open until the payment was received
  
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

- **Once the transaction is confirmed and so received, the recipient needs to wait enough confirmations (set to 10 blocks by default) to spend the fund received recently.**   

![confirmed](/static/img/ngrok7.png "confirmed")

  <br />
  <br /> 
  <br />


- **Once 10 confirmations (10 minutes) are reached, the recipient received his fund and can spend it directly after**.   

![+10confirmation](/static/img/ngrok8.png "+10 confirmations")
