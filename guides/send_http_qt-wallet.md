# Send via HTTP using the QT Wallet

## Contents : 
  * [Requirements](#requirements)
  * [Send via HTTP using the GUI Wallet](#Send-via-HTTP-using-the-GUI-Wallet)
  
------
  
## Requirements
To follow this tutorial, you will need the following:

- Up-to-date MWC QT-Wallet Software : https://github.com/mwcproject/mwc-qt-wallet/releases
- An active Internet Connection

------

## Send via HTTP using the GUI Wallet

 
 First let's lay out the overall procedure, a Detailed description with Images is below.
 
 1) Select the "Send" Tab
 2) Enter the Amount you wish to send
 3) click on "Next"
 4) Enter the Receiving Address in the "Send to" Field
 5) Click Send  
 6) If you have registered HODL Coins you will see a Dialog to doublecheck the Outputs that are spent.
 If you want to spend those Outputs confirm by clicking "Continue"
 7) Confirm typing your password and wait for the transaction to confirm
 
 
  - **Select the "Send" Tab of your Wallet and enter the Amount you want to send:**
  
  ![selectsend](/static/img/selectsend.png "Select Send")  
  
  <br />
  <br /> 
  <br /> 
  
  - **Enter the receiving Address and click "Send"**
  
   ![sendtransaction](/static/img/sendtransaction.png "sendtransaction")  
   
   <br />
   <br /> 
   <br /> 
   
  - **If you got HODL'ed Outputs, check if you want to spend those and Confirm by clicking "Continue" and enter your password**
  
   ![hodldialog](/static/img/hodldialog.png "HODL Dialog")  
  
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



