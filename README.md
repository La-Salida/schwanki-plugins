# Schwanki plugins

Connects Claude Code and Cursor to [Schwanki](https://schwankiapp.com), a spaced-repetition flashcard app for language learners.

## Setup

**Claude Code:**

```
/plugin install schwanki --marketplace La-Salida/schwanki-plugins
```

**Cursor:** install Schwanki from the Cursor Marketplace.

The Claude Code plugin adds the Schwanki MCP server at `https://schwankiapp.com/mcp/claude` (the same server listed in [Claude's connector directory](https://claude.ai/directory/schwanki)) and a `make-schwanki-deck` skill. The Cursor plugin adds `https://schwankiapp.com/mcp`. The first time a tool runs, your app opens Schwanki's sign-in page. Sign in, check the app's name, and choose **Connect**. There's no API key: the app registers itself and you approve it once.

## Tools

| Tool | What it does |
| --- | --- |
| `list_decks` | Lists your decks with language, card count and cards due now |
| `get_deck_cards` | Reads a deck's cards and review progress, up to 200 per call |
| `save_review_deck` | Saves 1 to 24 cards in one language as a deck, filed under a teacher or topic; skips cards you already have |

Connected apps can't edit or delete your decks, cards or review history.

## Example prompts

- Take this transcript from my italki Chinese lesson and save the top 20 words as a Schwanki deck filed under my teacher.
- Turn the words from this translation chat into cards filed under Señora Raquel, with an example sentence on each.
- Find the French words I keep forgetting and make me a new deck that uses each of them.

In Cursor and other apps using `https://schwankiapp.com/mcp`, the save tool can also add pictures, audio or short videos, which use Schwanki AI credits (1 per picture or audio clip, 7 per video) and are made only when you ask.

## Help

Setup guides: https://schwankiapp.com/integrations/claude · https://schwankiapp.com/integrations/mcp · Support: https://schwankiapp.com/support · Privacy: https://schwankiapp.com/privacy

## MCP Registry

`server.json` is Schwanki's entry in the [MCP Registry](https://registry.modelcontextprotocol.io) (`io.github.La-Salida/schwanki`). To update it, bump `version` and run the **Publish to MCP Registry** workflow.
