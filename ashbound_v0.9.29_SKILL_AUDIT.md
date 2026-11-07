# Ashbound v0.9.29 skill and minion audit

Invoked in the browser against v0.9.29. Not a string compare.

## Minion kill (bloom, sheet ≥ 2)

Minions have no HP. One hit is compared with the sheet threshold. Damage below the threshold knocks the minion down; the next hit destroys it. Hits are not added together into a fake HP pool.

Clicked in the combat UI:

| Attack | Shown before | Result |
| --- | --- | --- |
| Rapid Volley 2 damage ×1, opening-fight flag on | ฆ่าทันทีเมื่อดาเมจ ≥ 2 | That minion removed. The grove beside it (≥ 3) stayed. |
| Rapid Volley exactly 2 ×1 | same label | Killed. Log: สังหาร |
| Rapid Volley 4 ×1 | same label | Killed. Sibling stayed. |
| Rapid Volley 1 ×1 | same label | Not killed. Label becomes ล้มแล้ว · โดนอีกครั้งจะตาย |
| Basic attack 2 | ☠ สังหาร (ต้อง ≥2, ได้ 2) | Killed |
| Basic attack 1 | ล้ม (ต้อง ≥2 จึงตาย, ได้ 1) | Not killed |
| Basic attack 3 | ☠ สังหาร (ต้อง ≥2, ได้ 3) | Killed |
| Petunia elite | 14/14 | Unchanged when not targeted |

v0.9.28 failed the opening fight: the button said 4 damage ×2, both hits were discarded, and the card still showed 2/2. Cause: round 1 of the tutorial fight ignored every hit, and the minion was drawn as if it had 2 HP.

## Skills

60 skills × level 1 and level 2 = 120 calls of the live resolver, with a target in cells 0–3.

- 116 calls returned without throwing.
- 4 calls (Hold the Line 14, Trap 15, both levels) threw only when the combat object was missing `noEnter` / `traps`. A real fight creates those. Not changed.
- 16 calls offered no target because the fixture lacked the sheet’s precondition (no one to pull, no bonus die, no used skill, no status to copy, no cell behind). Expected.

Spot checks with the skill’s own stat mods included:

- Rapid Volley L1: (Str+N) × floor(Dex/2), forward range 2–3, one target.
- Rapid Volley L2: hit count is Dex−2.
- Cinder Barrage: (Int+N) × floor(Dex/2), same range.
- Sweeping Arc: Str/2 at level 1, Str at level 2, melee all in range.
- Black Tide: Int (or Int×2) to every enemy in the same cell only.
- Eroding Halo: De-Armor, not damage. Level 1 is distance 2.
- Lights Out: Stun, same cell.

Ally hits, same resolver as players: sheriff’s child deals 1 and only knocks a bloom down; the officer deals 2 and destroys it. AMY is Str 1, Atk 1, range 1–3. ALICE heals 1 on her own white 1–3.

## Left as written

- Oni Echo still uses Zemaki’s same-cell attack. The sheet line says Melee 1 Target.
- Night still fights before food.
- A line that only says “ระยะ N” and already hits both ways was not rewritten to facing-only.
- Safe Passage still does not bring allies.
- Two Rapid Volley hits of 1 are two hits. The second hit is the sheet’s below-threshold second hit. They are not added into 2 damage.
- Boss HP still scales with party size. Four players get the sheet number.
