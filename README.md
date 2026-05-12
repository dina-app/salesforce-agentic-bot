# Salesforce Agentic Bot

Salesforce Agentic Bot is a Chrome extension that adds a right-side assistant workspace for Salesforce admins and developers. It helps inspect the active Salesforce org, browse schema and metadata, open API tools, and chat with OpenAI using the user's own API key.

## Features

- Right-side Chrome side panel for Salesforce pages.
- Active Salesforce tab detection with current page title and URL context.
- Org and user summary for the signed-in Salesforce session.
- OpenAI chat powered by a user-entered API key stored in Chrome extension storage.
- Continued chat context using OpenAI `previous_response_id`.
- Token usage display for assistant responses.
- Save useful assistant responses to the Saved tab.
- Dev Logs tab for background Salesforce/OpenAI request logs.
- Data Export and REST Explorer extension pages.
- Schema Viewer with Salesforce-style project explorer layout.
- Metadata retrieval for objects, Apex, Visualforce, LWC, Aura, flows, layouts, labels, permission sets, profiles, reports, tabs, triggers, workflows, and other supported metadata types.
- Schema and metadata search with VS Code-like explorer results.
- XML/JSON detail viewer for retrieved metadata.

## Install Locally

1. Open Chrome and go to `chrome://extensions`.
2. Enable **Developer mode**.
3. Click **Load unpacked**.
4. Select the `Salesforce Agentic Bot` folder.
5. Open a Salesforce page and click the extension icon.

## OpenAI API Key

The extension does not ship with an OpenAI API key.

1. Open the extension on a Salesforce tab.
2. Go to the **Chat** tab.
3. Paste your OpenAI API key into **OpenAI API key**.
4. Click **Save**.

The key is stored locally in Chrome extension storage. You can clear it from the Chat tab.

## Salesforce Access

The extension uses the current Salesforce browser session. It reads the Salesforce `sid` cookie for the active Salesforce domain so it can call Salesforce REST, Tooling, and Metadata APIs as the currently signed-in user.

## Packaging

To create a Chrome Web Store upload zip, run this from inside the extension folder:

```sh
zip -r -FS ../salesforce-agentic-bot-v0.3.0.zip . -x '*.DS_Store' '__MACOSX/*' '*.zip'
```

The zip must contain `manifest.json` at the root.

## Chrome Web Store Submission

Use the root-level `CHROME_WEB_STORE_SUBMISSION.md` file for permission justifications, data usage selections, and privacy policy guidance.

The root-level `PRIVACY_POLICY.md` file contains a publishable privacy policy.

## Privacy

The extension stores settings, chat history, saved responses, and retrieved schema metadata locally in the browser. Chat messages and selected Salesforce context are sent to OpenAI only when the user sends a chat message. The extension does not sell user data, does not use advertising, and does not execute remote code.

## Notes

- The extension is built for Manifest V3.
- The OpenAI model is configured in `openai-config.js`.
- Large metadata retrieves can hit browser storage limits. If that happens, clear retrieved metadata, select fewer metadata types, and retrieve again.
