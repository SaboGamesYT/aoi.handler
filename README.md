<h1 align="center"><strong>AOI.JS-HANDLER</strong></h1>
2
3<p align="center">
4<img src="https://media.discordapp.net/attachments/1022533781040672839/1137241711614115910/Untitled96_20230805101633.png" alt="Logo" width="150" height="150">
5</p>
6
7
8<p>
9  aoi.js-handler is a package built for aoi.js to make it easy for users to load their command, events, custom functions and statuses.
10</p>
11<h2 align="center"><strong>Installation</strong></h2>
12
13```js {3} copy
14npm install aoi.js-handler
15```
16<h2 align="center"><strong>Setup</strong></h2>
17
18```js {3} copy
19// Import necessary modules
20const { AoiClient } = require("aoi.js");
21const { Handler } = require("aoi.js-handler")
22
23// Create a new AoiClient instance
24const client = new AoiClient({
25  token: "Discord Bot Token",
26  prefix: "Discord Bot Prefix",
27  intents: ["MessageContent", "Guilds", "GuildMessages"],
28  events: ["onMessage", "onInteractionCreate"],
29  database: {
30    type: "aoi.db",
31    db: require("@akarui/aoi.db"),
32    dbType: "KeyValue",
33    tables: ["main"],
34    securityKey: "a-32-characters-long-string-here",
35  }
36});
37
38// Initialize a Handler for structured command handling
39const handler = new Handler(
40  {
41    client: client,
42    readyLog: true
43  },
44  {
45    // Additional Handler configuration options go here
46  },
47  __dirname
48);
49
50// Module is now ready for use
51``` 
52
53# Useful Links
54| <a href="https://github.com/aho-emi/aoi.handler" target="_blank" rel="noopener noreferrer"><p align="center"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/91/Octicons-mark-github.svg/2048px-Octicons-mark-github.svg.png" alt="GitHub" width="35" height="35" style="border-radius: 50%;"></p>Github - aoi.handler</a> | <a href="https://www.npmjs.com/package/aoi.handler?activeTab=readme" target="_blank" rel="noopener noreferrer"><p align="center"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/db/Npm-logo.svg/2560px-Npm-logo.svg.png" alt="npm" width="75" height="35"></p>NPM - aoi.handler</a> | 
55| ---- | ---- |
56| <a href="https://aoi-handler.vercel.app" target="_blank" rel="noopener noreferrer"><p align="center"><img src="https://media.discordapp.net/attachments/902553397281030208/1137604638766530670/Untitled96_20230805101633.png" alt="docs" width="55" height="55"></p><strong>DOCS - aoi.handler</strong></a> | <a href="https://discord.gg/3vcucB8F5c" target="_blank" rel="noopener noreferrer"><p align="center"><img src="https://www.freepnglogos.com/uploads/discord-logo-png/concours-discord-cartes-voeux-fortnite-france-6.png" alt="support" width="55" height="55"></p><strong>Discord Support</strong></a> |
57
58### **Visit docs for further information.**
59
60
61## **Showcase**
62### Command Loader
63![command loader](https://media.discordapp.net/attachments/1029040684172333056/1185974042386243625/IMG_4470.png)
64
65### Variable Loader
66![variable loader](https://media.discordapp.net/attachments/1029040684172333056/1185974041656442900/IMG_4470.png)
67
68### Status Loader
69![status loader](https://media.discordapp.net/attachments/1029040684172333056/1185974041383809196/IMG_4470.png)
70
71### Custom Function Loader
72![function loader](https://media.discordapp.net/attachments/1029040684172333056/1185974041052463245/IMG_4470.png)
73
74
75### readyLog: true 
76![readyLog loading](https://media.discordapp.net/attachments/1029040684172333056/1185974042063286392/IMG_4471.png)
