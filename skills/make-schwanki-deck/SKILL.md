---
name: make-schwanki-deck
description: Turn a language chat, lesson transcript or translation into a Schwanki flashcard deck. Use when the user asks to save words to Schwanki, make flashcards from a lesson, or build a deck around words they keep forgetting.
---

# Make a Schwanki deck

Schwanki is the user's spaced-repetition flashcard app. Saved cards land in a swipe feed on their phone. Use the `schwanki` MCP tools.

## Pick the words

- From a transcript or chat: choose the words and phrases the learner did not already know, the ones they got wrong, and the ones a teacher corrected. Skip names, filler and words they clearly use well.
- Keep each card's front short: the word or phrase in the learning language. Put the meaning on the back. Add a reading (pinyin, kana, romanization) when the script needs one, and an example sentence from the conversation when there is a good one.
- One learning language per deck, 1 to 24 cards per save. Split bigger sets into themed decks.

## Check before saving

Call `list_decks`, then `get_deck_cards` on decks in the same language, and drop words the user already has.

To build around words the user keeps forgetting, read their cards and sort by `lapses`, then make new cards (phrases or sentences) that use those words.

## Save

Call `save_review_deck` with:

- `title`: what the deck is about ("italki lesson, Nov 12", "Tokyo tourist phrases").
- `teacher`: the tutor, class or source when the user names one, so Schwanki groups the deck with that teacher's other decks.

Share the review link from the result.

The tools cannot edit or delete decks or cards.
