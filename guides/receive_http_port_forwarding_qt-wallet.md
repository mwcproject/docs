# Receive via HTTP with a forwarded Port using a QT Wallet  
**To receive payment via HTTP, you need to configure your HTTP(S) Listener to listen first**


## Contents : 
  * [Requirements](#requirements)
  * [Receive via HTTP with Port Forwarding on GUI MWC Wallet](#Receive-via-HTTP-with-Port-Forwarding-on-GUI-MWC-Wallet)
  
## Requirements
To follow this tutorial, you will need the following:
- Up-to-date MWC QT-Wallet Software: https://github.com/mwcproject/mwc-qt-wallet/releases
- A Forwarded port on your Router forwarding Port 3415 to your local PC (See https://www.noip.com/support/knowledgebase/general-port-forwarding-guide/)


------

## Receive via HTTP with Port Forwarding on GUI MWC Wallet

 
 First let's lay out the overall procedure, more detailed instructions with screenshots are below:
 
 1) Enable the HTTP Listener
 2) Request the Payment
 3) Keep the Wallet open until the payment was received
 
  
  <br />
  <br /> 
  
  - By default, the HTTP listener is disabled, as you can see below.
  
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
  
  - A tab named _**FOREIGN API LISTENER**_ open, tick the case of _**Activate Foreign REST API listener**_, to enable the HTTP listener. 
  - Make sure to edit the _**Listening Address**_ to `0.0.0.0:3415`, then you can click on _**Apply**_.


  ![enable](/static/img/apilistenerconfig.png "FOREIGN API LISTENER")  
  
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

- Now you can  note down your Routers IP address to get your withdrawal address : 

Visit http://myip.is and note down your IP address displayed on the Webpage, an example is provided Below



![RouterAddress](/static/img/myipis1.png "Myip.is Router IP Address")

  <br />
  <br /> 
  <br />


- Once you have the http listener on the MWC wallet and know your external IP, you can make your withdrawal with the Router IP Address that you just looked up. An example is below

Make sure to have the MWC wallet open and running. An Example Address would be  : http://84.12.123.7:3415
   


  <br />
  <br /> 
  <br />


- Once the payement is sent, you will have a pop-up confirming that you received a payement, but at this step **the transaction still ```UNCONFIRMED``` and it's in ```AWAITING CONFIRMATION``` as you can see below :**

![popupreceived](/static/img/gui9.png "Received transaction")


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



