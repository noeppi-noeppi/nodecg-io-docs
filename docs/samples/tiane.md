## Using the TIANE sample bundle

The tiane-discord example bundle in `samples/tiane_discord` demonstrates how to run TIANE as a discord bot.

### Prerequisites

 * Working NodeCG & nodecg-oi installation
 * a Discord Bot token
 * A working [TIANE](https://github.com/FerdiKr/TIANE) Server
 
### Configure the Discord sample bundle

1. In  TIANE's repository root edit the file `server/TIANE_config.json` and set `websocket` to `enabled`

2. Start TIANE

3. Modify `index.ts` in `samples/tiane_discord/extension`: Set `dChannel` to the channel id of your discord channel id, where TIANE should chat. To find out a discord channel id, see [here](https://kb.statbot.net/faq/how-do-i-find-my-server-user-channel-id/)

4. Start nodecg with nodecg-io installed. The Discord-guild-chat bundle is currently part of it so it should also be loaded.

5. Go to the `nodecg-io` tab in the nodecg dashboard.

6. Login using your password. If this is your first run, then enter the password with which you want to encrypt your configurations and credentials.

7. Create and configure a new discord service instance. See [here](./discord.md) on how it works.

8. Crete a new TIANE service.

9. Provide the websocket-server address: Edit the configuration

```json
{
  "address": "localhost:19526"
}
```

10. Set the created discord and tiane service instances to the service dependencies of the tiane-discord bundle.

11. Ope nyour discord and start chatting with TIANE