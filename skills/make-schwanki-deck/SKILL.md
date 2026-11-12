---
name: make-schwanki-deck
description: Turn a language chat, lesson transcript or translation into a Schwanki flashcard deck, optionally with pictures, audio or videos. Use when the user asks to save words to Schwanki, make flashcards from a lesson, or build a deck around words they keep forgetting.
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
- `media`: only when the user asks for pictures (`image`), pronunciation (`audio`) or short videos (`video`). They cost Schwanki AI credits: 1 per picture or audio clip and 7 per video, per card. For a large video deck, tell the user the total first.
- `mediaStyle`: the user's own art direction for pictures and videos, such as a recurring character or setting ("an animated duck tourist in Shibuya").

Share the review link from the result. If the result says there aren't enough credits, the cards are still saved; tell the user they can top up in Schwanki Settings.

The tools cannot edit or delete decks or cards.
