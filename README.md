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
| `save_review_deck` | Saves 1 to 24 cards in one language as a deck, filed under a teacher or topic, with optional pictures, audio or video; skips cards you already have |

Connected apps can't edit or delete your decks, cards or review history.

## Example prompts

- Take this transcript from my italki Chinese lesson and save the top 20 words as a Schwanki deck with memorable video scenes.
- Turn the words from this translation chat into cards filed under Señora Raquel, with a video for each.
- Build me a Japanese tourist phrases deck where every card is a short video starring an animated duck tourist in Shibuya.
- Find the French words I keep forgetting and make me a new deck that uses each of them.

Pictures, audio and videos use Schwanki AI credits (1 per picture or audio clip, 7 per video) and are made only when you ask.

## Help

Setup guide: https://schwankiapp.com/integrations/mcp · Support: https://schwankiapp.com/support · Privacy: https://schwankiapp.com/privacy

## MCP Registry

`server.json` is Schwanki's entry in the [MCP Registry](https://registry.modelcontextprotocol.io) (`io.github.La-Salida/schwanki`). To update it, bump `version` and run the **Publish to MCP Registry** workflow.
