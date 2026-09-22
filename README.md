# PokeStonks

A Pokémon-style game where **stock tickers are the monsters**. Roam a pixel town, get pulled into a **live 1v1 battle** against another player (or a bot), and when you win, claim **synthetic stock tokens and a BrokerMon NFT** on Monad testnet with your own wallet.

**Play:** https://pokestonkss.vercel.app · works on desktop and phone, no install.

---

## Play in 60 seconds

1. Open **https://pokestonkss.vercel.app**.
2. **Play as guest** (instant) or **Connect wallet** (needed only to claim rewards).
3. **Choose your BrokerMon.** Each one is a stock with its own type and moves.
4. On the globe, tap a **market pin**, then **Enter route**.
5. Walk into the **tall dark grass**. About 1 step in 9 starts an encounter.
6. Win the battle, press **Claim reward**, approve in your wallet. The tokens land in your wallet.

Want to fight a friend? While you're in a route, press **Duel** (top right) → **Host a duel**, read out the 5‑letter code, and they press **Duel** → type the code → **Join**.

---

## Controls

| Action | Keyboard | Phone / touch |
|---|---|---|
| Move | Arrows or WASD | On-screen D-pad |
| Run | Hold Shift | Hold **B** |
| Talk, read signs, confirm | Z, Space or Enter | **A** button / tap |
| Back / cancel | X | — |
| Leave the route | Esc, or the exit sign at the edge of town | Walk to the exit sign at the edge of town |
| Battle menus | Arrows + Z / Enter | Tap the button |
| Tap-timing bar | Space, Z or click | Tap anywhere |

On a phone, turn it sideways for the biggest view.

---

## Game modes

| Mode | How to start | Opponent | Reward on win |
|---|---|---|---|
| **Wild encounter** | Walk in tall grass | A real player searching at the same time; if nobody joins within **20 s**, a Broker bot from that route | 0.02 s‑token vs bot, 0.10 vs a human (+ NFT) |
| **Trainer battle** | A rival NPC spots you (walk into their line of sight) | Same live matchmaking, with a trainer intro | Same as above |
| **Private duel** | **Duel** → Host / Join with a 5‑letter code | Your friend, on any device | 0.10 s‑token + BrokerMon NFT |

Every battle is decided by the **server**, not your browser: the client only sends "this move, this tap result". Nobody can edit HP, stats or dice rolls.

---

## How battles work

**Turn flow.** Both players pick a move at the same time (30 s timer, top right). The server resolves the turn and both screens play the exact same animation sequence. If your timer runs out, your first available move is used automatically.

**Menu.**
- **FIGHT** – your 4 moves, with type, power, accuracy, PP and a "super effective / not very effective" hint against the current opponent.
- **STATS** – both BrokerMon's live stats and stat changes.
- **MARKET** – the live market mood of both tickers (see below).
- **RUN** – forfeit the match (the opponent wins).

**Tap-timing bar.** Every attack opens a bar with a sweeping needle. Stop it:
- in the **green center** → **Perfect**: guaranteed critical hit (2×) and +10%
- in the **orange** → Good: normal damage
- at the **red edges** → Miss: −15% and an extra 10% chance to miss outright

**Damage** uses the real Gen‑3 formula: level, Attack vs Defense (Sp. Atk vs Sp. Def for non‑Normal moves), 1.5× same‑type bonus, type effectiveness, 6.25% natural crits, 85–100% random spread. Stat moves (Growl, Swords Dance, Agility, Calm Mind…) raise or lower stats in stages from −6 to +6. Higher priority (Quick Attack) goes first, then the faster BrokerMon.

**Type chart** (attacker ↓ vs defender →):

| | Normal | Electric | Grass | Fire | Water | Psychic |
|---|---|---|---|---|---|---|
| **Normal** | 1 | 1 | 1 | 1 | 1 | 1 |
| **Electric** | 1 | ½ | ½ | 1 | **2** | 1 |
| **Grass** | 1 | 1 | ½ | ½ | **2** | 1 |
| **Fire** | 1 | 1 | **2** | ½ | ½ | 1 |
| **Water** | 1 | 1 | ½ | **2** | ½ | 1 |
| **Psychic** | 1 | 1 | 1 | 1 | 1 | ½ |

**Market mood.** Live Pyth prices move the fight. If a stock trades more than **2% above** its average, its BrokerMon hits **10% harder** (bull); more than 2% below, **10% softer** (bear). When US markets are closed the last price is used; if no price is available the mood is neutral.

**Ending a battle.** You win when the other BrokerMon faints, or if they run, time out 3 turns in a row, or lose connection for more than **30 s** (you get the same 30 s to reconnect if your connection drops).

---

## The 12 BrokerMon

| Ticker | Name | Type | Sector | Moves |
|---|---|---|---|---|
| AAPL | Applon | Normal | Blue-chip | Tackle, Body Slam, Swords Dance, Quick Attack |
| MSFT | Microsaur | Normal | Blue-chip | Body Slam, Quick Attack, Growl, Tail Whip |
| TSLA | Teslaq | Electric | Tech | Thunderbolt, Thunder Shock, Quick Attack, Agility |
| NVDA | Nvidra | Electric | Tech | Thunderbolt, Thunder, Confusion, Calm Mind |
| XOM | Exxonyx | Grass | Energy | Razor Leaf, Vine Whip, Growl, Body Slam |
| CVX | Chevrune | Grass | Energy | Razor Leaf, Vine Whip, Tail Whip, Quick Attack |
| GME | Gamestomp | Fire | Growth | Flamethrower, Ember, Quick Attack, Growl |
| AMD | Amdrake | Fire | Growth | Flamethrower, Ember, Quick Attack, Agility |
| AMZN | Amazoo | Water | Consumer | Surf, Water Gun, Body Slam, Tail Whip |
| NKE | Nikefin | Water | Consumer | Surf, Water Gun, Quick Attack, Growl |
| COIN | Coinix | Psychic | Crypto | Psychic, Confusion, Calm Mind, Quick Attack |
| MSTR | Stratyr | Psychic | Crypto | Psychic, Confusion, Agility, Tackle |

All BrokerMon fight at level 50. Change yours any time from the globe (swap icon, top right).

---

## Routes (maps)

Each globe pin is a route in the company's home city. Every route is a hand‑styled town with:

- **The Exchange** – walk in and talk to the Teller to fully heal.
- **Tall grass** – 4 patches; wild BrokerMon from that route's pool.
- **Rival trainers** – walk into their line of sight and they challenge you.
- **Townsfolk** – wander and chat; signs explain the area.
- **An exit sign** at the edge of town to go back to the globe.

| Route | City | Theme |
|---|---|---|
| Apple Route | Cupertino | Blue-chip meadow |
| Redmond Route | Redmond | Blue-chip meadow |
| Gigafactory Route | Austin | Tech (server racks) |
| Silicon Route | Santa Clara | Tech |
| Markham Route | Markham | Tech |
| Oilfield Route | Spring | Energy (pump-jacks) |
| Refinery Route | San Ramon | Energy |
| Wall Street Route | New York | Meme (neon) |
| Harbor Route | Seattle | Consumer (shopfronts) |
| Track Route | Beaverton | Consumer |
| Ledger Route | San Francisco | Crypto (obelisks) |
| Treasury Route | Tysons | Crypto |

The theme also decides the battle backdrop and which BrokerMon you meet in the grass.

---

## Rewards and claiming

**What you win:** synthetic tokens of **the stock you defeated** (beat Amazoo → sAMZN).

| You beat | Tokens | NFT |
|---|---|---|
| A human player | 0.10 | A BrokerMon NFT of that species (fully on-chain art) |
| A Broker bot | 0.02 | — |

The live market mood adds **+10%** (bull) or **−10%** (bear) to the payout, verified on-chain from Pyth at claim time.

**How a claim works:**
1. You win and press **Claim reward**.
2. If no wallet is connected, a dialog lets you pick one (MetaMask, Rabby, any browser wallet).
3. The battle server signs a one-time voucher for your wallet.
4. Your wallet pops up, switches to **Monad Testnet**, and asks you to confirm `claim`. You pay a tiny MON network fee.
5. The tokens (and NFT) are minted straight to your wallet. See them under **Collection** (grid icon).

Rules: one claim per battle, voucher valid 30 minutes, at most 12 claims per wallet per hour. Tokens are **testnet-only, synthetic, with no cash value**.

**Getting set up:**
- Wallet network: **Monad Testnet**, chain ID `10143`, RPC `https://testnet-rpc.monad.xyz`, currency `MON`, explorer `https://testnet.monadvision.com`. The game adds/switches it for you.
- Free testnet MON: https://faucet.monad.xyz
- **On a phone:** open the game inside the **MetaMask app's browser** (the connect dialog has a button for it) to claim.

---

## Architecture

```
 Browser (Vercel)                       Battle server (Render)              Monad testnet
 ───────────────────────                ──────────────────────              ───────────────────────
 Next.js 16 + React 19                  Colyseus 0.18 (websockets)          BattleArena  (claims, EIP-712)
 Globe: MapLibre + PixelBlast   ◄─ws─►  Authoritative BattleRoom            SyntheticStock ×12 (sAAPL…)
 Game: Phaser 3 (overworld,             Matchmaking, bots, duels,           BrokerMonNFT (on-chain SVG)
       battle, cutscenes)               reconnects, anti-cheat              Pyth price feeds
 wagmi (wallet) ──────── claim tx ─────────────────────────────────────────►
                                        Signs reward vouchers (no gas)
 /api/spawns ── Pyth Hermes             Pyth Hermes (market mood)
```

| Folder | What it is |
|---|---|
| `apps/web` | The game website: title, BrokerMon select, globe, Phaser game, wallet, collection |
| `apps/server` | Authoritative battle server + reward voucher signer |
| `packages/game-core` | Shared rules: species, moves, type chart, damage, encounters, protocol (used by both web and server) |
| `packages/contracts-abi` | Contract ABIs and deployed addresses |
| `contracts` | Solidity (Foundry): BattleArena, SyntheticStock, BrokerMonNFT |

All art (monsters, tiles, towns, backdrops) and all music/sound effects are generated in code and original to this project.

### Deployed contracts (Monad testnet, chain 10143)

| Contract | Address |
|---|---|
| BattleArena | [`0x41930014D474415F0e9882DE82434f336502f5B0`](https://testnet.monadvision.com/address/0x41930014D474415F0e9882DE82434f336502f5B0) |
| BrokerMonNFT | [`0x7FDcf540e9897879ECd2aabF8055392fA86B363d`](https://testnet.monadvision.com/address/0x7FDcf540e9897879ECd2aabF8055392fA86B363d) |
| sTSLA / sAAPL / … | See [`packages/contracts-abi/deployments.json`](packages/contracts-abi/deployments.json) (12 tokens) |
| Pyth | `0x2880aB155794e7179c9eE2e38200202908C17B43` |

---

## Run it locally

Needs **Node 22+** and **pnpm 10** (`corepack enable`).

```bash
git clone https://github.com/Abhishek222983101/pokestonks.git
cd pokestonks
pnpm install

pnpm dev:server      # battle server  → ws://localhost:2567   (health: http://localhost:2567/health)
pnpm dev:web         # game website   → http://localhost:3000
```

Open http://localhost:3000. Everything is playable with no keys. To turn on **rewards** and **live prices** locally, create these files (they are gitignored):

`apps/server/.env`
```
ARENA_ADDRESS=0x41930014D474415F0e9882DE82434f336502f5B0
CLAIM_SIGNER_PRIVATE_KEY=0x...   # must be the arena's voucher signer
PYTH_API_KEY=...                 # free: https://docs.pyth.network/price-feeds/pro/acquire-api-key
```
`apps/web/.env.local`
```
PYTH_API_KEY=...                 # prices on the globe
# NEXT_PUBLIC_COLYSEUS_URL=ws://localhost:2567   (default)
```

Two players on one computer: use two different browsers (or one normal + one incognito window), not two tabs of the same browser.

---

## Deploy your own

**1. Contracts (Monad testnet).** Needs [Foundry](https://getfoundry.sh) and ~3.5 MON.
```bash
cp contracts/.env.example contracts/.env      # set PRIVATE_KEY=0x...
./contracts/deploy-testnet.sh                 # tests, deploys 14 contracts, exports ABIs, writes apps/server/.env
```

**2. Battle server → Render** (websockets can't run on Vercel). `render.yaml` and a root `Dockerfile` are included.
Create a Docker web service from this repo, health check `/health`, and set:

| Variable | Value |
|---|---|
| `ARENA_ADDRESS` | your BattleArena address |
| `CLAIM_SIGNER_PRIVATE_KEY` | the arena's voucher signer key (secret) |
| `PYTH_API_KEY` | Pyth key (secret) |
| `RPC_URL` | `https://testnet-rpc.monad.xyz` |

**3. Website → Vercel.** Import the repo, **Root Directory `apps/web`**, enable "Include files outside the root directory". Set:

| Variable | Value |
|---|---|
| `NEXT_PUBLIC_COLYSEUS_URL` | `wss://<your-render-service>.onrender.com` |
| `NEXT_PUBLIC_RPC_URL` | `https://testnet-rpc.monad.xyz` |
| `PYTH_API_KEY` | Pyth key |

Pushes to `main` deploy production; pushes to `staging` deploy a preview.

---

## Testing

```bash
pnpm typecheck                     # all packages
pnpm test                          # game rules (50) + server incl. real-websocket battles (30)
pnpm test:contracts                # Foundry: 109 tests
pnpm --filter server smoke wss://pokestonkss-server.onrender.com   # play a full battle against a live server
SERVER_URL=wss://pokestonkss-server.onrender.com \
  pnpm --filter server exec tsx scripts/testnet-claim.mts          # battle + real on-chain claim (uses contracts/.env key)
```

---

## Troubleshooting

| Problem | Fix |
|---|---|
| "Can't reach the battle server" | The free Render server may be waking up. Wait ~30 s and try again. |
| Wallet asks for the wrong network | Approve the switch to Monad Testnet (chain 10143). |
| "Needs a little MON" | Get testnet MON at https://faucet.monad.xyz |
| No wallet on my phone | Open the game inside the MetaMask app (button in the connect dialog). |
| Market mood always flat | Prices are within 2% of their average (common when markets are quiet or closed), or the server has no Pyth key. |
| Friend can't join my duel | Codes are 5 letters/numbers without I, O, 0 or 1. The host must stay on the "Duel code" screen. |

---

## Security

- The server holds **no gas money** and sends no transactions. It only signs vouchers; the winner's wallet submits them.
- The contract accepts a voucher only once per battle, only before its deadline, only from the configured signer, and pays only the address inside the voucher.
- Stats come from the species on the server; anything the client sends besides "move + tap result" is ignored.
- Your chosen move stays hidden from the opponent until the turn resolves.

## Credits

Built for Monad Blitz. Prices by [Pyth Network](https://pyth.network). Font: Press Start 2P (SIL OFL). Everything else, including art and audio, is original.
