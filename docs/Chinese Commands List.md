贊助原作者 => patreon: https://patreon.com/nadekobot paypal: https://paypal.me/Kwoth

## 目錄
- [幫助](#幫助)
- [管理](#管理)
- [權限](#權限)
- [音樂](#音樂)
- [小遊戲](#小遊戲)
- [賭博](#賭博)
- [寶可夢](#寶可夢)
- [搜尋](#搜尋)
- [小工具](#小工具)
- [自定義回覆](#自定義回覆)
- [Xp](#xp)
- [NSFW](#nsfw)


### 幫助
指令與簡寫 | 說明 | 用法
----------------|--------------|-------
`.modules` `.mdls` | 列出所有模組。 | `.modules`
`.commands` `.cmds` | 列出所有特定模組的指令，你可以指定模組的全名或名稱的前幾個字母。 | `.commands Administration` 或 `.cmds Admin`
`.help` `.h` | 它會將幫助頁面的連結私訊給你，或當你選擇特定指令時，將該指令的資訊回傳給你。 | `.h .cmds` 或 `.h`
`.hgit` | 生成 commandlist.md 檔案。**僅限Bot擁有者** | `.hgit`
`.readme` `.guide` | 在頻道內發送Bot簡介與教學連結。 | `.readme` 或 `.guide`
`.donate` | 顯示關於贊助NadekoBot的資訊。 | `.donate`

###### [回目錄](#目錄)

### 管理
指令與簡寫 | 說明 | 用法
----------------|--------------|-------
`.delmsgoncmd` | 開啟/關閉自動刪除成功執行的指令，以防止洗頻。 **Bot需要`管理員`權限** | `.delmsgoncmd`
`.setrole` `.sr` | 給予一名玩家指定的身分組。 **Bot需要`管理身分組`權限** | `.sr @User Guest`
`.removerole` `.rr` | 移除一名玩家指定的身分組。 **Bot需要`管理身分組`權限** | `.rr @User Admin`
`.renamerole` `.renr` | 重新命名身分組。重新命名的身分組權限必須低於Bot所擁有的最高身分組。 **Bot需要`管理身分組`權限** | `.renr "First role" SecondRole`
`.removeallroles` `.rar` | 移除指定玩家的所有身分組。 **Bot需要`管理身分組`權限** | `.rar @User`
`.createrole` `.cr` | 以使用者提供的名稱創建一個身分組。 **Bot需要`管理身分組`權限** | `.cr Awesome Role`
`.rolehoist` `.rh` | 設定指定身分組成員是否要與線上成員分開顯示。 **Bot需要`管理身分組`權限** | `.rh Guests true` 或 `.rh "Space Wizards" true`
`.rolecolor` `.roleclr` | 將選定身分組的顏色設置為使用者提供的十六進位色碼或0-255的RGB色碼。 **Bot需要`管理身分組`權限** | `.roleclr Admin 255 200 100` 或 `.roleclr Admin ffba55`
`.deafen` `.deaf` | 伺服器端拒聽特定成員(可選擇複數成員)。 **Bot需要`拒聽成員`權限** | `.deaf "@Someguy"` 或 `.deaf "@Someguy" "@Someguy"`
`.undeafen` `.undef` | 解除伺服器端拒聽特定成員(可選擇複數成員)。 **Bot需要`拒聽成員`權限** | `.undef "@Someguy"` 或 `.undef "@Someguy" "@Someguy"`
`.delvoichanl` `.dvch` | 刪除指定的語音頻道。 **Bot需要`管理頻道`權限** | `.dvch VoiceChannelName`
`.creatvoichanl` `.cvch` | 以使用者提供的名稱創建一個語音頻道。 **Bot需要`管理頻道`權限** | `.cvch VoiceChannelName`
`.deltxtchanl` `.dtch` | 刪除指定的文字頻道。 **Bot需要`管理頻道`權限** | `.dtch TextChannelName`
`.creatxtchanl` `.ctch` | 以使用者提供的名稱創建一個文字頻道。 **Bot需要`管理頻道`權限** | `.ctch TextChannelName`
`.settopic` `.st` | 設置目前所在頻道的主題。 **Bot需要`管理頻道`權限** | `.st My new topic`
`.setchanlname` `.schn` | 更改目前所在頻道的名稱。 **Bot需要`管理頻道`權限** | `.schn NewName`
`.mentionrole` `.menro` | 通知特定身分組內的所有成員(可選擇複數身分組，以','分隔不同的身分組)。 **Bot需要`通知所有人`權限** | `.menro RoleName`
`.donators` | 列出所有可愛的贊助者。 | `.donators`
`.donadd` | 將一名贊助者添加到資料庫。 **僅限Bot擁有者** | `.donadd Donate Amount`
`.autoassignrole` `.aar` | 自動給予每個新加入的用戶選定的身分組。 **Bot需要`管理身分組`權限** | `.aar` to disable, `.aar Role Name` to enable
`.gvc` | Toggles game voice channel feature in the voice channel you're currently in. Users who join the game voice channel will get automatically redirected to the voice channel with the name of their current game, if it exists. Can't move users to channels that the bot has no connect permission for. One per server. **Bot需要`管理員`權限** | `.gvc`
`.languageset` `.langset` | 設定Bot在當前伺服器上所使用的語言。如果Bot欲顯示的訊息已被翻譯成該語言，則會使用該語言來表示，反之則使用英語。若輸入`default`將重設為預設值。不提供參數則查看當前所設置的語言。 | `.langset de-DE ` 或 `.langset default`
`.langsetdefault` `.langsetd` | Sets the bot's default response language. All servers which use a default locale will use this one. Setting to `default` will use the host's current culture. Provide no arguments to see currently set language.  | `.langsetd en-US` 或 `.langsetd default`
`.languageslist` `.langli` | 列出可使用的語言列表。 | `.langli`
`.logserver` | 開啟或關閉紀錄伺服器所有事件，開啟後會將所有事件紀錄到當前文字頻道。 **Bot需要`管理員`權限** **僅限Bot擁有者** | `.logserver enable` 或 `.logserver disable`
`.logignore` | Toggles whether the `.logserver` command ignores this channel. Useful if you have hidden admin channel and public log channel. **Bot需要`管理員`權限** **僅限Bot擁有者** | `.logignore`
`.logevents` | 列出您可以使用`.log`紀錄的所有事件類型。 **Bot需要`管理員`權限** **僅限Bot擁有者** | `.logevents`
`.log` | Toggles logging event. Disables it if it is active anywhere on the server. Enables if it isn't active. Use `.logevents` to see a list of all events you can subscribe to. **Bot需要`管理員`權限** **僅限Bot擁有者** | `.log userpresence` 或 `.log userbanned`
`.migratedata` | Migrate data from old bot configuration **僅限Bot擁有者** | `.migratedata`
`.setmuterole` | Sets a name of the role which will be assigned to people who should be muted. Default is nadeko-mute. **Bot需要`管理身分組`權限** | `.setmuterole Silenced`
`.mute` | Mutes a mentioned user both from speaking and chatting. You can also specify time in minutes (up to 1440) for how long the user should be muted. **Bot需要`管理身分組`權限** **Bot需要`靜音成員`權限** | `.mute @Someone` 或 `.mute 30 @Someone`
`.unmute` | Unmutes a mentioned user previously muted with `.mute` command. **Bot需要`管理身分組`權限** **Bot需要`靜音成員`權限** | `.unmute @Someone`
`.chatmute` | Prevents a mentioned user from chatting in text channels. **Bot需要`管理身分組`權限** | `.chatmute @Someone`
`.chatunmute` | Removes a mute role previously set on a mentioned user with `.chatmute` which prevented him from chatting in text channels. **Bot需要`管理身分組`權限** | `.chatunmute @Someone`
`.voicemute` | Prevents a mentioned user from speaking in voice channels. **Bot需要`靜音成員`權限** | `.voicemute @Someone`
`.voiceunmute` | Gives a previously voice-muted user a permission to speak. **Bot需要`靜音成員`權限** | `.voiceunmute @Someguy`
`.rotateplaying` `.ropl` | Toggles rotation of playing status of the dynamic strings you previously specified. **僅限Bot擁有者** | `.ropl`
`.addplaying` `.adpl` | Adds a specified string to the list of playing strings to rotate. Supported placeholders: `%servers%`, `%users%`, `%playing%`, `%queued%`, `%time%`, `%shardid%`, `%shardcount%`, `%shardguilds%`. **僅限Bot擁有者** | `.adpl`
`.listplaying` `.lipl` | Lists all playing statuses with their corresponding number. **僅限Bot擁有者** | `.lipl`
`.removeplaying` `.rmpl` `.repl` | Removes a playing string on a given number. **僅限Bot擁有者** | `.rmpl`
`.prefix` | Sets this server's prefix for all bot commands. Provide no arguments to see the current server prefix.  | `.prefix +`
`.defprefix` | Sets bot's default prefix for all bot commands. Provide no arguments to see the current default prefix. This will not change this server's current prefix. **Bot owner only** | `.defprefix +`
`.antiraid` | Sets an anti-raid protection on the server. First argument is number of people which will trigger the protection. Second one is a time interval in which that number of people needs to join in order to trigger the protection, and third argument is punishment for those people (Kick, Ban, Mute) **Bot需要`管理員`權限** | `.antiraid 5 20 Kick`
`.antispam` | Stops people from repeating same message X times in a row. You can specify to either mute, kick or ban the offenders. Max message count is 10. **Bot需要`管理員`權限** | `.antispam 3 Mute` 或 `.antispam 4 Kick` 或 `.antispam 6 Ban`
`.antispamignore` | Toggles whether antispam ignores current channel. Antispam must be enabled. **Bot需要`管理員`權限** | `.antispamignore`
`.antilist` `.antilst` | Shows currently enabled protection features.  | `.antilist`
`.prune` `.clear` | `.prune` removes all Nadeko's messages in the last 100 messages. `.prune X` removes last `X` number of messages from the channel (up to 100). `.prune @Someone` removes all Someone's messages in the last 100 messages. `.prune @Someone X` removes last `X` number of 'Someone's' messages in the channel.  | `.prune` 或 `.prune 5` 或 `.prune @Someone` 或 `.prune @Someone X`
`.slowmode` | Toggles slowmode. Disable by specifying no parameters. To enable, specify a number of messages each user can send, and an interval in seconds. For example 1 message every 5 seconds. **Bot需要`管理訊息`權限** | `.slowmode 1 5` 或 `.slowmode`
`.slowmodewl` | Ignores a role or a user from the slowmode feature. **Bot需要`管理訊息`權限** | `.slowmodewl SomeRole` 或 `.slowmodewl AdminDude`
`.adsarm` | Toggles the automatic deletion of confirmations for `.iam` and `.iamn` commands. **Bot需要`管理訊息`權限** | `.adsarm`
`.asar` | Adds a role to the list of self-assignable roles. **Bot需要`管理身分組`權限** | `.asar Gamer`
`.rsar` | Removes a specified role from the list of self-assignable roles. **Bot需要`管理身分組`權限** | `.rsar`
`.lsar` | Lists all self-assignable roles.  | `.lsar`
`.togglexclsar` `.tesar` | Toggles whether the self-assigned roles are exclusive. (So that any person can have only one of the self assignable roles) **Bot需要`管理身分組`權限** | `.tesar`
`.iam` | Adds a role to you that you choose. Role must be on a list of self-assignable roles.  | `.iam Gamer`
`.iamnot` `.iamn` | Removes a specified role from you. Role must be on a list of self-assignable roles.  | `.iamn Gamer`
`.scadd` | Adds a command to the list of commands which will be executed automatically in the current channel, in the order they were added in, by the bot when it startups up. **僅限Bot擁有者** | `.scadd .stats`
`.sclist` | Lists all startup commands in the order they will be executed in. **僅限Bot擁有者** | `.sclist`
`.wait` | Used only as a startup command. Waits a certain number of miliseconds before continuing the execution of the following startup commands. **僅限Bot擁有者** | `.wait 3000`
`.scrm` | Removes a startup command with the provided command text. **僅限Bot擁有者** | `.scrm .stats`
`.scclr` | Removes all startup commands. **僅限Bot擁有者** | `.scclr`
`.fwmsgs` | Toggles forwarding of non-command messages sent to bot's DM to the bot owners **僅限Bot擁有者** | `.fwmsgs`
`.fwtoall` | Toggles whether messages will be forwarded to all bot owners or only to the first one specified in the credentials.json file **僅限Bot擁有者** | `.fwtoall`
`.leave` | Makes Nadeko leave the server. Either server name or server ID is required. **僅限Bot擁有者** | `.leave 123123123331`
`.die` | Shuts the bot down. **僅限Bot擁有者** | `.die`
`.setname` `.newnm` | Gives the bot a new name. **僅限Bot擁有者** | `.newnm BotName`
`.setnick` | Changes the nickname of the bot on this server. You can also target other users to change their nickname. **Bot需要`更改暱稱`權限** | `.setnick BotNickname` 或 `.setnick @SomeUser New Nickname`
`.setstatus` | Sets the bot's status. (Online/Idle/Dnd/Invisible) **僅限Bot擁有者** | `.setstatus Idle`
`.setavatar` `.setav` | Sets a new avatar image for the NadekoBot. Argument is a direct link to an image. **僅限Bot擁有者** | `.setav http://i.imgur.com/xTG3a1I.jpg`
`.setgame` | Sets the bots game. **僅限Bot擁有者** | `.setgame with snakes`
`.setstream` | Sets the bots stream. First argument is the twitch link, second argument is stream name. **僅限Bot擁有者** | `.setstream TWITCHLINK Hello`
`.send` | Sends a message to someone on a different server through the bot.  Separate server and channel/user ids with `|` and prefix the channel id with `c:` and the user id with `u:`. **僅限Bot擁有者** | `.send serverid|c:channelid message` 或 `.send serverid|u:userid message`
`.reloadimages` | Reloads images bot is using. Safe to use even when bot is being used heavily. **僅限Bot擁有者** | `.reloadimages`
`.greetdel` `.grdel` | Sets the time it takes (in seconds) for greet messages to be auto-deleted. Set it to 0 to disable automatic deletion. **Bot需要`管理伺服器`權限** | `.greetdel 0` 或 `.greetdel 30`
`.greet` | Toggles anouncements on the current channel when someone joins the server. **Bot需要`管理伺服器`權限** | `.greet`
`.greetmsg` | Sets a new join announcement message which will be shown in the server's channel. Type `%user%` if you want to mention the new member. Using it with no message will show the current greet message. You can use embed json from <http://nadekobot.me/embedbuilder/> instead of a regular text, if you want the message to be embedded. **Bot需要`管理伺服器`權限** | `.greetmsg Welcome, %user%.`
`.greetdm` | Toggles whether the greet messages will be sent in a DM (This is separate from greet - you can have both, any or neither enabled). **Bot需要`管理伺服器`權限** | `.greetdm`
`.greetdmmsg` | Sets a new join announcement message which will be sent to the user who joined. Type `%user%` if you want to mention the new member. Using it with no message will show the current DM greet message. You can use embed json from <http://nadekobot.me/embedbuilder/> instead of a regular text, if you want the message to be embedded. **Bot需要`管理伺服器`權限** | `.greetdmmsg Welcome to the server, %user%`
`.bye` | Toggles anouncements on the current channel when someone leaves the server. **Bot需要`管理伺服器`權限** | `.bye`
`.byemsg` | Sets a new leave announcement message. Type `%user%` if you want to show the name the user who left. Type `%id%` to show id. Using this command with no message will show the current bye message. You can use embed json from <http://nadekobot.me/embedbuilder/> instead of a regular text, if you want the message to be embedded. **Bot需要`管理伺服器`權限** | `.byemsg %user% has left.`
`.byedel` | Sets the time it takes (in seconds) for bye messages to be auto-deleted. Set it to `0` to disable automatic deletion. **Bot需要`管理伺服器`權限** | `.byedel 0` 或 `.byedel 30`
`.timezones` | Lists all timezones available on the system to be used with `.timezone`.  | `.timezones`
`.timezone` | Sets this guilds timezone. This affects bot's time output in this server (logs, etc..)  | `.timezone` 或 `.timezone GMT Standard Time`
`.warn` | Warns a user. **Bot需要`封鎖成員`權限** | `.warn @b1nzy Very rude person`
`.warnlog` | See a list of warnings of a certain user. **Bot需要`封鎖成員`權限** | `.warnlog @b1nzy`
`.warnlogall` | See a list of all warnings on the server. 15 users per page. **Bot需要`封鎖成員`權限** | `.warnlogall` 或 `.warnlogall 2`
`.warnclear` `.warnc` | Clears all warnings from a certain user. **Bot需要`封鎖成員`權限** | `.warnclear @PoorDude`
`.warnpunish` `.warnp` | Sets a punishment for a certain number of warnings. Provide no punishment to remove. **Bot需要`封鎖成員`權限** | `.warnpunish 5 Ban` 或 `.warnpunish 3`
`.warnpunishlist` `.warnpl` | Lists punishments for warnings.  | `.warnpunishlist`
`.ban` `.b` | Bans a user by ID or name with an optional message. **Bot需要`封鎖成員`權限** | `.b "@some Guy" Your behaviour is toxic.`
`.unban` | Unbans a user with the provided user#discrim or id. **Bot需要`封鎖成員`權限** | `.unban kwoth#1234` 或 `.unban 123123123`
`.softban` `.sb` | Bans and then unbans a user by ID or name with an optional message. **Bot需要`踢除成員`權限** **Bot需要`管理訊息`權限** | `.sb "@some Guy" Your behaviour is toxic.`
`.kick` `.k` | Kicks a mentioned user. **Bot需要`踢除成員`權限** | `.k "@some Guy" Your behaviour is toxic.`
`.vcrole` | Sets or resets a role which will be given to users who join the voice channel you're in when you run this command. Provide no role name to disable. You must be in a voice channel to run this command. **Bot需要`管理身分組`權限** **Bot需要`管理頻道`權限** | `.vcrole SomeRole` 或 `.vcrole`
`.vcrolelist` | Shows a list of currently set voice channel roles.  | `.vcrolelist`
`.voice+text` `.v+t` | Creates a text channel for each voice channel only users in that voice channel can see. If you are server owner, keep in mind you will see them all the time regardless. **Bot需要`管理身分組`權限** **Bot需要`管理頻道`權限** | `.v+t`
`.cleanvplust` `.cv+t` | Deletes all text channels ending in `-voice` for which voicechannels are not found. Use at your own risk. **Bot需要`管理頻道`權限** **Bot需要`管理身分組`權限** | `.cleanv+t`

###### [回目錄](#目錄)

### 權限
指令與簡寫 | 說明 | 用法
----------------|--------------|-------
`.verbose` `.v` | Sets whether to show when a command/module is blocked.  | `.verbose true`
`.permrole` `.pr` | Sets a role which can change permissions. Supply no parameters to see the current one. Default is 'Nadeko'.  | `.pr role`
`.listperms` `.lp` | Lists whole permission chain with their indexes. You can specify an optional page number if there are a lot of permissions.  | `.lp` 或 `.lp 3`
`.removeperm` `.rp` | Removes a permission from a given position in the Permissions list.  | `.rp 1`
`.moveperm` `.mp` | Moves permission from one position to another in the Permissions list.  | `.mp 2 4`
`.srvrcmd` `.sc` | Sets a command's permission at the server level.  | `.sc "command name" disable`
`.srvrmdl` `.sm` | Sets a module's permission at the server level.  | `.sm ModuleName enable`
`.usrcmd` `.uc` | Sets a command's permission at the user level.  | `.uc "command name" enable SomeUsername`
`.usrmdl` `.um` | Sets a module's permission at the user level.  | `.um ModuleName enable SomeUsername`
`.rolecmd` `.rc` | Sets a command's permission at the role level.  | `.rc "command name" disable MyRole`
`.rolemdl` `.rm` | Sets a module's permission at the role level.  | `.rm ModuleName enable MyRole`
`.chnlcmd` `.cc` | Sets a command's permission at the channel level.  | `.cc "command name" enable SomeChannel`
`.chnlmdl` `.cm` | Sets a module's permission at the channel level.  | `.cm ModuleName enable SomeChannel`
`.allchnlmdls` `.acm` | Enable or disable all modules in a specified channel.  | `.acm enable #SomeChannel`
`.allrolemdls` `.arm` | Enable or disable all modules for a specific role.  | `.arm [enable/disable] MyRole`
`.allusrmdls` `.aum` | Enable or disable all modules for a specific user.  | `.aum enable @someone`
`.allsrvrmdls` `.asm` | Enable or disable all modules for your server.  | `.asm [enable/disable]`
`.ubl` | Either [add]s or [rem]oves a user specified by a Mention or an ID from a blacklist. **僅限Bot擁有者** | `.ubl add @SomeUser` 或 `.ubl rem 12312312313`
`.cbl` | Either [add]s or [rem]oves a channel specified by an ID from a blacklist. **僅限Bot擁有者** | `.cbl rem 12312312312`
`.sbl` | Either [add]s or [rem]oves a server specified by a Name or an ID from a blacklist. **僅限Bot擁有者** | `.sbl add 12312321312` 或 `.sbl rem SomeTrashServer`
`.cmdcooldown` `.cmdcd` | Sets a cooldown per user for a command. Set it to 0 to remove the cooldown.  | `.cmdcd "some cmd" 5`
`.allcmdcooldowns` `.acmdcds` | Shows a list of all commands and their respective cooldowns.  | `.acmdcds`
`.srvrfilterinv` `.sfi` | Toggles automatic deletion of invites posted in the server. Does not affect the Bot Owner.  | `.sfi`
`.chnlfilterinv` `.cfi` | Toggles automatic deletion of invites posted in the channel. Does not negate the `.srvrfilterinv` enabled setting. Does not affect the Bot Owner.  | `.cfi`
`.srvrfilterwords` `.sfw` | Toggles automatic deletion of messages containing filtered words on the server. Does not affect the Bot Owner.  | `.sfw`
`.chnlfilterwords` `.cfw` | Toggles automatic deletion of messages containing filtered words on the channel. Does not negate the `.srvrfilterwords` enabled setting. Does not affect the Bot Owner.  | `.cfw`
`.fw` | Adds or removes (if it exists) a word from the list of filtered words. Use`.sfw` 或 `.cfw` to toggle filtering.  | `.fw poop`
`.lstfilterwords` `.lfw` | Shows a list of filtered words.  | `.lfw`
`.listglobalperms` `.lgp` | Lists global permissions set by the bot owner. **僅限Bot擁有者** | `.lgp`
`.globalmodule` `.gmod` | Toggles whether a module can be used on any server. **僅限Bot擁有者** | `.gmod nsfw`
`.globalcommand` `.gcmd` | Toggles whether a command can be used on any server. **僅限Bot擁有者** | `.gcmd .stats`
`.resetperms` | 重設這個伺服器上的權限模組至預設值。 **Bot需要`管理員`權限** | `.resetperms`
`.resetglobalperms` | 重設所有伺服器上的權限模組至預設值。 **僅限Bot擁有者** | `.resetglobalperms`

###### [回目錄](#目錄)

### 音樂
指令與簡寫 | 說明 | 用法
----------------|--------------|-------
`.play` `.start` | 如果沒有指定參數，則作為`.next 1`命令。如果指定一首歌曲之編號，將跳轉至該歌曲。如果指定搜索參數，則作為`.q`命令。  | `.play` 或 `.play 5` 或 `.play Dream Of Venice`
`.queue` `.q` `.yq` | 以關鍵字、影片ID或影片網址點播一首歌，Bot將加入您所在的語音頻道。 **你必須在一個語音頻道內** | `.q Dream Of Venice`
`.queuenext` `.qn` | 與`.queue`相似，點播的歌曲將於目前的歌曲結束後播放(插播)。 **你必須在一個語音頻道內** | `.qn Dream Of Venice`
`.queuesearch` `.qs` `.yqs` | 使用關鍵字搜索前5個YouTube搜尋結果，並輸入歌曲編號以點播該歌曲。Bot將加入您所在的語音頻道。 **你必須在一個語音頻道內** | `.qs Dream Of Venice`
`.listqueue` `.lq` | 顯示已點播歌曲列表，每頁10條，預設頁數為1 (歌曲編號請使用該命令查詢)。 | `.lq` 或 `.lq 2`
`.next` `.n` | 播放點播列表中的下一首歌曲，你必須與Bot處於同一個語音頻道；你也可以同時跳過多首歌曲，若以啟用單曲循環`.rcs`或所有歌曲循環`.rpl`，歌曲將不會被重新排列。  | `.n` 或 `.n 5`
`.stop` `.s` | 停止播放音樂並保留當前以點播歌曲(未播放完畢之歌曲將一同保留)。機器人將留在語音頻道內。 | `.s`
`.destroy` `.d` | 停止播放歌曲並使Bot離開當前語音頻道(可能會發生奇怪的事情)。 | `.d`
`.pause` `.p` | 暫停或取消暫停播放歌曲。 | `.p`
`.volume` `.vol` | 設定播放音量(0-100%)。 | `.vol 50`
`.defvol` `.dv` | 設定音樂播放器的預設音量(0-100)；重新啟動Bot後將使用當前預設音量進行播放。 | `.dv 80`
`.songremove` `.srm` | 以點播列表之編號刪除以點播歌曲，或使用"all"以刪除所有歌曲並重置歌曲索引。 | `.srm 5`
`.playlists` `.pls` | 列出已儲存的播放清單，每頁20條，預設頁數為0。 | `.pls 1`
`.deleteplaylist` `.delpls` | 刪除一個已儲存的播放清單，只有在你是該播放清單的製作者或Bot管理員的情況下才可使用。 | `.delpls animu-5`
`.save` | 取個名字將目前的點播清單儲存起來，名稱必須小於20個字元且不得包含'-'。 | `.save classical1`
`.load` | 使用清單編號來讀取並播放一個已儲存的播放清單；使用`.pls`可列出所有已保存的播放清單與其編號；使用`.save`可儲存新的播放清單。 | `.load 5`
`.fairplay` `.fp` | 開啟/關閉公平播放。啟用後，Bot將優先播放"最近沒有點播歌曲"的用戶所點播的歌，而不是依照點播列表的排序播放。 | `.fp`
`.songautodelete` `.sad` | 切換點播歌曲是否應該在完成播放後從點播列表內刪除。 | `.sad`
`.soundcloudqueue` `.sq` | 以關鍵字搜尋並點播一首soundcloud上的音樂，Bot會進入你當前所在語音頻道。你必須在一個語音頻道內。 **你必須在一個語音頻道內** | `.sq Dream Of Venice`
`.soundcloudpl` `.scpl` | 使用連結網址點播soundcloud上的播放清單。 | `.scpl soundcloudseturl`
`.nowplaying` `.np` | 顯示目前播放中的歌曲資訊。 | `.np`
`.shuffle` `.sh` `.plsh` | 隨機排列點播列表中的歌曲。 | `.plsh`
`.playlist` `.pl` | 以搜尋字串或網址點播最多500首歌曲的播放清單。 | `.pl <youtube_playlist_link>`
`.radio` `.ra` | 使用連結網址點播線上電台，可用的電台格式有.mp3、.m3u、.pls、.asx、.xspf (教學影片:https://streamable.com/al54)。 | `.ra radio link here`
`.local` `.lo` | 點播開設者電腦內的一首歌曲。僅限Bot擁有者 **僅限Bot擁有者** | `.lo C:/music/mysong.mp3`
`.localplaylst` `.lopl` | 點播Bot開設者電腦裡某資料夾內的所有歌曲。 **僅限Bot擁有者** | `.lopl C:/music/classical`
`.move` `.mv` | 將Bot移動至你目前所在的頻道。 (僅限音樂正在播放時有效)  | `.mv`
`.movesong` `.ms` | 更改點播列表的播放順序。 | `.ms 5>3`
`.setmaxqueue` `.smq` | 設定點播歌曲量最大上限，0或無參數則為沒有上限。 | `.smq 50` 或 `.smq`
`.setmaxplaytime` `.smp` | 設置每首歌曲的最大播放秒數(秒數必須大於14)；設為0則沒有秒數限制。 | `.smp 0` 或 `.smp 270`
`.reptcursong` `.rcs` | 開啟/關閉單曲循環播放。 | `.rcs`
`.rpeatplaylst` `.rpl` | 開啟/關閉所有歌曲循環播放 (當一首歌曲播放完畢時，自動重新點播該歌曲至點播列表後)。 | `.rpl`
`.autoplay` `.ap` | 開啟/關閉自動播放 - 歌曲播放完畢後自動點播相關影片。(僅適用於播放Youtube歌曲，且點播列表無任何歌曲時才會作用) | `.ap`
`.setmusicchannel` `.smch` | 將目前文字頻道設為音樂訊息輸出頻道。這將輸出播放、結束、暫停和刪除的音樂訊息到當前文字頻道。 **Bot需要`管理訊息`權限** | `.smch`

###### [回目錄](#目錄)

### 小遊戲
指令與簡寫 | 說明 | 用法
----------------|--------------|-------
`.choose` | 替您從列表中選擇一個答案。 | `.choose 起床;睡;睡更多`
`.8ball` | 問8ball一個是非題yes/no問題(其答案非常多樣化(例：當然, 也許不...)且皆無翻譯，請慎用)。 | `.8ball Is b1nzy a nice guy?`
`.rps` | Play a game of Rocket-Paperclip-Scissors with Nadeko.  | `.rps scissors`
`.rategirl` | Use the universal hot-crazy wife zone matrix to determine the girl's worth. It is everything young men need to know about women. At any moment in time, any woman you have previously located on this chart can vanish from that location and appear anywhere else on the chart.  | `.rategirl @SomeGurl`
`.linux` | Prints a customizable Linux interjection  | `.linux Spyware Windows`
`.leet` | Converts a text to leetspeak with 6 (1-6) severity levels  | `.leet 3 Hello`
`.acrophobia` `.acro` | Starts an Acrophobia game. Second argument is optional round length in seconds. (default is 60)  | `.acro` 或 `.acro 30`
`.cleverbot` | Toggles cleverbot session. When enabled, the bot will reply to messages starting with bot mention in the server. Custom reactions starting with %mention% won't work if cleverbot is enabled. **Bot需要`管理訊息`權限** | `.cleverbot`
`.connect4` `.con4` | Creates or joins an existing connect4 game. 2 players are required for the game. Objective of the game is to get 4 of your pieces next to each other in a vertical, horizontal or diagonal line.  | `.connect4`
`.hangmanlist` | Shows a list of hangman term types. | `. hangmanlist`
`.hangman` | Starts a game of hangman in the channel. Use `.hangmanlist` to see a list of available term types. Defaults to 'all'.  | `.hangman` 或 `.hangman movies`
`.hangmanstop` | Stops the active hangman game on this channel if it exists.  | `.hangmanstop`
`.nunchi` | Creates or joins an existing nunchi game. Users have to count up by 1 from the starting number shown by the bot. If someone makes a mistake (types an incorrent number, or repeats the same number) they are out of the game and a new round starts without them.  Minimum 3 users required.  | `.nunchi`
`.pick` | Picks the currency planted in this channel. 60 seconds cooldown.  | `.pick`
`.plant` | Spend an amount of currency to plant it in this channel. Default is 1. (If bot is restarted or crashes, the currency will be lost)  | `.plant` 或 `.plant 5`
`.gencurrency` `.gc` | Toggles currency generation on this channel. Every posted message will have chance to spawn currency. Chance is specified by the Bot Owner. (default is 2%) **Bot需要`管理訊息`權限** | `.gc`
`.poll` `.ppoll` | Creates a public poll which requires users to type a number of the voting option in the channel command is ran in. **Bot需要`管理訊息`權限** | `.ppoll Question?;Answer1;Answ 2;A_3`
`.pollstats` | Shows the poll results without stopping the poll on this server. **Bot需要`管理訊息`權限** | `.pollstats`
`.pollend` | Stops active poll on this server and prints the results in this channel. **Bot需要`管理訊息`權限** | `.pollend`
`.typestart` | Starts a typing contest.  | `.typestart`
`.typestop` | Stops a typing contest on the current channel.  | `.typestop`
`.typeadd` | Adds a new article to the typing contest. **僅限Bot擁有者** | `.typeadd wordswords`
`.typelist` | Lists added typing articles with their IDs. 15 per page.  | `.typelist` 或 `.typelist 3`
`.typedel` | Deletes a typing article given the ID. **僅限Bot擁有者** | `.typedel 3`
`.tictactoe` `.ttt` | Starts a game of tic tac toe. Another user must run the command in the same channel in order to accept the challenge. Use numbers 1-9 to play. 15 seconds per move.  | .ttt
`.trivia` `.t` | Starts a game of trivia. You can add `nohint` to prevent hints. First player to get to 10 points wins by default. You can specify a different number. 30 seconds per question.  | `.t` 或 `.t 5 nohint`
`.tl` | Shows a current trivia leaderboard.  | `.tl`
`.tq` | Quits current trivia after current question.  | `.tq`

###### [回目錄](#目錄)

### 賭博
指令與簡寫 | 說明 | 用法
----------------|--------------|-------
`.raffle` | 從線上成員(身分組)中隨機抽出一名成員並顯示其名稱與ID。 | `.raffle` 或 `.raffle RoleName`
`.$` `currency` `.$$` `.$$` `cash` `cur` | 查看自己或他人目前擁有多少花幣 (預設為查看自己)。 | `.$` 或 `.$ @SomeGuy`
`.give` | 給予他人花幣。 | `.give 1 @SomeGuy`
`.award` | 給予某位成員一定數量的貨幣。您還可以指定一個身分組，已將貨幣贈與該身分組中的所有成員。 **僅限Bot擁有者** | `.award 100 @person` 或 `.award 5 Role Of Gamblers`
`.take` | 取走某位成員一定數量的貨幣。 **僅限Bot擁有者** | `.take 1 @someguy`
`.betroll` `.br` | 投注一定數量的貨幣並擲骰子。骰子點數超過66將會有2倍的獎勵、超過90會有4倍、100則會有10倍 | `.br 5`
`.leaderboard` `.lb` | 顯示機器人使用者的貨幣排行榜。 | `.lb`
`.race` | 開始一場新的動物賽跑(該比賽並非使用者控制，而是隨機前進；一種碰運氣的遊戲)。 | `.race`
`.joinrace` `.jr` | 加入一場新的比賽，您可以指定下注金額(可選)。如果您獲勝了，將得到**下注金額x(參與玩家數-1)**。 | `.jr` 或 `.jr 5`
`.startevent` | 開始一個貨幣贈送活動。目前僅可使用`reaction`和`sneakygamestatus`。 **僅限Bot擁有者** | `.startevent reaction`
`.roll` | Rolls 0-100. If you supply a number `X` it rolls up to 30 normal dice. If you split 2 numbers with letter `d` (`xdy`) it will roll `X` dice from 1 to `y`. `Y` can be a letter 'F' if you want to roll fate dice instead of dnd.  | `.roll` 或 `.roll 7` 或 `.roll 3d5` 或 `.roll 5dF`
`.rolluo` | Rolls `X` normal dice (up to 30) unordered. If you split 2 numbers with letter `d` (`xdy`) it will roll `X` dice from 1 to `y`.  | `.rolluo` 或 `.rolluo 7` 或 `.rolluo 3d5`
`.nroll` | Rolls in a given range.  | `.nroll 5` (rolls 0-5) or `.nroll 5-15`
`.draw` | Draws a card from the deck.If you supply number X, she draws up to 5 cards from the deck.  | `.draw` 或 `.draw 5`
`.drawnew` | Draws a card from the NEW deck of cards. You can draw up to 10 cards by supplying a number of cards to draw.  | `.drawnew` 或 `.drawnew 5`
`.deckshuffle` `.dsh` | Reshuffles all cards back into the deck.  | `.dsh`
`.flip` | 翻硬幣 - 人頭(heads)或字(tails)，並顯示其圖像。 | `.flip` 或 `.flip 3`
`.betflip` `.bf` | 翻硬幣並猜其結果，人頭(heads)或字(tails)。猜中後將獎勵你**下注金額x1.95(四捨五入)**。機器人擁有者可更改乘數。 | `.bf 5 heads` 或 `.bf 3 t`
`.shop` | 列出這個伺服器上的管理員商店(該意思為**管理員開設的商店**，而不是**僅限管理員使用的商店**)。 | `.shop` 或 `.shop 2`
`.buy` | Buys an item from the shop on a given index. If buying items, make sure that the bot can DM you.  | `.buy 2`
`.shopadd` | Adds an item to the shop by specifying type price and name. Available types are role and list. **Bot需要`管理員`權限** | `.shopadd role 1000 Rich`
`.shoplistadd` | Adds an item to the list of items for sale in the shop entry given the index. You usually want to run this command in the secret channel, so that the unique items are not leaked. **Bot需要`管理員`權限** | `.shoplistadd 1 Uni-que-Steam-Key`
`.shoprem` `.shoprm` | Removes an item from the shop by its ID. **Bot需要`管理員`權限** | `.shoprm 1`
`.slotstats` | 顯示此機器人的吃角子老虎機統計資訊。 **僅限Bot擁有者** | `.slotstats`
`.slottest` | Tests to see how much slots payout for X number of plays. **僅限Bot擁有者** | `.slottest 1000`
`.slot` | 玩吃角子老虎。最大下注金額為**9999**，每位使用者有1.5秒的冷卻時間。 | `.slot 5`
`.claimwaifu` `.claim` | Claim a waifu for yourself by spending currency.  You must spend at least 10% more than her current value unless she set `.affinity` towards you.  | `.claim 50 @Himesama`
`.divorce` | Releases your claim on a specific waifu. You will get some of the money you've spent back unless that waifu has an affinity towards you. 6 hours cooldown.  | `.divorce @CheatingSloot`
`.affinity` | Sets your affinity towards someone you want to be claimed by. Setting affinity will reduce their `.claim` on you by 20%. You can leave second argument empty to clear your affinity. 30 minutes cooldown.  | `.affinity @MyHusband` 或 `.affinity`
`.waifus` `.waifulb` | Shows top 9 waifus. You can specify another page to show other waifus.  | `.waifus`
`.waifuinfo` `.waifustats` | Shows waifu stats for a target person. Defaults to you if no user is provided.  | `.waifuinfo @MyCrush` 或 `.waifuinfo`
`.waifugift` `.gift` `.gifts` | Gift an item to someone. This will increase their waifu value by 50% of the gifted item's value if they don't have affinity set towards you, or 100% if they do. Provide no arguments to see a list of items that you can gift. | `.gifts` 或 `.gift Rose @Himesama`
`.wheeloffortune` `.wheel` | Bets a certain amount of currency on the wheel of fortune. Wheel can stop on one of many different multipliers. Won amount is rounded down to the nearest whole number. | `.wheel 10`

###### [回目錄](#目錄)

### 寶可夢
指令與簡寫 | 說明 | 用法
----------------|--------------|-------
`.attack` | 使用動作指令攻擊目標。使用`.move list`來查看該類型可使用的動作列表。 | `.attack "vine whip" @someguy`
`.movelist` `.ml` | 列出您可使用的動作。 | `.ml`
`.heal` | 花費一點貨幣，治癒某個人或復活某位暈倒的玩家。 | `.heal @someone`
`.type` | 查詢目標的屬性。 | `.type @someone`
`.settype` | 花費一點貨幣來重新設定你的寶可夢屬性；不提供參數時將顯示屬性列表。 | `.settype fire` 或 `.settype`

###### [回目錄](#目錄)

### 搜尋
指令與簡寫 | 說明 | 用法
----------------|--------------|-------
`.lolban` | Shows top banned champions ordered by ban rate.  | `.lolban`
`.weather` `.we` | Shows weather data for a specified city. You can also specify a country after a comma.  | `.we Moscow, RU`
`.time` | Shows the current time and timezone in the specified location.  | `.time London, UK`
`.youtube` `.yt` | 在Youtube上搜尋指定字串並回傳第一個結果。 | `.yt query`
`.imdb` `.omdb` | Queries omdb for movies or series, show first result.  | `.imdb Batman vs Superman`
`.randomcat` `.meow` | Shows a random cat image.  | `.meow`
`.randomdog` `.woof` | Shows a random dog image.  | `.woof`
`.image` `.img` | Pulls the first image found using a search parameter. Use `.rimg` for different results.  | `.img cute kitten`
`.randomimage` `.rimg` | Pulls a random image using a search parameter.  | `.rimg cute kitten`
`.lmgtfy` | Google something for an idiot.  | `.lmgtfy query`
`.shorten` | Attempts to shorten an URL, if it fails, returns the input URL.  | `.shorten https://google.com`
`.google` `.g` | Get a Google search link for some terms.  | `.google query`
`.magicthegathering` `.mtg` | Searches for a Magic The Gathering card.  | `.magicthegathering about face` 或 `.mtg about face`
`.hearthstone` `.hs` | Searches for a Hearthstone card and shows its image. Takes a while to complete.  | `.hs Ysera`
`.yodify` `.yoda` | Translates your normal sentences into Yoda styled sentences!  | `.yoda my feelings hurt`
`.urbandict` `.ud` | Searches Urban Dictionary for a word.  | `.ud Pineapple`
`.define` `.def` | Finds a definition of a word.  | `.def heresy`
`.#` | Searches Tagdef.com for a hashtag.  | `.# ff`
`.catfact` | Shows a random catfact from <http://catfacts-api.appspot.com/api/facts>  | `.catfact`
`.revav` | Returns a Google reverse image search for someone's avatar.  | `.revav @SomeGuy`
`.revimg` | Returns a Google reverse image search for an image from a link.  | `.revimg Image link`
`.safebooru` | Shows a random image from safebooru with a given tag. Tag is optional but preferred. (multiple tags are appended with +)  | `.safebooru yuri+kissing`
`.wikipedia` `.wiki` | Gives you back a wikipedia link  | `.wiki query`
`.color` | Shows you what color corresponds to that hex.  | `.color 00ff00`
`.videocall` | Creates a private <http://www.appear.in> video call link for you and other mentioned people. The link is sent to mentioned people via a private message.  | `.videocall "@the First" "@Xyz"`
`.avatar` `.av` | Shows a mentioned person's avatar.  | `.av @SomeGuy`
`.wikia` | Gives you back a wikia link  | `.wikia mtg Vigilance` 或 `.wikia mlp Dashy`
`.mal` | Shows basic info from a MyAnimeList profile.  | `.mal straysocks`
`.anime` `.ani` `.aq` | Queries anilist for an anime and shows the first result.  | `.ani aquarion evol`
`.manga` `.mang` `.mq` | Queries anilist for a manga and shows the first result.  | `.mq Shingeki no kyojin`
`.feed` `.feedadd` | Subscribes to a feed. Bot will post an update up to once every 10 seconds. You can have up to 10 feeds on one server. All feeds must have unique URLs. **Bot需要`管理訊息`權限** | `.feed https://www.rt.com/rss/`
`.feedremove` `.feedrm` `.feeddel` | Stops tracking a feed on the given index. Use `.feeds` command to see a list of feeds and their indexes. **Bot需要`管理訊息`權限** | `.feedremove 3`
`.feeds` `.feedlist` | Shows the list of feeds you've subscribed to on this server. **Bot需要`管理訊息`權限** | `.feeds`
`.yomama` `.ym` | Shows a random joke from <http://api.yomomma.info/>  | `.ym`
`.randjoke` `.rj` | Shows a random joke from <http://tambal.azurewebsites.net/joke/random>  | `.rj`
`.chucknorris` `.cn` | Shows a random Chuck Norris joke from <http://api.icndb.com/jokes/random/>  | `.cn`
`.wowjoke` | Get one of Kwoth's penultimate WoW jokes.  | `.wowjoke`
`.magicitem` `.mi` | Shows a random magic item from <https://1d4chan.org/wiki/List_of_/tg/%27s_magic_items>  | `.mi`
`.memelist` | Pulls a list of memes you can use with `.memegen` from http://memegen.link/templates/  | `.memelist`
`.memegen` | Generates a meme from memelist with top and bottom text.  | `.memegen biw "gets iced coffee" "in the winter"`
`.osu` | Shows osu stats for a player.  | `.osu Name` 或 `.osu Name taiko`
`.osub` | Shows information about an osu beatmap.  | `.osub https://osu.ppy.sh/s/127712`
`.osu5` | Displays a user's top 5 plays.  | `.osu5 Name`
`.overwatch` `.ow` | Show's basic stats on a player (competitive rank, playtime, level etc) Region codes are: `eu` `us` `cn` `kr`  | `.ow us Battletag#1337` 或 `.overwatch eu Battletag#2016`
`.placelist` | Shows the list of available tags for the `.place` command.  | `.placelist`
`.place` | Shows a placeholder image of a given tag. Use `.placelist` to see all available tags. You can specify the width and height of the image as the last two optional arguments.  | `.place Cage` 或 `.place steven 500 400`
`.pokemon` `.poke` | Searches for a pokemon.  | `.poke Sylveon`
`.pokemonability` `.pokeab` | Searches for a pokemon ability.  | `.pokeab overgrow`
`.smashcast` `.hb` | Notifies this channel when a certain user starts streaming. **Bot需要`管理訊息`權限** | `.smashcast SomeStreamer`
`.twitch` `.tw` | 當特定的Twitch頻道開播時在當前頻道發送通知訊息。 **Bot需要`管理訊息`權限** | `.twitch SomeStreamer`
`.mixer` `.bm` | Notifies this channel when a certain user starts streaming. **Bot需要`管理訊息`權限** | `.mixer SomeStreamer`
`.liststreams` `.ls` | 列出當前已開啟開播通知的直播頻道。 | `.ls`
`.removestream` `.rms` | 取消發送特定直播頻道開播時的通知訊息。 **Bot需要`管理訊息`權限** | `.rms Twitch SomeGuy` 或 `.rms mixer SomeOtherGuy`
`.checkstream` `.cs` | Checks if a user is online on a certain streaming platform.  | `.cs twitch MyFavStreamer`
`.translate` `.trans` | 原語言>翻譯語言；將文字從原本的語言翻譯成另一個語言。 | `.trans en>fr Hello`
`.autotrans` `.at` | Starts automatic translation of all messages by users who set their `.atl` in this channel. You can set "del" argument to automatically delete all translated user messages. **Bot需要`管理員`權限** **僅限Bot擁有者** | `.at` 或 `.at del`
`.autotranslang` `.atl` | Sets your source and target language to be used with `.at`. Specify no arguments to remove previously set value.  | `.atl en>fr`
`.translangs` | 列出所有有效的翻譯語言。 | `.translangs`
`.xkcd` | Shows a XKCD comic. No arguments will retrieve random one. Number argument will retrieve a specific comic, and "latest" will get the latest one.  | `.xkcd` 或 `.xkcd 1400` 或 `.xkcd latest`

###### [回目錄](#目錄)

### 小工具
指令與簡寫 | 說明 | 用法
----------------|--------------|-------
`.togethertube` `.totube` | Creates a new room on <https://togethertube.com> and shows the link in the chat.  | `.totube`
`.whosplaying` `.whpl` | Shows a list of users who are playing the specified game.  | `.whpl Overwatch`
`.inrole` | Lists every person from the specified role on this server. You can use role ID, role name.  | `.inrole Some Role`
`.checkmyperms` | Checks your user-specific permissions on this channel.  | `.checkmyperms`
`.userid` `.uid` | 查看玩家ID。 | `.uid` 或 `.uid @SomeGuy`
`.channelid` `.cid` | 查看目前所在頻道ID。 | `.cid`
`.serverid` `.sid` | 查看目前所在伺服器ID。 | `.sid`
`.roles` | 列出目前所在伺服器的所有身分組，每頁顯示20個身分組。 | `.roles 2` 或 `.roles @Someone`
`.channeltopic` `.ct` | 顯示目前所在頻道說明。 | `.ct`
`.createinvite` `.crinv` | 創建一個不限使用次數與時間的邀請連結。 **Bot需要`建立即時邀請`權限** | `.crinv`
`.shardstats` | Stats for shards. Paginated with 25 shards per page.  | `.shardstats` 或 `.shardstats 2`
`.stats` | 顯示機器人的統計資訊。 | `.stats`
`.showemojis` `.se` | 顯示訊息中每個伺服器表情符號的名稱與連結。 | `.se A message full of SPECIAL emojis`
`.listservers` | 列出機器人加入的所有伺服器與其資訊。 **僅限Bot擁有者** | `.listservers 3`
`.savechat` | 將指定數量的訊息儲存為文字檔並傳給你。 **僅限Bot擁有者** | `.savechat 150`
`.ping` | 確認機器人的延遲數值。 | `.ping`
`.botconfigedit` `.bce` | Sets one of available bot config settings to a specified value. Use the command without any parameters to get a list of available settings. **Bot owner only** | `.bce CurrencyName b1nzy` 或 `.bce`
`.activity` | 列出以往洗頻的使用者與其詳細資訊。 **僅限Bot擁有者** | `.activity`
`.calculate` `.calc` | 運算一個簡單的數學算式。 | `.calc 1+1`
`.calcops` | 列出所有可在 `.calc` 指令內使用的函式。 | `.calcops`
`.alias` `.cmdmap` | Create a custom alias for a certain Nadeko command. Provide no alias to remove the existing one. **Bot需要`管理員`權限** | `.alias allin $bf 100 h` 或 `.alias "linux thingy" >loonix Spyware Windows`
`.aliaslist` `.cmdmaplist` `.aliases` | Shows the list of currently set aliases. Paginated.  | `.aliaslist` 或 `.aliaslist 3`
`.serverinfo` `.sinfo` | Shows info about the server the bot is on. If no Server is supplied, it defaults to current one.  | `.sinfo Some Server`
`.channelinfo` `.cinfo` | Shows info about the channel. If no channel is supplied, it defaults to current one.  | `.cinfo #some-channel`
`.userinfo` `.uinfo` | Shows info about the user. If no user is supplied, it defaults a user running the command.  | `.uinfo @SomeUser`
`.activity` | Checks for spammers. **僅限Bot擁有者** | `.activity`
`.parewrel` | Forces the update of the list of patrons who are eligible for the reward. **僅限Bot擁有者** | `.parewrel`
`.clparew` | Claim patreon rewards. If you're subscribed to bot owner's patreon you can use this command to claim your rewards - assuming bot owner did setup has their patreon key.  | `.clparew`
`.listquotes` `.liqu` | Lists all quotes on the server ordered alphabetically. 15 Per page.  | `.liqu` 或 `.liqu 3`
`...` | Shows a random quote with a specified name.  | `... abc`
`.qsearch` | Shows a random quote for a keyword that contains any text specified in the search.  | `.qsearch keyword text`
`.quoteid` `.qid` | Displays the quote with the specified ID number. Quote ID numbers can be found by typing `.liqu [num]` where `[num]` is a number of a page which contains 15 quotes.  | `.qid 123456`
`..` | Adds a new quote with the specified name and message.  | `.. sayhi Hi`
`.quotedel` `.qdel` | Deletes a quote with the specified ID. You have to be either server Administrator or the creator of the quote to delete it.  | `.qdel 123456`
`.delallq` `.daq` | Deletes all quotes on a specified keyword. **Bot需要`管理員`權限** | `.delallq kek`
`.remind` | Sends a message to you or a channel after certain amount of time. First argument is `me`/`here`/'channelname'. Second argument is time in a descending order (mo>w>d>h>m) example: 1w5d3h10m. Third argument is a (multiword) message.  | `.remind me 1d5h Do something` 或 `.remind #general 1m Start now!`
`.remindtemplate` | Sets message for when the remind is triggered.  Available placeholders are `%user%` - user who ran the command, `%message%` - Message specified in the remind, `%target%` - target channel of the remind. **僅限Bot擁有者** | `.remindtemplate %user%, do %message%!`
`.repeatinvoke` `.repinv` | Immediately shows the repeat message on a certain index and restarts its timer. **Bot需要`管理訊息`權限** | `.repinv 1`
`.repeatremove` `.reprm` | Removes a repeating message on a specified index. Use `.repeatlist` to see indexes. **Bot需要`管理訊息`權限** | `.reprm 2`
`.repeat` | Repeat a message every `X` minutes in the current channel. You can have up to 5 repeating messages on the server in total. **Bot需要`管理訊息`權限** | `.repeat 5 Hello there`
`.repeatlist` `.replst` | Shows currently repeating messages and their indexes. **Bot需要`管理訊息`權限** | `.repeatlist`
`.streamrole` | Sets a role which is monitored for streamers (FromRole), and a role to add if a user from 'FromRole' is streaming (AddRole). When a user from 'FromRole' starts streaming, they will receive an 'AddRole'. Provide no arguments to disable **Bot需要`管理身分組`權限** | `.streamrole "Eligible Streamers" "Featured Streams"`
`.streamrolekw` `.srkw` | Sets keyword which is required in the stream's title in order for the streamrole to apply. Provide no keyword in order to reset. **Bot需要`管理身分組`權限** | `.srkw` 或 `.srkw PUBG`
`.streamrolebl` `.srbl` | Adds or removes a blacklisted user. Blacklisted users will never receive the stream role. **Bot需要`管理身分組`權限** | `.srbl add @b1nzy#1234` 或 `.srbl rem @b1nzy#1234`
`.streamrolewl` `.srwl` | Adds or removes a whitelisted user. Whitelisted users will receive the stream role even if they don't have the specified keyword in their stream title. **Bot需要`管理身分組`權限** | `.srwl add @b1nzy#1234` 或 `.srwl rem @b1nzy#1234`
`.convertlist` | List of the convertible dimensions and currencies.  | `.convertlist`
`.convert` | Convert quantities. Use `.convertlist` to see supported dimensions and currencies.  | `.convert m km 1000`
`.verboseerror` `.ve` | Toggles whether the bot should print command errors when a command is incorrectly used. **Bot需要`管理訊息`權限** | `.ve`

###### [回目錄](#目錄)

### 自定義回覆
指令與簡寫 | 說明 | 用法
----------------|--------------|-------
`.addcustreact` `.acr` | Add a custom reaction with a trigger and a response. Running this command in server requires the Administration permission. Running this command in DM is Bot Owner only and adds a new global custom reaction. Guide here: <http://ghostbot.readthedocs.io/zh_TW/latest/Custom%20Reactions/>  | `.acr "hello" Hi there %user%`
`.listcustreact` `.lcr` | Lists global or server custom reactions (20 commands per page). Running the command in DM will list global custom reactions, while running it in server will list that server's custom reactions. Specifying `all` argument instead of the number will DM you a text file with a list of all custom reactions.  | `.lcr 1` 或 `.lcr all`
`.listcustreactg` `.lcrg` | Lists global or server custom reactions (20 commands per page) grouped by trigger, and show a number of responses for each. Running the command in DM will list global custom reactions, while running it in server will list that server's custom reactions.  | `.lcrg 1`
`.showcustreact` `.scr` | Shows a custom reaction's response on a given ID.  | `.scr 1`
`.delcustreact` `.dcr` | Deletes a custom reaction on a specific index. If ran in DM, it is bot owner only and deletes a global custom reaction. If ran in a server, it requires Administration privileges and removes server custom reaction.  | `.dcr 5`
`.crca` | Toggles whether the custom reaction will trigger if the triggering message contains the keyword (instead of only starting with it).  | `.crca 44`
`.crdm` | Toggles whether the response message of the custom reaction will be sent as a direct message.  | `.crdm 44`
`.crad` | Toggles whether the message triggering the custom reaction will be automatically deleted.  | `.crad 59`
`.crstatsclear` | Resets the counters on `.crstats`. You can specify a trigger to clear stats only for that trigger. **僅限Bot擁有者** | `.crstatsclear` 或 `.crstatsclear rng`
`.crstats` | Shows a list of custom reactions and the number of times they have been executed. Paginated with 10 per page. Use `.crstatsclear` to reset the counters.  | `.crstats` 或 `.crstats 3`

###### [回目錄](#目錄)

### Xp
指令與簡寫 | 說明 | 用法
----------------|--------------|-------
`.experience` `.xp` | Shows your xp stats. Specify the user to show that user's stats instead. | `.xp`
`.xprolerewards` `.xprrs` | Shows currently set role rewards. | `.xprrs`
`.xprolereward` `.xprr` | Sets a role reward on a specified level. Provide no role name in order to remove the role reward. **Bot需要`管理身分組`權限** | `.xprr 3 Social`
`.xpnotify` `.xpn` | Sets how the bot should notify you when you get a `server` or `global` level. You can set `dm` (for the bot to send a direct message), `channel` (to get notified in the channel you sent the last message in) or `none` to disable. | `.xpn global dm` 或 `.xpn server channel`
`.xpexclude` `.xpex` | Exclude a channel, role or current server from the xp system, or whole current server. **Bot需要`管理員`權限** | `.xpex Role Excluded-Role` 或 `.xpex Server`
`.xpexclusionlist` `.xpexl` | Shows the roles and channels excluded from the XP system on this server, as well as whether the whole server is excluded. | `.xpexl`
`.xpleaderboard` `.xplb` | Shows current server's xp leaderboard. | `.xplb`
`.xpgleaderboard` `.xpglb` | Shows the global xp leaderboard. | `.xpglb`
`.xpadd` | Adds xp to a user on the server. This does not affect their global ranking. You can use negative values. **Bot需要`管理員`權限** | `.xpadd 100 @b1nzy`
`.clubadmin` | Assigns (or unassigns) staff role to the member of the club. Admins can ban, kick and accept applications.  | `.clubadmin`
`.clubcreate` | Creates a club. You must be atleast level 5 and not be in the club already. | `.clubcreate b1nzy's friends`
`.clubicon` | Sets the club icon. | `.clubicon https://i.imgur.com/htfDMfU.png`
`.clubinfo` | Shows information about the club. | `.clubinfo b1nzy's friends#123`
`.clubbans` | Shows the list of users who have banned from your club. Paginated. You must be club owner to use this command. | `.clubbans 2`
`.clubapps` | Shows the list of users who have applied to your club. Paginated. You must be club owner to use this command. | `.clubapps 2`
`.clubapply` | Apply to join a club. You must meet that club's minimum level requirement, and not be on its ban list. | `.clubapply b1nzy's friends#123`
`.clubaccept` | Accept a user who applied to your club.  | `.clubaccept b1nzy#1337`
`.clubleave` | Leaves the club you're currently in. | `.clubleave`
`.clubkick` | Kicks the user from the club. You must be the club owner. They will be able to apply again. | `.clubkick b1nzy#1337`
`.clubban` | Bans the user from the club. You must be the club owner. They will not be able to apply again. | `.clubban b1nzy#1337`
`.clubunban` | Unbans the previously banned user from the club. You must be the club owner. | `.clubunban b1nzy#1337`
`.clublevelreq` | Sets the club required level to apply to join the club. You must be club owner. You can't set this number below 5. | `.clublevelreq 7`
`.clubdisband` | Disbands the club you're the owner of. This action is irreversible. | `.clubdisband`
`.clublb` | Shows club rankings on the specified page. | `.clublb 2`
 
 ###### [回目錄](#目錄)

### NSFW
指令與簡寫 | 說明 | 用法
----------------|--------------|-------
`.autohentai` | Posts a hentai every X seconds with a random tag from the provided tags. Use `|` to separate tags. 20 seconds minimum. Provide no arguments to disable. **Bot需要`管理訊息`權限** | `.autohentai 30 yuri|tail|long_hair` 或 `.autohentai`
`.autoboobs` | Posts a boobs every X seconds. 20 seconds minimum. Provide no arguments to disable. **Bot需要`管理訊息`權限** | `.autoboobs 30` 或 `.autoboobs`
`.autobutts` | Posts a butts every X seconds. 20 seconds minimum. Provide no arguments to disable. **Bot需要`管理訊息`權限** | `.autobutts 30` 或 `.autobutts`
`.hentai` | Shows a hentai image from a random website (gelbooru or danbooru or konachan or atfbooru or yandere) with a given tag. Tag is optional but preferred. Only 1 tag allowed.  | `.hentai yuri`
`.hentaibomb` | Shows a total 5 images (from gelbooru, danbooru, konachan, yandere and atfbooru). Tag is optional but preferred. | `.hentaibomb yuri`
`.yandere` | Shows a random image from yandere with a given tag. Tag is optional but preferred. (multiple tags are appended with +) | `.yandere tag1+tag2`
`.konachan` | Shows a random hentai image from konachan with a given tag. Tag is optional but preferred. | `.konachan yuri`
`.e621` | Shows a random hentai image from e621.net with a given tag. Tag is optional but preferred. Use spaces for multiple tags. | `.e621 yuri kissing`
`.rule34` | Shows a random image from rule34.xx with a given tag. Tag is optional but preferred. (multiple tags are appended with +) | `.rule34 yuri+kissing`
`.danbooru` | Shows a random hentai image from danbooru with a given tag. Tag is optional but preferred. (multiple tags are appended with +) | `.danbooru yuri+kissing`
`.gelbooru` | Shows a random hentai image from gelbooru with a given tag. Tag is optional but preferred. (multiple tags are appended with +) | `.gelbooru yuri+kissing`
`.boobs` | Real adult content. | `.boobs`
`.butts` `.ass` `.butt` | Real adult content. | `.butts` 或 `.ass`
`.nsfwtagbl` `.nsfwtbl` | Toggles whether the tag is blacklisted or not in nsfw searches. Provide no parameters to see the list of blacklisted tags. | `.nsfwtbl poop`
`.nsfwcc` | Clears nsfw cache. **僅限Bot擁有者** | `.nsfwcc`

###### [回目錄](#目錄)
