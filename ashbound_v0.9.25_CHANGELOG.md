# Ashbound v0.9.25

New file only. v0.9.23 and older builds are unchanged. `index.html` is unchanged, so the live page is not updated.

## Combat dock

- Skill, attack, move, and ultimate cards draw a cell strip (behind, self, forward 1–5) for **which cells the action affects**.
- Your figure and facing arrow sit **inside** your own square. If that square is also hit, the effect icon stays in the corner so you remain visible.
- ✹ = every enemy in the cell. ◎ = choose a target in those cells. · = not affected.
- Dice sockets are a separate row. Body text is 14px, wraps, and is not ellipsized.
- Dark/gold dock. The board gives up height so the cards on screen fit in the viewport. Extra skills move with ก่อนหน้า / ถัดไป. A card that is on screen shows its name, diagram, full body, sockets, and the lock line together. The lock line sits under the sockets. Diagram captions are one short line; the strip shows the cells. Missing combat title or tier prints a fallback instead of the word undefined.
- Hover no longer scales or slides cards. Idle loops stay off.

## Rules touched

- Night still has no action phase. It also skips the story popup and goes straight into combat. Other fights still open with the story.
- Black Tide follows rulebook §33: Close Melee, same cell only.
- Eroding Halo level 1 is distance 2 (sheet: Rang 2), forward only.
- Jack Volley and Lilith Purge use Rang 2–4 from the sheet.
- Sora’s warp is distance 1–3 (sheet: Rang 1–3), both directions.
- Facing on the board flips with the turn button. Sora’s back-attack mark matches same-cell, same-facing.

## Kept from the unpublished v0.9.24 pass

- Lorebook lists only the heroes in the party (or the ones selected before start), plus the world text and glossary.
- Official card and hero names are not half-translated.

## Not changed on purpose

- Night still fights first, then food, ally upkeep, and weakness. Rulebook §20 lists food before the fight. The later ruling is “straight to combat,” and the rest of the current Night flow stays.
- Oni Echo’s sheet line says Melee 1 Target. Zemaki’s basic attack, and this skill, still hit the same cell only.
- Skills that only say “ระยะ N” and are implemented in both directions (for example Open Wound) were not rewritten to facing-only. Rulebook §30 says facing matters for attacks; it does not say every ranged line is forward-only.
- Safe Passage still does not bring allies along (already marked in the build).
- Bleed still ticks per cell stepped, while the rulebook counts one Hp per move action.
