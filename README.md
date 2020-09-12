# Quest Messenger JS
> We strive to become the first fully featured, multi-platform, publicly auditable, decentralized, end-to-end encrypted messenger with a feature to send money to rival all the chat apps out there.

![Screenshot](https://github.com/QuestNetwork/quest-messenger-js/raw/0.9.2/doc/images/0.9.2.png?raw=true)

## Lead Maintainer

[StationedInTheField](https://github.com/StationedInTheField)


## Description
The Quest Messenger is on track to become the first fully featured, multi-platform, publicly auditable, decentralized, end-to-end encrypted messenger with a feature to send money to rival all the other chat apps. It makes use of the [Interplanetary Filesystem](https://ipfs.io), [IPFS GossipSub](https://blog.ipfs.io/2020-05-20-gossipsub-v1.1/) as well as of the [Quest Network PubSub Protocol](https://github.com/QuestNetwork/quest-pubsub-js), [Quest Network Image Captcha](https://github.com/QuestNetwork/quest-captcha-js) and the Quest Network Whistle ID Protocol among others. We're planning to integrate payments soon, so you can send each other money!

We're planning to become for messaging what [Atom](https://atom.io) is for writing code. Full Matrix integration is planned as well.

The Quest Messenger works in the browser, as an Electron on Windows, Mac and Linux and Android using Cordova.

Check out other [Awesome Quest Network dApps](https://github.com/QuestNetwork/awesome/blob/master/README.md)!

## Support Us
This project is a lot of work and unfortunately we need to eat food (ツ)

| Bitcoin | Ethereum | 
|---|---|
| `bc1qujrqa3s34r5h0exgmmcuf8ejhyydm8wwja4fmq`  |  `0xBC2A050E7B87610Bc29657e7e7901DdBA6f2D34E` |
| <img src="doc/images/btc-qr.png" >  | <img src="doc/images/eth-qr.png" >  | 

## Download

| Version | Linux | Mac |
|---------:|------------------------------|------------------------------|
| 0.9.1 |  [quest-messenger-0.9.1.AppImage](https://github.com/QuestNetwork/quest-messenger-js/releases/download/0.9.1/quest-messenger-0.9.1.AppImage) | [quest-messenger-0.9.1.dmg](https://github.com/QuestNetwork/quest-messenger-js/releases/download/0.9.1/quest-messenger-0.9.1.dmg) |

If you want anything else, you'll have to build from sources and probably fix some stuff.

**WARNING:** THIRD PARTY DEPENDENCIES NOT AUDITED YET! APP HAS ACCESS TO FILESYSTEM! USE IN VIRTUAL MACHINE UNTIL 1.0.0!

## IPFS Gateways

https://gateway.pinata.cloud/ipfs/QmYDKkaCtwAG1obMezLS1RgNmke5CxjrtdRU4fdpgzMuP4/

https://cloudflare-ipfs.com/ipfs/QmYDKkaCtwAG1obMezLS1RgNmke5CxjrtdRU4fdpgzMuP4/

https://ipfs.eternum.io/ipfs/QmYDKkaCtwAG1obMezLS1RgNmke5CxjrtdRU4fdpgzMuP4/

https://ipfs.io/ipfs/QmYDKkaCtwAG1obMezLS1RgNmke5CxjrtdRU4fdpgzMuP4/

http://ipfs.infura.io/ipfs/QmYDKkaCtwAG1obMezLS1RgNmke5CxjrtdRU4fdpgzMuP4/

https://35.208.30.22/ipfs/QmYDKkaCtwAG1obMezLS1RgNmke5CxjrtdRU4fdpgzMuP4/


## IPFS Deploy
**Memory** 3.75GB **Storage** 6GB **NodeJS** 14 **NPM** 6 **IPFS** 0.6

```git clone https://github.com/QuestNetwork/quest-messenger-js```

```cd quest-messenger-js```

```git checkout 0.9.2```

```npm install```

```npm run ipfs```

```ipfs pin add <CID>```

If you have trouble getting the directory discovered by gateways, you can try ```./ipfs-propagate.sh``` from the root git folder. 
Keep in mind that the bundled web application is >6MB alone without assets, please be patient until we have a preloader.

## Development

**Prerequisites**

To fully participate in the development, you'll need: 
- [Quest Network Operating System](https://github.com/QuestNetwork/quest-os-js)
- [Quest Network Bee Process](https://github.com/QuestNetwork/quest-bee-js)
- [Quest Network Ocean Process](https://github.com/QuestNetwork/quest-ocean-js)
- [Quest Network Dolphin Process](https://github.com/QuestNetwork/quest-dolphin-js)
- [Quest Network PubSub Process](https://github.com/QuestNetwork/quest-pubsub-js)

```git clone https://github.com/QuestNetwork/quest-os-js && git clone https://github.com/QuestNetwork/quest-bee-js && git clone https://github.com/QuestNetwork/quest-ocean-js && git clone https://github.com/QuestNetwork/quest-dolphin-js && git clone https://github.com/QuestNetwork/quest-pubsub-js && git clone https://github.com/QuestNetwork/quest-messenger-js ```

**Commands**


To The same directory you're cloning this repository to.

```npm run inst``` Removes ```package-lock.json``` and runs ``npm install``

```npm run linux``` Builds Linux AppImage and Snap files to ```dist/```

```npm run mac``` Builds MacOS DMG and .app files to ```dist/``` and ```dist/mac```

```npm run ipfs```  Creates the bundled application for the web with dynamic base path to ```dist/web```

```npm run web``` Creates the bundled application for the web with base path ```/```  to ```dist/web```

```npm run serve``` Serves the bundled application on ```localhost:4200``` from ```dist/web```

```ng serve``` Serves a just in time compilation of the messenger on ```localhost:4200```

```npm run serve-fresh``` Runs ``rm -rf node_modules && npm run inst && ng serve``

```watch-reset``` Cleans the watch list, in case of ```System Limit``` error


We added an example ```swarm.json``` to the ```src/app``` folder with an example node to make reproduction easier, but we strongly recommend to use our [Quest CLI](https://github.com/QuestNetwork/quest-cli) to test and build the app.

Pro Tip: Put a file in your `/bin` that runs the quest-cli like so `node /path/to/quest-cli/index.js` from any folder on your system. It's much nicer!

## Features

**0.9.0**
- Does not depend on the internet
- Does not depend on centralized servers
- No static external address or port forwarding necessary
- Dark Mode
- Messages are signed using P-521 EC keypairs
- Encrypted P2P Channels (End-To-End, AES-256-CBC, Shared Via 4096 Bit OAEP)
- Organize Channels By Transport/Protocol And Custom Groups (like project folders in Atom)
- AutoSave For Settings

**0.9.1**
- Auto SignIn, if signed in
- Create Channels/Folders
- Generate Invite Tokens (optional with folder structure)
- Import/Join From Invite Token (optional with folder structure)
- Delete Channels

**0.9.2**
- After 0.9.0 & 0.9.1 proved the concept, 0.9.2 is almost an entire rewrite 
- IPFS Update (0.50.1)
- Enhanced Mobile UI, Centered Snackbar, New Fonts, Icons & Buttons
- Included All Fonts And Icons In The Bundle
- [Quest Network Operating System](https://github.com/QuestNetwork/quest-os-js)
- [Quest Network Bee Process](https://github.com/QuestNetwork/quest-bee-js)
- [Quest Network Ocean Process](https://github.com/QuestNetwork/quest-ocean-js)
- [Quest Network Dolphin Process](https://github.com/QuestNetwork/quest-dolphin-js)
- Delete Folders
- Drag/Drop Folders/Channels
- Export Settings
- SignOut
- Enable Write Lock To Keep All Processes From Writing
- Disable AutoSave
- Change AutoSave Interval
- Disable Challenge Flow (close channels to invite only)
- Dynamic Swarm Peer List On Desktop (add and remove bootstrap peers)
- Share and Import Channels By QR Code

## Roadmap

**0.9.3**
- Sidebars resizable
- Participant/Friends Groups And Folders
- Set Alias (show custom name instead of pub key) and profile pictures
- Pair with participants by QR Code
- Private Encrypted P2P Channels (End-To-End, AES-256-CBC, Shared Via 4096 Bit OAEP)
- Encrypted Audio/Video P2P Channels (Encryption Can Be Turned Off For Higher Quality)

**0.9.4**
- Ignore/Mute Channel Participants Locally
- Ban Channel Participants By Generating New Channel Names (ask representatives for new name, refuse banned participants

**0.9.5**
- Encrypted Audio/Video Group Channels (Encryption Can Be Turned Off For Higher Quality)
- AES Encrypt Invite Tokens
- AutoSave For Message Histories
- Export Message Histories

**0.9.6**
- [Quest Network Coral Process](https://github.com/QuestNetwork/quest-coral-js)
- Encrypted P2P File Transfer (End-To-End AES-256-CBC, Shared Via 4096 Bit OAEP)
- Inline Preview For Media Files And Links (images, videos, etc)
- Encrypt Settings/Message History Files

**0.9.7**
- Private Channels Extendable To Groups (background create and join)
- Add Custom Themes By Pasting CSS Into The Built-In Theme Editor
- Import/Export Themes
- Light Mode

**0.9.8**
- Badges for unread messages
- Desktop Notifications

**0.9.9**
- Ethereum Payment Integration Beta

**1.0.0**
- Third Party Dependencies Audited, Security Issues Fixed
- Dynamic Swarm Peer List Also On The Web (add and remove bootstrap peers)
- Unlimited Custom Emojis
- Quest Network Calendar App Plugin (for shared calendars)
- IRC Plugin

**1.1.0**
- QuickResponse (from list of possible responses)
- AutoResponse (from quick responses)

**1.2.0**
- Parenting (reply to channel and private messages)
- Sync Message History (like syncing the blockchain, channel participants can offer a history, since every message is signed with an elliptic curve key, we can verify and merge it into ours)

**2.0.0**
- Ethereum Payment Integration Finalized

**3.0.0**
- Matrix Plugin to add Matrix rooms and communities

**4.0.0**
- [OpenAI GPT3](https://en.wikipedia.org/wiki/GPT-3) Integration For Suggestions, AutoRespond And Completion

**5.0.0**
- Quest Network Widgets (plug-in that connects the messenger to other apps, for example collaborative illustration in Inkscape)
- Modular Crypto Currency Integration (presets for Bitcoin, Monero and Chainlink)
- Share Screen

## License

GNU Affero GPLv3
