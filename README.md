# Schwanki for Cursor

Connects Cursor to [Schwanki](https://schwankiapp.com), a spaced-repetition flashcard app for language learners.

## Setup

1. Install the plugin. It adds the Schwanki MCP server at `https://schwankiapp.com/mcp`.
2. The first time a tool runs, Cursor opens Schwanki's sign-in page. Sign in, check that the app asking is Cursor, and choose **Connect**.

There's no API key: Cursor registers itself and you approve it once.

## Tools

| Tool | What it does |
| --- | --- |
| `list_decks` | Lists your decks with language, card count and cards due now |
| `get_deck_cards` | Reads a deck's cards and review progress, up to 200 per call |
| `save_review_deck` | Saves 1 to 24 cards in one language as a deck; skips cards you already have |

Connected apps can't edit or delete your decks, cards or review history.

## Example prompts

- Find the Spanish words I keep forgetting in Schwanki and write me a short story that uses all of them.
- I'm in Tokyo next week. Check my Japanese decks, then save the 20 phrases I'll need that I don't have yet.
- Be a waiter in a Paris café. When we're done, save every phrase I got wrong to Schwanki.
- Here's my German lesson transcript. Make cards for the new words and skip anything already in my decks.

## Help

Setup guide: https://schwankiapp.com/integrations/mcp · Support: https://schwankiapp.com/support · Privacy: https://schwankiapp.com/privacy

## MCP Registry

`server.json` is Schwanki's entry in the [MCP Registry](https://registry.modelcontextprotocol.io) (`io.github.La-Salida/schwanki`). To update it, bump `version` and run the **Publish to MCP Registry** workflow.
