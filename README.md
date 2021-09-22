# MailBag
MailBag is a single sign on application that links an email address using IMAP and SMTP to a client's front-end interface, based off Frank Zammetti's starter code. After installing and configuring your email with IMAP, you will be able to control your email through a custom-built client interface in your browser. 

#### Languages and Technology Used
* TypeScript
* React.js
* Node.js
* Webpack
* Docker 

#### Frameworks Used
* express.js
* neDB 
* nodemailer
* mailparser
* emailjs-imap-client 

#### Software Requirements
* Node.js
* NPM 

#### Config IMAP
* You need access to an outside email address along with its corresponding IMAP information. This all goes into the file <code>serverInfo.json</code> located in the <code>/server</code> directory. There is already an example JSON file there named <code>example_serverInfo.json</code>. Make sure to rename the example file for use. <br>
* The config file will look similar to this: 

```
{
    "smtp" : {
      "host" : "imap.gmail.com",
      "servername": "imap.gmail.com",
      "port" : 465,
      "auth" : {
        "user" : "a@gmail.com",
        "pass" : "x"
      }
    },
    "imap" : {
      "host" : "imap.gmail.com",
      "servername": "imap.gmail.com",
      "port" : 993,
      "auth" : {
        "user" : "a@gmail.com",
        "pass" : "x"
      }

    }
}
```
* Make sure to enable IMAP with your email provider 
* You may run into TLS/SSL errors as well as less secure application authentication failures. The solutions vary depending on your email provider and their security settings. 

#### Install and Run 
Make sure the paths are correct so the server folder can find the client directory. <br> 
In the <code>/server</code> directory run <br>
```npm install``` 
and then <br> 
```npm run dev``` <br> 
to compile the TypeScript and launch the server 

#### File Rundown 
├── client
│   ├── dist
│   │   ├── index.html
│   │   ├── main.js
│   │   ├── main.js.map
│   │   ├── src
│   │   │   └── code
│   │   │       ├── components
│   │   │       │   ├── BaseLayout.js
│   │   │       │   ├── BaseLayout.js.map
│   │   │       │   ├── ContactList.js
│   │   │       │   ├── ContactList.js.map
│   │   │       │   ├── ContactView.js
│   │   │       │   ├── ContactView.js.map
│   │   │       │   ├── MailboxList.js
│   │   │       │   ├── MailboxList.js.map
│   │   │       │   ├── MessageList.js
│   │   │       │   ├── MessageList.js.map
│   │   │       │   ├── MessageView.js
│   │   │       │   ├── MessageView.js.map
│   │   │       │   ├── Toolbar.js
│   │   │       │   ├── Toolbar.js.map
│   │   │       │   ├── WelcomeView.js
│   │   │       │   └── WelcomeView.js.map
│   │   │       ├── config.js
│   │   │       ├── config.js.map
│   │   │       ├── Contacts.js
│   │   │       ├── Contacts.js.map
│   │   │       ├── IMAP.js
│   │   │       ├── IMAP.js.map
│   │   │       ├── main.js
│   │   │       ├── main.js.map
│   │   │       ├── SMTP.js
│   │   │       ├── SMTP.js.map
│   │   │       ├── state.js
│   │   │       └── state.js.map
│   │   ├── webpack.config.js
│   │   └── webpack.config.js.map
│   ├── package.json
│   ├── package-lock.json
│   ├── src
│   │   ├── code
│   │   │   ├── components
│   │   │   │   ├── BaseLayout.tsx
│   │   │   │   ├── ContactList.tsx
│   │   │   │   ├── ContactView.tsx
│   │   │   │   ├── MailboxList.tsx
│   │   │   │   ├── MessageList.tsx
│   │   │   │   ├── MessageView.tsx
│   │   │   │   ├── Toolbar.tsx
│   │   │   │   └── WelcomeView.tsx
│   │   │   ├── config.ts
│   │   │   ├── Contacts.ts
│   │   │   ├── IMAP.ts
│   │   │   ├── main.tsx
│   │   │   ├── SMTP.ts
│   │   │   └── state.ts
│   │   ├── css
│   │   │   └── main.css
│   │   └── index.html
│   ├── tsconfig.json
│   └── webpack.config.js
├── LICENSE
├── README.md
└── server
    ├── dist
    │   ├── contacts.db
    │   ├── Contacts.js
    │   ├── Contacts.js.map
    │   ├── IMAP.js
    │   ├── IMAP.js.map
    │   ├── main.js
    │   ├── main.js.map
    │   ├── ServerInfo.js
    │   ├── ServerInfo.js.map
    │   ├── SMTP.js
    │   └── SMTP.js.map
    ├── example_serverInfo.json
    ├── package.json
    ├── package-lock.json
    ├── serverInfo.json
    ├── src
    │   ├── Contacts.ts
    │   ├── IMAP.ts
    │   ├── main.ts
    │   ├── ServerInfo.ts
    │   └── SMTP.ts
    └── tsconfig.json
