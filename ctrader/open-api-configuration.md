## What's Open API?

cMAM uses Spotware Open API service to access your cTrader trading accounts and perform trading operations on your behalf, this API allows cMAM to have full access to your trading accounts like you do via cTrader without any kind of dependence on cTrader.

Spotware Open API is part of their cTrader package, all of the cTrader supported brokers will also have the Open API service, so for cTrader users its free to use Open API.

Below you can find the details of how to start using Spotware Open API.

## Creating an application

The first step to use Open API is to create an API application, its like registering for API to get access to it.

Go to the [Spotware Open API web page](https://openapi.ctrader.com/):

![Screenshot](../img/open_api_0.png)

Log in with your cTrader ID account, then navigate to the [applications page](https://openapi.ctrader.com/apps). 

Click on the "Add New Application" button.

![Screenshot](../img/open_api_1.png)

Now fill the application form, for example:

* Channel: Your_cTrader_ID_Username_cMAM (ex: afhacker_cMAM)

* Logo: Its optional, you don't have to provide a logo

* Description: This app will be used by cMAM for copy trading

* Redirect URIs: Please add the cMAM redirect URI on your application redirect URIs list, it's **http://api.algodeveloper.com/redirects/**

![Screenshot](../img/open_api_5.png)

* Contact Name: Your first name

* Contact Surname: Your last name

* Phone: Your phone number

* Company Name: cMAM

* Company Website: https://www.algodeveloper.com/

* Application Usages: Check "Access own account information" and "Trading for own purpose"

* Allowed Grant Types: Check all the boxes

!!! warning

	**Please follow the above guide exactly while filling your application form, otherwise Spotware will not activate your application.**

After you filled the form click on "Save" button.

Now your application will appear on your applications list on the site.

![Screenshot](../img/open_api_2.png)

**To get your application credentials (client ID / Secret) click on "View" button of the application on your applications list.**

As you can see I have plenty of Open API applications on my account which I use for different things, and all my applications are active, the application you just created isn't active yet, its status will be "Submitted" not "Active".

## Application Activation

After you created your Open API application, the next step is to activate the app, Spotware will review and activate your app in 24-48 hours after your application submission.
 
## Configuring

Once your application got activated then you can setup cMAM to use your API application, open cMAM and go to Settings -> Open API Configuration:

![Screenshot](../img/open_api_3.png)

![Screenshot](../img/open_api_4.png)

There you have three fields inside "Application" group on the right side, enter your application Client ID, Secret, and the Redirect URI you used during application creation, if you used the default cMAM Redirect URI then you don't have to change the redirect URI field and leave the default value.

If you haven't provided any Redirect URI for your application you can do it now, go to your [applications page](https://connect.spotware.com/apps), click on the application "Edit" button, you will see the same application creation form again but this time it will be filled with your application detail, you can add a Redirect URI and then save the application.

**We recommend you to use the cMAM default redirect URI as it will save your time and makes the API configuration easy.**

After you entered your application credentials (client Id, secret, and redirect URI), scroll down and click save button, a connection dialog will appear and if it disappeared quickly then it means cMAM was able to connect successfully, otherwise it will stuck and you have to click the "Let's do it" button on the dialog to configure the API again.

## API Advanced Options

You can change all the settings related to API if you want to, there is no need to change these options unless you are using your own open API proxy which you can get if you have large trading volume and it will allow more requests per second which will decrease the latency of cMAM.

You shouldn't increase the maximum requests per second, the Open API limits it to 50, if you increase it then you might face bad behavior on the program.