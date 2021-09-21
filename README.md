# MailBag

#### Technology Used
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

#### Requirements
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
In the <code>/server</code> directory run 
```npm install``` and then <br> 
```npm run dev``` to compile the TypeScript and launch the server 
