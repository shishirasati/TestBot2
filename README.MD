# Project ANA - Open Source Conversation Suite

[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](http://www.gnu.org/licenses/gpl-3.0)

## DEPRECATED - This project is deprecated in favor of new [cross-platform Ana app](https://github.com/kitsune-tools/ana-app)

World's first **Open Source Conversation Platform** which comes with a **Graphical Chat Flow Designer** and **Chat Simulator**.
Supported channels are [Web Chat](https://github.com/Kitsune-tools/ANAChat-Web), [Android](https://github.com/Kitsune-tools/ANAChat-Android), [iOS](https://github.com/Kitsune-tools/ANAChat-iOS) and Facebook Messenger.

----------

[![Studio and Simulator Image](https://github.com/Kitsune-tools/ProjectANA/blob/master/Assets/anaflow.png)](https://github.com/Kitsune-tools/ProjectANA/blob/master/Assets/anaflow.png)

----------

## Installation

**Prerequisites:**

* Windows 10 PC with *developer mode* enabled. 
  - Developer mode is needed to install ANA Simulator as it is a [Universal Windows Platform](https://docs.microsoft.com/en-us/windows/uwp/get-started/whats-a-uwp) app usually distributed via Windows App Store.
  - To enable developer mode, go to your PC Settings > Update & Security > For Developers. Under 'Use developer features', choose 'Developer Mode'. 
* If you have older version of windows, ANA Conversation Studio will install but the ANA Simulator will not be installed. You can still publish and use the chat bot in [Web Chat](https://github.com/Kitsune-tools/ANAChat-Web), [Android](https://github.com/Kitsune-tools/ANAChat-Android), [iOS](https://github.com/Kitsune-tools/ANAChat-iOS) or Facebook Messenger.


**Installing ANA Conversation Studio:**

1.  Download `ANA Conversation Studio Setup x.x.x.msi` from [releases](https://github.com/Kitsune-tools/ProjectANA/releases/latest).
2.  Run it and follow the on screen instructions. 
    - If developer mode is not already enabled in your PC, installer will ask you to enable it.  
    - Once installation is complete, you can run the ANA Conversation Studio from the desktop or from start menu.

 **Note:** 
 
 To use localhost APIs in your chat, you need to run a small command which will unblock location APIs being used from the ANA Conversation Simulator. 
   - Open command prompt and run `checknetisolation loopbackexempt -a -n=44cabbc3-0a2f-4255-b5bb-b099cd5762f9_hvc7j3s42jt6e`. 
   - By default, localhost URLs are blocked in UWP Apps for security, above command will unblock it for only this particular app. 

----------

## Publishing your ANA chat bot

Once you have created and tested your chat bot in the ANA Simulator in your computer, you would want to publish it. You can publish your chat bot once and have it live on multiple channels, be it [Web Chat](https://github.com/Kitsune-tools/ANAChat-Web), [Android](https://github.com/Kitsune-tools/ANAChat-Android), [iOS](https://github.com/Kitsune-tools/ANAChat-iOS) or Facebook Messenger.

**Prerequisites**

To publish, you need an [ANA Chat Server](ANA-CHAT-SERVER-SETUP-README.MD)
   - Click [here](ANA-CHAT-SERVER-SETUP-README.MD) for instructions on how to setup one yourselves.
   - Assuming you have got one after following the above stated process, let's call it `http://ana-chat-server.com` 

**Publishing Steps**
   
   1. In ANA Conversation Studio, open the chat bot project you want to publish.
   2. Go to Tools>Publish. In the window that appears, click on 'Add Server/Chat Project'.
   3. Now, in the window that appears, click on the 'Add' button to the top left, then select 'New Publish Server' that was added.
   4. Enter your ANA Chat Server details 
      - Server URL is mandatory.
      - Key and Secret are only needed if they are set in the chat server. 
   5. Click on 'Chat Projects' field. In the window that appears, click 'Add' and enter a new 'Chat Project Id' and also a Name. The 'Chat Project Id' a.k.a. 'Business Id' is the one you need to link this chat bot on [Web Chat](https://github.com/Kitsune-tools/ANAChat-Web), [Android](https://github.com/Kitsune-tools/ANAChat-Android), [iOS](https://github.com/Kitsune-tools/ANAChat-iOS) or Facebook Messenger.
   6. Click 'Ok' and then Click 'Save'. You should be back to Publish Window. Choose the server you just created, in Server drop down. Choose the Chat Project you just created, in Chat Project drop down and click publish.

## Deploying your ANA chat bot

The following channels are supported for deploying your ana chat bot. Follow the links for instructions.
   1. [Web Chat](https://github.com/Kitsune-tools/ANAChat-Web)
   2. [Android](https://github.com/Kitsune-tools/ANAChat-Android)
   3. [iOS](https://github.com/Kitsune-tools/ANAChat-iOS)
   4. Facebook Messenger (Coming soon...)

## Note

This is just the setup documentation. ANA Conversation Suite has much more scope than predefined flows. You can call your own APIs from the chat, capture and save information from the user. You can take different types of inputs like button clicks, text, image, video etc. For now, explore the code to get to know all the possibilities.

Detailed documentation is on its way.

## License

ANA Conversation Suite is available under the [GNU GPLv3 license](https://www.gnu.org/licenses/gpl-3.0.en.html).

