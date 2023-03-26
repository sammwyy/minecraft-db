# ⛏️ Minecraft DB

JSON based Minecraft data for multipurpose.

## 📖 Index

- [Server Software](#server-software)

## 📦 Entities

### Server Software

List of software to host Java and Bedrock servers. Including mods, plugin support and proxies.

`GET` [data/servers.json](data/servers.json)

```jsonc
{
    // Software ID, example bukkit, paper, spigot, vanilla, etc...
    "{software:id}": {
        // Possible values: server, proxy, modded, bedrock, misc.
        "type": String,

        // Minecraft-like versions (1.19.3, 1.12.2, 1.8.8, etc)
        "versions": [ String ],

        // OPTIONAL: Jar url where you replace the {version} placeholder.
        "url": "",

        // OPTIONAL: urls map in case of being specific for each version.
        "resources": {
            "{version:id}": String
        },

        // OPTIONAL: In case the software needs a special installation.
        "installer": {
          "temp": Boolean, // Run installer jar in temporary folder.
          "execute": String, // Command in installer terminal.
          "archive": String, // Dir created by the installer where the server is located.
          "jar": String // Jar file to be executed.
        }
    }
}
```

## 🤝 Contributing

Contributions, issues and feature requests are welcome!
Feel free to check [issues page](https://github.com/sammwyy/minecraft-db/issues).

## ❤️ Show your support

Give a ⭐️ if this project helped you!

Or buy me a coffeelatte 🙌

[Ko-fi](https://ko-fi.com/sammwy) | [Patreon](https://patreon.com/sammwy)

## 📝 License

Copyright © 2023 [Sammwy](https://github.com/sammwyy).  
This project is [MIT](LICENSE) licensed.
