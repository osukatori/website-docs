---
title: "Crystal bot commands"
old_id: 4
---
## **Main commands**

-   `!roll` – Returns any number from `0` to `100`
-   `!roll num` – Returns any number from `0` to `num`
-   `!help` – Gives you this documentation
-   `!stats [nickname] [mode]` – Gives you an stats for `<nickname>` on the `<mode>`. If two parameters are none, but this cannot be :). For example `!stats KotRik` or `!stats KotRik 2`  
    `!clantop [on/off]` – Turns clan top thing. This top replaces the country top.  
    `!flag [country code]` – Special thing for donors, changes your flag. (eg: `!flag jp` – sets up a Japanese flag. Flag codes are not difficult to search in google )

## **Tillerino-like commands**
Crystal has the similar command to the Tillerino. But, they are working faster because of  
implemented inside of a server core.

-   `/np` – shows pp for a beatmap (works only for osu!std)
-   `!with <mods>` - Shows you pp for a map for /np with mods, for example: NF, EZ, HD, HR, DT, HT, NC, FL, SO, RX, AP. *Don't use the space between mods!* (eg: `!with HDHR`)

## **Admin commands:**

-   `!system restart` – Restarts the server
-   `!system status` – Shows the system current status
-   `!system reload` – Reloads the system config file (RAP)
-   `!system maintenance on/off` – Turns “maintenance work” of Bancho
-   `!silence <username> <count> <unit (s/m/h/d)> <reason>` - User silence
-   `!removesilence <target>` - Removes the silence from a user
-   `!kick <username>` - Kicks the user from the server
-   `!ban <username>` - Death. Absolute BANHAMMER!
-   `!unban <username>` - Unbans the user.
-   `!restrict <username>` - Restricts the user
-   `!unrestrict <username>` - Removes restrict from the user.
-   `!crystal reconnect` – Crystal reconnect. This is needed when Crystal is not on a players list.
-   `!alert <message>` - Global message. As usual, stupid CM’s use it for a trolling
-   `!useralert <username> <message>` - User message, works like usual !alert but for an one player
-   `!rtx <username> <message>` - Shows a message to the entire game window.
-   `!kill <username>` - Kills user game
