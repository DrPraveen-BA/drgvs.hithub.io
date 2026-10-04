# TRUST NO ONE

A real-time social deduction game for 4–10 players.

## Game loop

- Join with a room code. No account or install required.
- Everyone receives a secret role.
- The Crew must repair the ship before oxygen reaches zero.
- One or more players are secretly Saboteurs.
- Saboteurs do **not** learn who the other Saboteurs are.
- Players can repair, stabilize oxygen, investigate, secure systems, sabotage, plant evidence, chat, whisper, and call emergency votes.
- Votes reveal the ejected player's role.
- The game ends when the Crew repairs the ship / ejects all Saboteurs, or the Saboteurs drain oxygen / outlast the mission clock.

## Multiplayer architecture

The browser host is authoritative for shared game state. PeerJS provides browser-to-browser networking and room connectivity. Public state strips roles and secret missions before synchronization; each player receives their own private role payload.

## Run

Open `index.html` from a static web host. The page loads PeerJS from the public CDN.

## Challenge-ready MVP

This build focuses on the core required experience:
- room codes
- 4–10 player support
- synchronized timer, oxygen, repair progress, events, eliminations and votes
- hidden roles
- private player identity
- public chat
- peer-to-peer whispers
- responsive phone/laptop UI
- end-of-game role reveal

## Planned v2

Dynamic AI-generated events, richer evidence chains, persistent player stats, spectator mode, reconnection recovery, and a production server-authoritative backend.
