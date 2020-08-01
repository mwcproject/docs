# HTTP listener troubleshooting
When using the HTTP transfer method it can be usefult to test that the HTTP listener on your MWC node is still working correctly before trying to send or recieve coins especially from an exchange

## Test your MWC node HTTP listener

To test to see if the wallet is working use curl or an online curl tool like
https://reqbin.com/curl

Then make a curl request to confirm your HTTP listener is working on your MWC node

    curl --request POST --data-raw '{"jsonrpc": "2.0","method": "check_version","id": 1,"params": []}' http://youripaddress:3415/v2/foreign

If your MWC node's HTTP listener is accessible it should return something like this

    { "id": 1, "jsonrpc": "2.0", "result": { "Ok": { "foreign_api_version": 2, "supported_slate_versions": [ "V3", "V2" ] } } }

If you do not recieve a valid response resolve the possible issues below as needed
____
## Your IP address may have changed

To check your ip use a tool like https://api.myip.com/

## The local IP address of your computer may have changed on  your router
The local IP address assigned to your computer by your router may have changed

Login to your router to confirm the local IP address with an open port of 3415 still refers to the computer running your MWC node

An example of your local IP address changing on your router would be your computer having an address of

    192.168.0.11
Then the local IP address changing to

    192.168.0.6    

If the local IP address has changed update your NAT records to ensure the open port of 3415 refers to the computer running your MWC node