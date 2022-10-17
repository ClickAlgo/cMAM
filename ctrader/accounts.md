# How it works?

To allow cMAM to access your trading accounts, you must first add those accounts on cMAM. 

cMAM uses Open API to access cTrader trading accounts, you have to first create an Open API application and enter its credentials on cMAM to be able to add cTrader trading accounts on cMAM.

You just need one Open API application for managing as many cTrader trading accounts as you want to from different cID profiles.

After you added your accounts and authorized your previously created Open API application to have access to those authorized account then cMAM will be able to perform trading operations on those added accounts.

Before adding accounts to cMAM you must finish the Open API configuration.
 
The account adding process is very simple and straightforward.

# Adding an account

Open cMAM and go to the "Trading Accounts" view, then click on the "Add Account" button:

![Screenshot](../img/accounts_0.png)

Open the authentication URL on your system browser by clicking on authentication URL open icon button:

![Screenshot](../img/accounts_6.png)

If you are using cMAM default redirect URL then it will show the authentication code after account authorization:

![Screenshot](../img/accounts_7.png)

As you can see the authentication code is in green box, your client must copy and give you back this code before the code expires, it has one minute expiry time and after one minute it will become useless or invalid.

If you are using your own redirect URL then the authentication code will be appended on your redirect URL via a "code" parameter, it will look like this:

http://your_redirect_url/?code=324hdsaldh2uesa342edasdsaddc332jdh

Once you got the code you have to immediately enter it on "Auth Code" text box field and click on "Add Accounts" button:

![Screenshot](../img/accounts_5.png)

cMAM will start the adding account process and it will show a progress dialog box.

***If you want to add new trading accounts from the same cID profile that already has some accounts connected to cMAM, please don't forget to select those previously added accounts too. If you don't, then cMAM will lose access to those previously added accounts and it will not execute any trading operation on those accounts, those not selected accounts status will change to deactivated (not active) in cMAM accounts list, if you forgot to do this then you can add the accounts again, there is no need to remove the deactivated accounts from cMAM, just add all added accounts again.***

# Account view

Once you have added an account to cMAM, you can navigate to that account view by clicking the open icon button on the accounts list:

![Screenshot](../img/accounts_4.png)

You will be able to see the account's open positions, pending orders, history, and transactions.

On the right side of the account view there is an account info section which shows all of the account's related details.

At the end of the account info section there is a check box drop down field, which you can use to create account categories and assign the account to one or more of those categories. In the case that you would want to assign multiple trading accounts to a category, you can use the account list view instead. The same category selection field is available in the accounts view tool bar.

You can also set an alias to an account for differentiating it from your other accounts in account view.

