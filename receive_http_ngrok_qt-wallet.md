
# Receive via HTTP with ngrok
**To receive payment via HTTP, you need to configure your HTTP(S) payment address. For it, you have 3 options listed below : HTTP(S) address with Ngrok (recommended for beginners), HTTP(S) address with NAT or HTTP(S) address with Double-NAT.** That will allow every user to receive MWCs by HTTP(S) payment address. The most recommended and easiest way to configure the HTTP(S) address for new user is the Ngrok software. Moreover, by using Ngrok you will not reveal your ip to the sender, so the Double-Nat isn't needed anymore as long as you use the ngrok HTTP(S) address.  


## Contents : 
  * [Requirements](#requirements)
  * [Install and Run Ngrok ](#install-and-run-ngrok )
  * [Receive via HTTP with ngrok on GUI MWC Wallet](#receive-via-http-with-port-forwarding-on-gui-mwc-wallet)
  
## Requirements
To follow this tutorial, you will need to download the following file : 
- GUI MWC Wallet : https://github.com/mwcproject/mwc-qt-wallet/releases
- ngrok : https://ngrok.com/download


## Install and Run Ngrok 

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

## Receive via HTTP with ngrok on GUI MWC Wallet

  > _Your Ngrok link expires after being online 8 hours in a row. You will need to close and launch back the Ngrok sotware to have a new session and as well a new usable link. By the way, make sure to type ```ngrok http 3415``` in the Ngrok terminal to enable the HTTP(S) port 3415 tunnel. Moreover, you need to let the Ngrok Terminal open to be online when you receive your MWC withdrawal. To close Ngrok, you just need to close the Terminal manually or type ```CTRL + C``` . Make sure that QT Wallet recipient wallet is listening and the Ngrok HTTP(S) tunnel port is online and running !_   

  <br />
  <br /> 
  
  - By default, the HTTP listener is disable, as you can see below.
  
  ![httpdisable](/static/img/gui1.png "HTTP listener offline")  
  
  <br />
  <br /> 
  <br /> 
  
  - To enable the HTTP listener, click on the on the gear up, then click on `mwc mq` to go in the settings of the different methods of payement.
  
   ![settings](/static/img/gui2.png "go in the setting the different methods of payement")  
   
   <br />
   <br /> 
   <br /> 
   
  - Then click on _**Configure**_ to set-up the HTTP listener as we can see below.
  
  ![configure](/static/img/gui3.png "Configure HTTP listener")
  
  <br />
  <br /> 
  <br /> 
  
  - A tab named _**FOREIGN API LISTENER**_ open, tick the case of _**Activate Foreign REST API listener**_, to enable the HTTP listener. Also edit the _**Listening Address**_ to `127.0.0.1:3415`, then you can click on _**Apply**_.
  
  > Note that if you use the ip:port address instead of ngrok address, you will need to let this as `0.0.0.0:3415`

  ![enable](/static/img/gui4.png "FOREIGN API LISTENER")  
  
  <br />
  <br /> 
  <br /> 

  - A warning pop-up, click on _**Continue**_ then the wallet will restart.
    
  ![warning](/static/img/gui5.png "Warning pop-up")  
  
  <br />
  <br /> 
  <br /> 

  - As we can see below, the HTTP listener is now _**Online**_.
  
   ![withdrawal](/static/img/gui6.png "withdrawal")
   
  <br /> 
  <br /> 
  <br /> 

- Now you can run ngrok to expose your local web server and type in newly opened ngrok terminal : 

  - On Windows 7-10 :

        ngrok http 3415  

  - On Mac OSX & Linux : 

        ./ngrok http 3415  

![runngrok](/static/img/gui7.png "run ngrok")

  <br />
  <br /> 
  <br />


- Once you have the http listener on the MWC wallet and ngrok running, you can make your withdrawal with the ngrok address that you can find on the ngrok terminal as we can see below.

   > Make sure to have the MWC wallet and ngrok open and running. Note that a typical ngrok address for withdrawal is : https://xxxxxx.ngrok.io
   

![request](/static/img/gui8.png "ngrok address for withdrawal")

  <br />
  <br /> 
  <br />


- Once the payement is sent, you will have a pop-up confirming that you received a payement, but at this step **the transaction still ```UNCONFIRMED``` and it's in ```AWAITING CONFIRMATION``` as you can see below :**

![popupreceived](/static/img/gui9.png "Received transaction")


  <br />
  <br /> 
  <br />


- **To check the current statue of the transaction go in the _Transaction_ tab. As we saw before the transaction still have no confirmation yet, you will need at least to wait 2 min to see it as confirmed.**

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



