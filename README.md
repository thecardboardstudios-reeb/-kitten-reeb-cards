# Kitten & ReeB's House of Cards

A two-player browser card table with Crazy Eights and a simplified Gin Rummy variant. No accounts, passwords, databases, or build tools.

## Install on GitHub Pages

1. Download and unzip the supplied package.
2. Open your `kitten-reeb-cards` GitHub repository, choose **Add file → Upload files**.
3. Upload **index.html**, **style.css**, and **app.js** from the unzipped folder (to the repository root). Commit changes.
4. Wait for GitHub Pages to publish at `https://thecardboardstudios-reeb.github.io/kitten-reeb-cards/`.
5. Open the page on both laptops. One person clicks **Create table**, reads the six-character code aloud, and the other clicks **Join table**. The host chooses a game.

## GoDaddy embed

Paste this into your GoDaddy HTML / Custom Code section:

```html
<iframe src="https://thecardboardstudios-reeb.github.io/kitten-reeb-cards/" title="Kitten and ReeB's House of Cards" style="width:100%;height:850px;border:0;border-radius:12px" loading="lazy" allow="clipboard-write"></iframe>
```

If GoDaddy or the browser blocks the iframe, link directly to the GitHub Pages URL instead. Test the published page on both laptops before embedding.

## Important limits

- This is a **first playable version**, not a production-secure gambling or tournament system. It uses PeerJS's public signaling service and WebRTC peer-to-peer networking; some networks, firewalls, and browsers may block direct connections. If that happens, a dedicated relay or real-time backend is needed.
- Both players must be online simultaneously. If the host refreshes/closes the page, the table and scores reset.
- The room code is a convenience, **not authentication**. Anyone with the code could join first. Do not use real money or share sensitive information.
- **Crazy Eights** uses a standard 52-card deck, 7 cards each; play matching rank/suit or an eight to change suit; drawing one card ends the turn. This is *not* official UNO, and there are no skip/draw-two/draw-four cards.
- **Gin Rummy** uses 10 cards each, alternating draw/discard, valid 3+ card runs and sets, knock at 10 or fewer deadwood, gin +25, undercut +25. This simplified version **does not implement opponent layoff after a knock**. Ace is low. A player cannot immediately discard a card taken from the discard pile. Stock exhaustion draws the round.
- The app loads PeerJS from a CDN, so internet access is required even though GitHub Pages serves the game files.

## Troubleshooting

If the other laptop cannot join, refresh both pages, create a new table, and try again. Test in normal Chrome tabs first, not inside the GoDaddy embed. If it works in Chrome but not embedded, the iframe or browser policy is the issue.

## New: Draw Dominoes (beta)

Choose **Dominoes 🁣** from the game menu. This is a two-player, double-six draw-dominoes variant: seven tiles each, play to either end, draw from the boneyard until a play is available, and pass when the boneyard is empty. The first player to empty their hand wins the opponent's remaining pip total. If both players pass, the player with fewer remaining pips wins. Ties score zero. The existing peer-to-peer room and running scores are reused. This version has not yet been live-tested across two browsers, so keep a backup of your currently working website files before uploading.
