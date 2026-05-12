# Privacy Policy for Salesforce Agentic Bot

Effective date: May 12, 2026

Salesforce Agentic Bot is a Chrome extension that provides a side-panel assistant for Salesforce admins and developers. It helps users inspect the active Salesforce org, view schema and metadata, open Salesforce API tools, and chat with OpenAI using a user-provided OpenAI API key.

## Data the extension handles

Salesforce Agentic Bot may handle the following data to provide its features:

- Salesforce session cookie: used locally to authenticate Salesforce API requests for the currently signed-in Salesforce user.
- Salesforce org and user information: such as org ID, org name, username, user name, email address, user ID, and related Salesforce profile fields returned by Salesforce APIs.
- Salesforce website and API content: such as the active Salesforce tab URL and title, schema, metadata, REST API responses, Tooling API responses, and Metadata API responses.
- OpenAI API key: entered by the user and stored in Chrome extension storage.
- Chat data: messages typed by the user, assistant responses, saved responses, token usage, and previous OpenAI response IDs.

The extension is not designed to collect health information, financial/payment information, GPS location, nearby-device location, full browser history, mouse tracking, scroll tracking, or keystroke logging.

## How data is used

The extension uses data only to provide its Salesforce assistant features:

- To authenticate Salesforce API calls for the active Salesforce org.
- To display org, user, schema, metadata, REST, Tooling, and Metadata API information inside the extension.
- To show the current Salesforce tab context in the side panel.
- To send chat messages, selected Salesforce context, and current Salesforce tab URL/title to OpenAI only when the user sends a chat message.
- To store chat history, saved responses, schema metadata, and the user-entered OpenAI API key locally for convenience.

## Data sharing

Salesforce Agentic Bot does not sell user data and does not use user data for advertising, tracking, or profiling.

Data is shared only as needed for user-facing functionality:

- Salesforce data is requested from Salesforce domains for the currently signed-in Salesforce user.
- Chat messages and related Salesforce context are sent to OpenAI at `https://api.openai.com` only when the user sends a chat message.

No extension data is sent to a separate developer-operated server.

## Storage and retention

The extension stores settings and feature data in Chrome extension storage and browser local storage, including:

- User-entered OpenAI API key.
- Chat history and saved assistant responses.
- Previous OpenAI response IDs used to continue chat context.
- Retrieved Salesforce schema and metadata used for local browsing and search.

Users can clear the OpenAI API key from the Chat tab and clear retrieved schema metadata from the Schema tools. Users can also remove extension data by uninstalling the extension or clearing extension storage in Chrome.

## Security

Network requests use HTTPS. The extension does not execute remote code. All JavaScript, HTML, and CSS are packaged with the extension.

## Contact

For privacy questions, contact the publisher using the contact email listed on the Chrome Web Store listing.
