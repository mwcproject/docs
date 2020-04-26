# Receive via Files using a QT Wallet  


## Contents : 
  * [Requirements](#requirements)
  * [Receive via Files using a QT Wallet](#receive-via-files-using-a-gui-mwc-wallet)
  
## Requirements
To follow this tutorial, you will need the following:
- Up-to-date MWC QT-Wallet Software: https://github.com/mwcproject/mwc-qt-wallet/releases


------

## Receive via Files using a GUI MWC Wallet

 
 First let's lay out the overall procedure, a Detailed description with Images is below.
 
 1) Receive the Transactionfile and generate a respone
 2) Upload the Response to the Exchange or Sender
 3) Wait for the Transaction to confirm
 
  
  <br />
  <br /> 
  
  - If you received a Transactionfile simply click on the "Receive MWC by File" Button in the "receive" Tab of the Wallet
  
  ![receivefileqt](/static/img/receivefileqt.png "Receive Transaction File")  
  
  <br />
  <br /> 
  <br /> 
  
  - Click on "Generate Response" and confirm by typing your password
 
  
   ![generateresponse](/static/img/generateresponse1.png "Generate Response")  
   
   <br />
   <br /> 
   <br /> 
   
  - Note down the Location of the anwserfile and Upload it to the exchange or Sender.
  
  ![generateredsponse](/static/img/generateresponse2.png "Generate Response")
  
  <br />
  <br /> 
  <br /> 
  


- **To check the current status of the transaction go in the _Transaction_ tab. As we saw before the transaction still has no confirmations yet, you will need at least to wait 2 min to see it as confirmed.**

![unconfirmed](/static/img/gui10.png "Unconfirmed")

  <br />
  <br /> 
  <br />


- **Once the transaction is confirmed you need to wait for enough confirmations (set to 10 blocks by default) to spend the fund received recently.**   

![confirmed](/static/img/gui11.png "awaiting confirmations")

  <br />
  <br /> 
  <br />


- **Once 10 confirmations (10 minutes) are reached, you can spend it directly after**.   

![+10confirmation](/static/img/gui12.png "+10 confirmations")



