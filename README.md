# **Gunbot Autoconfig**

> **Automatic Bittrex pair selection for Gunbot > v4.**

> **Updater tool for Gunbot config.js**

> **Use up to 5 trading profiles**

> **Trading API key stored local only**

> **Optional PM2 launcher for fast single pair Gunbot instances**



**[AutoConfig is now fully integrated into Gunbot v15](https://www.gunbot.com/)**

**[The info on this page is about the legacy version, click here for updated docs](https://wiki.gunthy.org/how-to-work-with-gunbot/autoconfig)**



## **How it works**
Gunbot Autoconfig provides a web interface to setup your gunbot config file and automatically select pairs filtered by Tradingview ratings, volume and volatility. This config file is synced with your Gunbot machine with a multi platform updater tool. 




### **Settings for pair filtering & bag handling**

![setup image](https://user-images.githubusercontent.com/2372008/31356083-f43a7042-ad3c-11e7-8494-0c971ad59e49.png)

**Filtering options for:**
> Max. number of trading pairs

> Minimum BTC volume 

> TradingView [ratings](https://www.tradingview.com/markets/cryptocurrencies/quotes-bitcoin/)

> Volatility

> Customizable buy / sell options for bags.




### **JSON config editor with trading profiles**

![json editor gif](https://user-images.githubusercontent.com/2372008/31355641-72952fba-ad3b-11e7-855e-849b9c6b53bd.gif)

> Easy to use JSON editor for all Gunbot settings

> Override strategy settings with profiles for each TradingView rating




### **Dashboard for starting setups and monitoring logs**

![dashboard image](https://user-images.githubusercontent.com/2372008/31355630-6ac8b20c-ad3b-11e7-8038-160b75e47349.png)
> Config preview


![logs image](https://user-images.githubusercontent.com/2372008/31355618-5b3692e6-ad3b-11e7-8450-a03a9016f7b4.png)
> Logviewer for config changes

![orders image](https://user-images.githubusercontent.com/2372008/31402813-6c756c5a-adf7-11e7-8774-2412c703fcf3.jpg)
>  Order overview




### **Multiplatform updater app for Gunbot config file**

> Updater works on Windows, Linux and MacOS

> Bittrex API key for trading is saved on local machine only




### **PM2 Launcher to automatically start each pair in a new Gunbot instance**

![launcher gif](https://user-images.githubusercontent.com/2372008/31355649-7cec3684-ad3b-11e7-8784-95d85ac39e19.gif)
*actual gunbot speed with the launcher*

PM2 Launcher script for PM2 to automatically launch Gunbot instances for each pair in your config. For Linux only.

- Speeds up cycling rate to about 1s per pair
- Saves Gunbot logs for all pairs
- Automatically reloads Gunbot settings when config file is updated




## **Getting started**
1. [Join the Telegram group](https://t.me/joinchat/Fci7JUOw9Z7i0eUpUrAZmQ) and request an invite
1. [Create your free BETA account](https://app.gunbot-autoconfig.com)
1. Enter read only API key to retrieve Bittrex data (and improve pair selection)
1. Create a setup for pair filtering and your Gunbot settings
1. Preview your setup and start it
1. Install the updater, enter login data and trading API key
1. *Optional: install PM2 launcher*
1. Start running Gunbot or start the launcher




## **Downloads & instructions**
Installation instructions for the updater and launcher are provided at GitHub. 

Dashboard: [https://app.gunbot-autoconfig.com](https://app.gunbot-autoconfig.com)



### **Updater**
[Updater on GitHub](https://github.com/Gunbot-Autoconfig/Gunbot-Autoconfig/releases)



### **Launcher**
[Launcher on GitHub](https://gist.github.com/GuilhermeMedeiros/eb9f0f8b4161cdb87d5fac822447ab6c)




## **FAQ**

### What does Gunbot Autoconfig consider a bag?
All pairs that you have balance on and are no longer between the pairs in your config, are considered bags. A pair must have met the filter criteria you've set to trade on at least once to be consided a bag.

### I'm just starting with Gunbot Autoconfig, how can I let it handle my old bags?
To include your old bags in the config file that Gunbot Autoconfig creates, you need to make sure that these pairs have been in your setup once. To do so, you could create a setup with really loose settings for mimimum buy rating, volatility and volume - this way all pairs will be considered for trading (don't run Gunbot at this time). Start the setup in the dashboard and keep it running for a short while. Afterwards, update the setup so that it reflects the actual settings for pairs you want to really trade on. Your bags should be in there now.

### Is this tool secure to use?
As long as you're fine with the concept to use Gunbot with a dynamically generated config file based on your preferences, yes it is. The online part of the toolset works with just a read only API key for Bittrex: it cannot do actual harm. Your trading API key is stored on your local computer only.

