# Package Tracker for Gemini CLI

Ask Gemini CLI about your parcels. This extension connects [Package Tracker](https://starthrop.com/en/package-tracker/) by Starthrop Dynamics — more than 1,100 carriers and national postal services in one tracking engine, in 39 languages, on iPhone, Android, Apple Watch, Apple TV, the web and the Chrome and Edge extensions — to Gemini CLI through its remote MCP server.

## What you can do

- **My deliveries** (`list_shipments`): which parcels are still on the way, with carrier, status and latest event. Read-only.
- **Track my parcel** (`track_shipment`): the confirmed current status of one delivery, when it was last checked and a link to its full timeline. Read-only.
- **Add tracking codes** (`add_shipments`): paste a shipping email or a list of codes; Gemini shows you a preview of the codes found and adds them only after you agree.

Try:

- "Which of my packages are still on the way?"
- "What is the latest update on my AliExpress order?"
- "Add the tracking numbers from this email: …"

## Install

```bash
gemini extensions install https://github.com/starthrop-dynamics/package-tracker-gemini-extension
```

Restart Gemini CLI. The first time a tool is used, Package Tracker's sign-in opens in your browser (it must run on the same computer). If it does not open, run `/mcp auth package-tracker` inside Gemini CLI.

When you connect, Package Tracker asks you to choose:

- **Read** (required): your parcels' codes, names and statuses.
- **Add** (optional): adding parcels, always after you confirm each request.

Requires a Package Tracker account — [create one for free](https://package-tracker.starthrop.com/).

### Without the extension

```bash
gemini mcp add --transport http package-tracker https://package-tracker.starthrop.com/mcp
```

## Privacy

The assistant sees only your own deliveries — never your addresses, contacts, documents or proof-of-delivery images. Your conversations are handled by Google under its own terms. See the [Package Tracker privacy policy](https://starthrop.com/en/package-tracker/privacy/) and [terms of use](https://starthrop.com/en/package-tracker/terms/).

To disconnect, open **Profile › Connections** in Package Tracker and choose **Disconnect**, or uninstall the extension with `gemini extensions uninstall package-tracker`.

## Support

- Documentation: https://starthrop.com/en/package-tracker/assistants/
- Email: support@starthrop.com (Portuguese and English). We will never ask for your password.

© Starthrop Dynamics
