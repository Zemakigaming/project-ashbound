# Ashbound v0.9.26

Playable file: `ashbound_v0.9.26.html`. `index.html` is the same file, so the public page serves this version. Older versioned HTML files are unchanged.

Sheet dated 7 Nov 2026 wins over the attached rulebook text (that file is labeled 1.6 and still matches the 3 Nov PDF).

## Sheet logic

- Mina Charge costs 5 (Encore and Rainbow Warp).
- THE CURSED SEER ริน่า is MES-002: 30 HP, speed 7, walk 3, melee 1 target, 4 damage, bonus Y. A hit applies เลือดสาด and she steps up to 4 cells away. The old shriek is gone.
- AMY: Str 1, Atk 1, range 1–3. She grants +1 Move, and the first attack this turn spends that extra step.
- ALICE rolls her own W. Face 1–3 heals 1 HP to one hurt friend in her cell.
- AVA Elite: Dex 2, Int 0, Atk 3, melee all enemies in range. End of round, D6 1–3 hits enemies in her cell and the cells beside it; 4–6 hits those cells including survivors and allies.
- Bicycle no longer discounts food. Joining a friend’s fight does not spend the next action. Other actions still cost an action.
- สร้อยรินา (IT-020): +2 Int while worn, and 2 HP at the start of each combat round. No shop price in the sheet.
- รองเท้าหนัง is IT-031. Same first-round extra die. The invented name and price are gone, and it is not in the shop.
- พลุไฟ is IT-02. IT-018 is not in this catalog.

## Still unresolved

- Night still fights first, then food and weakness. The rulebook lists food before the fight.
- Oni Echo still uses Close Melee (same cell), matching Zemaki’s basic attack.
- Skills that only say “ระยะ N” and already hit both ways were not rewritten to facing-only.
- Safe Passage still does not bring allies. เลือดสาด still ticks once per cell stepped.
- ALICE’s “(1–3)” is her own white die, not a die the owner already placed.
- Boss HP still scales with party size. Four players get the sheet’s 30 HP.
- IT-020 and IT-031 have no drop or shop row in the sheet, so they only work if the character is already wearing them.
- Summon and facing cases the sheet does not specify stay as they were.

# Ashbound v0.9.25

New file only. v0.9.23 and older builds are unchanged. The live page now points at v0.9.26.

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
