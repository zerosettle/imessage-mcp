# ZeroSettle iMessage for ChatGPT

Review conversations and draft replies for your ZeroSettle business number in ChatGPT. Connect ZeroSettle's hosted MCP server with OAuth from ChatGPT on the web.

| Setting | Value |
| --- | --- |
| Name | `ZeroSettle iMessage` |
| MCP server URL | `https://portal.zerosettle.io/mcp` |
| Authentication | OAuth with dynamic client registration |

## Connect in ChatGPT

1. Open [ChatGPT Plugins](https://chatgpt.com/plugins), select **+**, then **Add custom MCP server**.
2. Enter the name and URL above. Choose **OAuth** and leave the client ID and secret blank. If ChatGPT offers a registration choice, select dynamic client registration (DCR).
3. Review the permissions, select **Create as a plugin**, and install it. Sign in on the ZeroSettle authorization page when prompted and select your existing line if asked.
4. Open a new Work chat, type **@**, and select **ZeroSettle iMessage**. Try this read-only check:

   ```text
   Use ZeroSettle iMessage to call get_line once. Show only my connected business number and whether the line is active. Do not send a message or change settings.
   ```

An active ZeroSettle line gives you access to its conversations. ChatGPT Pro supports read/fetch for custom MCP servers. Business and Enterprise/Edu can enable writes subject to workspace permissions and confirmations. If **Add custom MCP server** is missing, check your plan and workspace with an admin. [OpenAI setup guide](https://developers.openai.com/plugins/deploy/connect-chatgpt) · [Plans and permissions](https://help.openai.com/en/articles/12584461-connecting-custom-mcp-servers-in-chatgpt)

## Give ChatGPT the instructions

Paste this into a new chat:

```text
Read https://raw.githubusercontent.com/zerosettle/imessage-mcp/main/CHATGPT.md and help me connect my ZeroSettle iMessage line.
```

If ChatGPT cannot open the link, attach or paste [CHATGPT.md](CHATGPT.md). The guide works without an installed plugin. To use your line in chat, complete the connection above. Keep API keys and sign-in codes out of the conversation.

Once connected, start with “Show my recent ZeroSettle conversations” or “Read the latest messages in the conversation I select and draft a reply for me to review.” On a workspace with write access, review the sending line, recipient, and exact text before confirming a send.

This connection uses a ZeroSettle business number from inside a conversation. For an assistant that replies when people text the number, use [ZeroSettle's hosted agent or webhook API](https://zerosettle.io/imessage-api/ai-apps/).

[MCP tool reference](https://portal.zerosettle.io/docs/mcp) · [Plain-text reference](https://portal.zerosettle.io/docs/mcp.md) · [Privacy](https://zerosettle.io/legal/privacy/) · [Terms](https://zerosettle.io/legal/imessage-terms/)
