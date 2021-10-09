# Dory Games
> **Dory Games is a powerful module that allows you to play games within Discord :)**

## **⚙️ Installation** 
```
npm i https://github.com/sludgepudge/doryGames.git
```


## **✨ Features**

- Super simple and easy to use.
- Beginner friendly.
- Easy to Implement.
- Supports Slash Commands.

## **📚 Usage**
```js
const { Snake } = require('dorygames')

new Snake({
  message: message,
  slash_command: false,
  embed: {
    title: 'Snake Game',
    color: '#5865F2',
    overTitle: 'Game Over',
  },
  snake: { head: '🟢', body: '🟩', tail: '🟢' },
  emojis: {
    board: '⬛', 
    food: '🍎',
    up: '⬆️', 
    right: '➡️',
    down: '⬇️',
    left: '⬅️',
  },
}).startGame()
```


## **✏️ Example**
### **Looking for Examples? click here:** [**Examples!**](https://discord-gamecord.js.org/docs/gamecord/master/general/welcome)
```js
const Discord = require('discord.js');
const client = new Discord.Client();
const { Snake } = require('dorygames');


client.on('messageCreate', async (message) => {
  if(message.content === '!snake') {
    new Snake({
      message: message,
      slash_command: false,
      embed: {
        title: 'Snake Game',
        color: '#5865F2',
        OverTitle: 'Game Over',
      },
      snake: { head: '🟢', body: '🟩', tail: '🟢' },
      emojis: {
        board: '⬛',
        food: '🍎',
        up: '⬆️', 
        down: '⬇️',
        right: '➡️',
        left: '⬅️',
      }
    }).startGame();
  }
});

client.login('YOUR_COOL_DISCORD_BOT_TOKEN');
```