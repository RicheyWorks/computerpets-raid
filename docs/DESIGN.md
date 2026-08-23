# Raid design

Implement against this file, not folklore.

## Identity

- Product: **Raid**
- Repo: `computerpets-raid`
- Idea: Pet Boss Raids
- Genre: Co-op raid
- Engine: Spring WebSockets
- Surface: `8096`

## Loop

One Rui cannot punch a weekly titan. Raid is the MMO slice: Visitation presence + WebSockets. Damage is care-stat scaled. Loot is shared cosmetics.

## Play beats

- Schedule a raid window.
- Bring 12–40 pets (one per player, or kennel support NPCs).
- Phases. Wipe = all tired, nobody burned.
- Loot via Ledger, bind-on-pickup cosmetics.

## Neighbors

- computerpets-visitation
- computerpets-companion
- computerpets-overlay
- computerpets-ledger
- computerpets-stampede (load)

## Failure doctrine

Desync → boss pauses. Stampede-tested to 10k presence, raid cap is lower on purpose. Cheat damage → kick, log Forensics.

## Hard rules

1. Minigames cannot mint or burn NFTs by themselves (Minter is the write path).
2. Stats come from lived overlay care + Dojo caps, not cash shop.
3. Species kits stay inside Lore. Illegal hybrids never spawn.
4. Fail soft: the desktop overlay process is not this process.
