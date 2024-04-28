# DS4WEB
Embed a Nintendo DS emulator easily. (Embeddable version of [DeSmuME-wasm](https://github.com/44670/desmume-wasm/tree/master) and based on [desmond](https://github.com/js-emulators/desmond))

# Usage
```html
<html>
    <body>
        <div id="msg-layer" hidden="">
            <p id="msg-text"></p>
        </div>
        <DS4WEB-player id="player"></DS4WEB-player>
        <script src="path/to/DS4WEB.min.js"></script>
        <script>
            document.getElementById("player").loadURL("path/to/game.nds");
        </script>
    </body>
</html>
```
# Run function after load
To run a function after the file loads, you may attach a function as the second argument. You can also enable microphone using it.

# Enable microphone
To use the microphone, you have to use the "enableMicrophone" function inside of the callback function.
Here is an example:
```html
<!doctype html>
<html>
<body>
    <div id="msg-layer" hidden="">
        <p id="msg-text"></p>
    </div>
    <DS4WEB-player id="player"></DS4WEB-player>
    <script src="path/to/DS4WEB.min.js"></script>
    <script>
        var player = document.getElementById("player");
        player.loadURL("path/to/game.nds", () => {
            player.enableMicrophone();
        });
    </script>
</body>
</html>
```

# How to save
Just save in the game and wait a few seconds. An auto-saving banner will appear, and your saved data will automatically be stored in the web app's local storage.