<p align="center">
  <img src="https://github.com/BrewTheFox/ReKITtyPaw/blob/main/images/rainbow-color.gif?raw=true" alt="ReKITtyPaw" width="100%", =50%>
</p>

<h1 align="center">
  ReKITtyPaw
</h1>

<p align="center">
  <img src="https://github.com/BrewTheFox/ReKITtyPaw/blob/main/images/Shulker.gif?raw=true" alt="ReKITtyPaw" width="10%">
</p>


<p align="center">
  <img src="https://github.com/BrewTheFox/ReKITtyPaw/blob/main/images/rainbow-color.gif?raw=true" alt="ReKITtyPaw" width="100%">
</p>

## What is this?
#### ReKITtyPaw is a Minecraft bot designed to simplify the setup of kit delivery bots in anarchy servers. Developed in JavaScript using the Mineflayer library, ReKITtyPaw aims to simplify the configuration process through an easy-to-use JSON file.

## Key Features:

- #### Easy to configure.
- #### Compatible with almost* any server.
- #### Made to be used together with discord.

## How to install:
- #### First of all clone the git repository of the project with this command:

```bash
git clone https://github.com/BrewTheFox/ReKITtyPaw.git ./ReKittyPaw
```

- #### Then change the directory to ReKittyPaw:


```bash
cd ReKittyPaw
```

- #### Install the project dependencies:


```node
npm install
```

## How to configure:
#### After you have installed the project, you should configure it in the file ./config.json. There are some important things to take into consideration.

- ## Keywords
  
  | **Keyword**        | **Replaced With**                                                     | **Used in**                                                                            |
  |--------------------|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------|
  | {{User}}           | The minecraft username of the person that requested the delivery.     | UTPCancelMSG, UTPAcceptMSG, ExpiredTP, AcceptTPASK, ErrorMessage, UnstockedItemMessage |
  | {{TPAcceptTime}}   | The time that you've set on TPAcceptTime converted to seconds.        | AcceptTPASK                                                                            |
  | {{RequestID}}      | A randomly generated uuid generated after the user requested the kit. | ExpiredTP, AcceptTPASK, ErrorMessage, UnstockedItemMessage                             |
  | {{MinuteKitDelay}} | Replaced with the value of MinuteKitDelay in the config file.         | KitDelayMessage                                                                        |

- ## The example ./config.json file

  | **Keyword** | **Content** | **Usage** |
  |---|---|---|
  | token | havfYeMZVkMmAfz0TiNmyFYcGk19rdSG1xV11NP2Cp8yP6pygeQndRLSyNezpCz0T9Y2BpDm3JwNUrFcUhuNtVVwzP3d2Rzwe6uw | This is your discord bot token |
  | username | MyNameIsBot | Bot's minecraft username |
  | password | ThisIsMyPassword | If the server needs authentication here is where you should put the bot password |
  | host | RandomAnarchyServer.net | The minecraft server IP Address |
  | port | 12345 | The minecraft server port |
  | version | 1.18.1 | The minecraft server version |
  | TPDelay | 5000 | The delay the bot will need to wait after the user accepted the teleport request |
  | HomeDelay | 8000 | The delay the bot will need to wait after "/home" is written |
  | LavaCoords | [-14, 65, 0] | A array containing the coordinates of the lava formatted [X,Y,Z] |
  | TPAcceptTime | 15000 | How much time does the bot gives the user to accept the teleport request (Miliseconds) |
  | MaxDeliverKits | 10 | How many kits can deliver the bot per request |
  | BotOwner | ThisIsYourMinecraftUsername | Your minecraft username |
  | HomeMessage | You are now in home | The message that shows up in the minecraft chat when you've successfully teleported to your home |
  | HomeCancelMSG | Pending teleportation request cancelled. | The message that shows up in the minecraft chat when you didn't teleport to your home |
  | AfterRegisterMSG | Successfully registered! | The message that shows up in the minecraft chat when you register in the server |
  | AfterLoginMSG | You have successfully logged in! | The message that shows up in the minecraft chat when you login in the server |
  | RegisterMSG | Please use /register 'Password' 'Password' to register. | The message that shows up in the minecraft chat that asks you to register |
  | LoginMSG | Welcome again. Please use /login 'Password' to start enjoying. | The message that shows up in the minecraft chat that asks you to login |
  | UTPCancelMSG | [RandomTPA] {{User}} cancelled your petition! | The message that shows up when the user cancels your teleport request  |
  | UTPAcceptMSG | [RandomTPA] {{User}} Teleported to you! | The message that shows up when the user accepts your teleport request |
  | AcceptTPASK | You have {{TPAcceptTime}} seconds to accept your request that have the id {{RequestID}} before it cancels. | The message that the bot sends to the player before sending the teleport request |
  | ExpiredTP | The request with the id {{RequestID}} expired. | The message that the bot sends after the teleport request expired |
  | UnstockedItemMessage | One of the items that you have requested is not in stock, please try again later :( | The message that the bot sends if there is no stock of certain item |
  | ErrorMessage | There was a problem delivering the kit, please try again later :( | The message that the bot sends if the delivery is cancelled |
  | KitSelectionMenuTitle | Selection Menu - Ranarchy | The discord menu embed title |
  | MinuteKitDelay | 5 | How long does the user will need to wait before begin able to request another kit |
  | KitDelayMessage | Hey hold on you didn't wait the {{MinuteKitDelay}} minutes delay :( |  |
  | EmbedTitle | Request a delivery. |  |
  | Embed1Title | How to? |  |
  | Embed1Content | Just click the button down this text |  |
  | Embed2Title |  |  |
  | Embed2Content |  |  |
  | Embed3Title |  |  |
  | Embed3Content |  |  |
  | KitMenuOpenText | Request your kit NwN |  |
  | ServerRestartError | We're sorry. Our Server restarted, please try filling the form again. |  |
  | MinecraftEmptyServerError | Hey. you're not on the Minecraft Server. |  |
  | NameAskMessage | Now tell me. which one is your nickname? |  |
  | GenericError | We're sorry. there was a problem handling your request. |  |
  | VoucherText | Thank you for using Ranarchy delivery bot. Please wait some time for the bot to be available and delivers your kit. |  |
  | KitsDict | {"KitOption1":"wither_skeleton_skull", "KitOption2":"detector_rail"} |  |
  | RepresentativeKitEmoji | 🍕 |  |
  | SelectedKitEmoji | 🌏 |  |
  | UnSelectedKitEmoji | 🧨 |  |
