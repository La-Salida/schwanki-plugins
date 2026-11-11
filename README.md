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

- Save the Spanish phrases from this chat to Schwanki.
- Which of my Schwanki decks has the most cards due?
- Quiz me on my Japanese deck.

## Help

Setup guide: https://schwankiapp.com/integrations/mcp · Support: https://schwankiapp.com/support · Privacy: https://schwankiapp.com/privacy

## MCP Registry

`server.json` is Schwanki's entry in the [MCP Registry](https://registry.modelcontextprotocol.io) (`io.github.La-Salida/schwanki`). To update it, bump `version` and run the **Publish to MCP Registry** workflow.
