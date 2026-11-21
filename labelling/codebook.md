# Codebook: Complaint Types in Steam Reviews (version 2, 2026-11-19: pure wishes and suggestions are not complaints)

Each review gets **one or more label numbers**. Labels come from the review text only. The reviewer's recommendation (thumbs up or down) is not shown and must not be guessed. A positive-sounding review can still contain complaints.

| No. | Label | Covers |
|---|---|---|
| 0 | No complaint | The review contains no complaint about the game, its developer or its service. **Use 0 alone, never with another number.** |
| 1 | Technical and performance | Bugs, glitches, crashes, freezes, failure to launch, save corruption, low frame rate, stutter, poor optimisation, high hardware demands, visual or audio glitches, hardware or platform compatibility (Steam Deck, Linux, controllers, keyboard layouts). |
| 2 | Gameplay and design | How the game plays and is designed: mechanics, combat, controls, camera, user interface and menus, difficulty, balance, grind, repetitive or tedious tasks, progression, AI behaviour, quest and level design, art style or sound design that the reviewer dislikes, missing quality-of-life options (for example unskippable cutscenes). |
| 3 | Content and updates | How much there is and how complete it is: too little content, short length, little variety, missing features or modes, unfinished or "early access" feel, story, characters and writing, slow or poor updates, content removed by an update. |
| 4 | Community and cheating | Other players: cheaters and hackers, toxic or hostile players, griefing, a dead or small player base that makes matchmaking empty, abuse of reporting by players. |
| 5 | Pricing and monetisation | Price too high, poor value for money ("not worth $60", "waste of money"), expensive or excessive DLC, microtransactions, content locked behind DLC, pay-to-win, discounts or regional pricing. |
| 6 | Developer conduct and operations | The developer or publisher and the online service: servers, connection drops, lag caused by the network, desync, matchmaking or reconnect failures, launcher, account and login requirements, DRM or always-online requirements, customer support, ban and moderation decisions, ignoring player feedback or bugs, broken promises, communication, use of generative AI, policy or business decisions (for example removing a feature from Steam Family Sharing). |
| 7 | Other complaint | A complaint that fits none of 1 to 6, or a negative judgement with no specific reason ("garbage game", "overrated", "boring", "refunded"), or a complaint too vague to place. |

## Rules

1. **What counts as a complaint.** A statement that something about this game, its developer or its service is currently bad, broken, missing or too much. Mild criticism inside a positive review counts ("great game, but a bit grindy" → 2). The test is whether the review says the current state is bad.
2. **What does not count.**
   - Pure wishes and suggestions that do not say anything is bad now ("hope they add co-op", "would love more Pals in future updates"). If the wish states a current problem, label that problem ("I wish there were more maps, the four we have get old fast" → 3; "please fix the crashes" → 1).
   - Problems that the reviewer says are already fixed ("crashed at launch, fixed now").
   - Criticism aimed only at other games or companies ("better than Elden Ring", "Nintendo sucks").
   - Jokes, memes, role-play and sarcasm with no clear criticism of this game.
   - The reviewer's own life ("I lost my weekend to this game") when it is praise.
   - Difficulty or challenge described as a good thing.
3. **Choose all that apply.** If a review complains about several things, give every matching number ("2,5"). Give each number at most once.
4. **Use 7 only when nothing else fits.** If a review has a specific complaint (for example 1) and also a vague negative judgement, give only the specific number(s).
5. **Boundary rules.**
   - Technical (1) vs operations (6): problems on the player's machine (crash, frame rate, in-game bug) are 1. Problems with servers, network, launcher or accounts are 6. Lag in an online game caused by servers or connection is 6; low frame rate is 1.
   - Gameplay (2) vs content (3): *how* it plays is 2 (mechanics, difficulty, UI, balance, tedious quests); *how much* there is or *how complete* it is is 3 (amount, variety, missing modes, story).
   - Content (3) and pricing (5) often occur together: "too little content for $60" → 3,5. "The base game lacks features that are sold as DLC" → 3,5.
   - Community (4) and operations (6): cheaters → 4. If the review also blames the developer for not acting ("devs do nothing about hackers") → 4,6.
   - Bugs that the developer ignores: the bug → 1; ignoring it → 6.
   - Remasters and editions compared with the original: label the specific problem (for example worse graphics through bugs → 1, changed art style → 2); if no specific problem is named → 7.
6. **Uncertain cases.** Pick the most likely reading of the text. Do not use outside knowledge about the game to add complaints that the text does not state.
