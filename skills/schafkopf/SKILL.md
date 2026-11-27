---
name: schafkopf
description: Rules, terminology and basic strategy of Schafkopf, the Bavarian trick-taking card game, following the official rules of the Schafkopfschule e.V. (successor of the Bavarian Schafkopf rules of 2007) and its tournament rules (Turnierregeln). Covers Rufspiel/Sauspiel, Solo, Wenz, Farbwenz, Geier, Farbgeier, Tout, Sie, bidding (Spielverhandlung), Rufsau duties, Davonlaufen, Laufende, Schneider/Schwarz, Stoß/Kontra, tariffs and tournament scoring, plus common house rules (Kurzes Blatt, Ramsch, Klopfen, Bock) and Bavarian card nicknames. Use this skill whenever Schafkopf comes up — explaining rules, settling a dispute at the table, checking whether a card or call was legal, scoring or settling up a hand, analysing or simulating deals, or implementing the game in code — and whenever the user writes Schafkopf jargon such as Sauspiel, Rufsau, Wenz, Davonlaufen, Spritze, Laufende, Schneider or "Hundsgfickte", even if they never name the game.
license: MIT
metadata:
  version: "1.1"
---

# Schafkopf

Four-player trick-taking game from Bavaria. Tricks are worth card points (*Punkte*, *Augen*); the declaring side needs **61 of 120** to win, the defence only **60**. In the most common game (*Rufspiel*) the declarer picks a partner by calling an ace (*Sau*), and nobody knows who the partner is until that ace is played.

## Authority

This skill follows two documents of the **Schafkopfschule e.V.** (Munich), which maintains the Bavarian standard rules first adopted in 2007 and revised in 2024:

1. **Schafkopfregeln, April 2024** — the binding core of the game. Section numbers like *(R 5.1.5)* refer to it.
2. **Turnierregeln, January 2020** — additional rules for tournaments. Referenced as *(T 6)*.

The rulebook explicitly leaves tariffs, extra game types and handling of rule violations to each table (*Spielrunde*) or tournament organiser (R 3.1.2, R 7.3.1). Anything outside these documents is marked **not in the official rules**. Tables differ most in tariffs, allowed games and doubling, and those change who wins how much — so when scoring, analysing or implementing, say which rule set you apply, and if the user plays at a private table, ask about their agreements instead of assuming.

### Where to look

This file holds the core rules. Read a reference only when the task needs it:

| Task | Read |
|---|---|
| Tournament play, tournament scoring, Tout approval | [references/tournament.md](references/tournament.md) |
| Kurzes Blatt, Ramsch, Klopfen/Legen, Bock, Stock, Muss | [references/house-rules.md](references/house-rules.md) |
| Explaining or checking a whole hand step by step | [references/worked-example.md](references/worked-example.md) |
| Translating jargon (Schmieren, frei, blank, …) | [references/glossary.md](references/glossary.md) |
| Advice on which game to play or how to play it | [references/strategy.md](references/strategy.md) |

## Cards

32 cards (*lange Karte*), German-suited, preferably the *Bayerisches Kartenbild*. Four players, eight cards each, all cards dealt (R 1.2).

| Suit (*Farbe*) | Letter |
|---|---|
| Eichel (acorns) | E |
| Gras (leaves; also *Laub*, *Grün*, *Blatt*) | G |
| Herz (hearts) | H |
| Schellen (bells) | S |

| Rank | Symbol | Punkte |
|---|---|---|
| Sau (ace; properly the *Daus*) | A | 11 |
| Zehn (*Zehner*) | 10 | 10 |
| König | K | 4 |
| Ober | O | 3 |
| Unter | U | 2 |
| Neun | 9 | 0 |
| Acht | 8 | 0 |
| Sieben | 7 | 0 |

4 × 30 = **120 Punkte** (R 1.2.3). Zero-point cards are colloquially *Spatzen* or *Luschen*.

Notation used here: suit letter + rank symbol, e.g. `EO` (Eichel-Ober), `GU`, `HA` (Herz-Sau), `S10`.

### Nicknames (colloquial, regional)

| Card | Nickname |
|---|---|
| EO | *der Alte* |
| GO | *der Blaue* |
| EA (Eichel-Sau) | *die Alte* |
| GA (Gras-Sau) | *die Blaue* |
| SA (Schellen-Sau) | *die Hundsgfickte* |
| any Unter | *Wenz* (plural *Wenzen*) |

"Ich spiel auf die Hundsgfickte" = Rufspiel calling the Schellen-Sau.

## Game types

### Trumps per game

Within Ober and Unter the suit order is always **Eichel > Gras > Herz > Schellen**. The Zehn ranks directly below the Sau.

| Game | Trumps, highest first | # trumps | Plain suits, highest first |
|---|---|---|---|
| Rufspiel | EO GO HO SO · EU GU HU SU · HA H10 HK H9 H8 H7 | 14 | 3 suits × 6: A 10 K 9 8 7 |
| Solo (suit X) | EO GO HO SO · EU GU HU SU · XA X10 XK X9 X8 X7 | 14 | 3 suits × 6: A 10 K 9 8 7 |
| Wenz | EU GU HU SU | 4 | 4 suits × 7: A 10 K O 9 8 7 |
| Farbwenz (suit X) | EU GU HU SU · XA X10 XK XO X9 X8 X7 | 11 | 3 suits × 7: A 10 K O 9 8 7 |
| Geier | EO GO HO SO | 4 | 4 suits × 7: A 10 K U 9 8 7 |
| Farbgeier (suit X) | EO GO HO SO · XA X10 XK XU X9 X8 X7 | 11 | 3 suits × 7: A 10 K U 9 8 7 |

Trumps form their own suit: an Ober or Unter that is trump belongs **only** to trump, not to its printed suit. In a Rufspiel `EO` is not an Eichel card and `HA` is not a plain card.

### Rufspiel (*Sauspiel*, *Partnerspiel*) — 2 vs 2 (R 2.1)

Announced as *"ich spiele mit der Eichel-Sau"* (Gras-, Schellen-Sau). Colloquially *"auf die Alte"*, *"auf die Blaue"*, *"auf die Hundsgfickte"*.

- Only Eichel-, Gras- or Schellen-Sau can be called; the Herz-Sau is trump (R 2.1.3).
- The caller must **not hold** the called Sau and must hold **at least one plain card (*Farbkarte*) of that suit** (R 2.1.4). Ober/Unter don't count.
- A player who, in every one of the three suits, either holds the Sau or no card of the suit is **gesperrt** (blocked) and cannot play a Rufspiel. He must not reveal this by word, gesture or face (R 2.1.6).
- The holder of the called Sau (*der Gerufene*) is the declarer's partner; together they are the *Spielerpartei*, the other two the *Gegenspielerpartei*. The partner must not reveal himself before playing the Sau (R 2.1.5).

### Solo (*Farbsolo*) — 1 vs 3 (R 2.4)

*"Ich spiele ein Eichel-Solo"* (Gras-, Herz-, Schellen-). Ober, Unter and the chosen suit are trump. A Herz-Solo has the same trumps as a Rufspiel.

### Wenz — 1 vs 3 (R 2.3)

*"Ich spiele einen (farblosen) Wenz."* Only the four Unter are trump; Ober rank in their suit between König and Neun. A Wenz may be played without holding any Unter (R 2.3.5).

### Farbwenz — 1 vs 3 (R 2.2)

*"Ich spiele einen Gras-Wenz"* etc. The four Unter plus the chosen suit are trump (11 trumps).

### Geier and Farbgeier — 1 vs 3 (R 8.2, appendix)

Wenz and Farbwenz with the roles of Ober and Unter swapped. Described as "increasingly common" variants in the appendix; **not allowed in tournaments** (T 1).

### Tout (R 2.5)

A single player (Solo, Wenz, Farbwenz, Geier, Farbgeier) may add *Tout* to his **final** announcement: *"ich spiele ein Herz-Solo-Tout"*. He must take **every trick**; a single trick to the defence loses, even one worth 0 Punkte (R 2.5.3). Tout cannot be added after the final announcement (R 2.5.2). A Rufspiel cannot be Tout.

### Sie (R 2.6)

A player dealt **all four Ober and all four Unter** holds *Sie*. He may lay it down face up; it need not be played out. Highest game. Probability: 1 in 10,518,300 for a given player.

### Ranking (R 2.7, R 8.2.2)

| Without Geier | With Geier/Farbgeier |
|---|---|
| 1. Sie | 1. Sie |
| 2. Solo-Tout | 2. Solo-Tout |
| 3. Wenz-Tout | 3. Wenz-Tout |
| 4. Farbwenz-Tout | 4. Geier-Tout |
| 5. Solo | 5. Farbwenz-Tout |
| 6. Wenz | 6. Farbgeier-Tout |
| 7. Farbwenz | 7. Solo |
| 8. Rufspiel | 8. Wenz |
| | 9. Geier |
| | 10. Farbwenz |
| | 11. Farbgeier |
| | 12. Rufspiel |

Equal games: **seat order alone decides** — the player closer to the dealer's left wins. The trump suit of a Solo or Farbwenz does not matter for rank.

## Seating, shuffling, dealing (R 3)

- Four players sit crosswise. The first dealer is player 1; the deal passes clockwise, so each player deals once per **Runde** of four games (R 3.3.4).
- **Seats**, relative to the dealer (*Geber*): the player on the dealer's left is **Vorhand** (*erster Spieler nach dem Geber*): he declares first and leads the first trick. Traditionally followed by **Mittelhand** and **Hinterhand**; the dealer plays last. (The rulebook itself just counts "erster Spieler nach dem Geber".)
- **Mischen**: the dealer shuffles properly; riffled cards must be shuffled again before the cut (R 3.2.3). Objections must be raised before looking at one's own cards (R 3.2.9).
- **Abheben**: the player on the **dealer's right** cuts. At least 3 cards taken off and at least 3 left; at most three cuts (R 3.2.5–6). Instead, players may agree to a short re-shuffle by that player (*nachmischen*, R 3.2.12) — mandatory in tournaments (T 3).
- **Geben**: clockwise, starting left of the dealer, **4 + 4** cards; optionally **4 × 2** (R 3.3.1) — 4 × 2 in tournaments (T 3).
- Misdeals (card face up, wrong count): reshuffle and redeal (R 7.1.1–2).

## Bidding (*Spielansage*, R 4)

### Declaration round (*Spielerklärung*)

Starting with Vorhand, each player says once, clearly (gestures are not enough):

- **"weiter"** — no interest; or
- **"ich möchte spielen"** / **"ich möchte auch spielen"** — without naming the game.

Both are binding (R 4.1.1). Minimum game implied by the declaration (R 4.1.2):

| Declaring player | Must have at least |
|---|---|
| 1st to declare interest | Rufspiel |
| 2nd | Farbwenz |
| 3rd | Wenz |
| 4th | Solo |

There is no further requirement on the hand: number of trumps or quality of side cards is irrelevant (R 4.1.6). A player who said "weiter" must not hint that he had considered playing (R 4.1.4).

### All pass

If all four say "weiter", the cards are **thrown in** (*zusammengeworfen*) and the **next dealer** deals (R 4.1.5). Other agreements (e.g. *"der Alte muss spielen"* — the holder of EO must play; paying into a *Stock*) may be made before the session. **Tournament: the same dealer deals again** until a game comes about (T 4).

### Negotiation (*Spielverhandlung*, R 4.2)

With two or more interested players:

1. The **later** of the first two names the rank of his game, never its suit: *"ich hätte (mindestens) einen Wenz"*.
2. The earlier player answers *"ich möchte selbst spielen"* (he has at least an equal game — seat priority) or *"weiter"*.
3. If the earlier one holds, the later one may raise (*"dann hätte ich einen Wenz-Tout"*), until one says "weiter".
4. The winner then negotiates with the 3rd interested player the same way, then with the 4th.
5. Only after everyone has declared does the winner make the **final announcement** *"ich spiele …"* with game type and suit (called Sau, Solo or Farbwenz suit). It is binding (R 4.2.5).

Examples (R 8.1):

- P1 has Rufspiel, P2 has Solo. P1 "ich möchte spielen", P2 "ich möchte auch spielen", P3/P4 "weiter". P1 "weiter" (P2 must have at least a Farbwenz). P2 "ich spiele ein Herz-Solo".
- P1 Wenz, P2 Farbwenz, P3 Solo; all three declare. P1 "ich möchte selbst spielen", P2 "weiter". P3 "ich hätte (mindestens) ein Solo", P1 "weiter", P3 "ich spiele ein Eichel-Solo".

## Play (R 5)

- **Vorhand leads** any card. Play proceeds clockwise — the player on the left of whoever just played is next; the winner of a trick leads the next (R 5.1.1, R 5.2.6).
- **Bedienpflicht** (must follow): if a suit is led, play a card of that suit if you have one; if trump is led, play a trump if you have one. Otherwise any card (R 5.1.2).
- **No obligation to beat or to trump** (*keine Stichpflicht*, R 5.2.3).
- Trick winner: highest trump if any trump was played, otherwise highest card of the led suit (R 5.2.1–2).
- *"Was liegt, das liegt"*: a played card cannot be taken back (R 5.1.8). The last trick may be looked at again until the next trick is turned (R 5.2.8).
- Every game is played to the last card (R 5.1.7). Throwing in one's cards early is forbidden; in tournaments it loses the game (T 11).
- Anyone may ask at any time who led, which Sau was called, who played which card, who played the Rufsau, and which suit is trump (R 5.1.9).
- Audibly counting trumps or points is not allowed (R 5.4.4).

### Rufsau rules (R 5.1.3–6)

The called Sau is the *Rufsau*, its suit the *Ruffarbe*. The suit is **gesucht** ("searched") when it is led for the first time.

1. When the Ruffarbe is led, the partner **must play the Rufsau** — even if a smaller card of that suit would do.
2. The partner **must not play the Rufsau** on a trick where the Ruffarbe was not led. If it is never searched, he may play it only in the **8th (last) trick**.
3. The partner may **lead the Rufsau himself** at any time.
4. While holding the Rufsau, the partner must not lead **any other card** of the Ruffarbe —
5. — **except Davonlaufen**: if, at the time of leading, he holds **at least four cards of the Ruffarbe including the Sau**, he may lead a smaller card of that suit ("unter der Sau ausspielen").
6. After Davonlaufen the Rufsau is an ordinary card: it may be played anytime and need not be played when the suit is led again.

Davonlaufen is only possible when the partner himself is on lead; if someone else leads the Ruffarbe first, rule 1 applies.

## Stoß (Kontra) (R 5.3)

- A defender who believes his side will win may give a **Stoß** (also *Kontra*, *Spritze*).
- Allowed before or after the first card is led, but **not once the second player's card has been played or shown**.
- The declarer **or his called partner** may answer with a **Retour-Stoß** (*Retour*), also before the second card.
- The called partner must not give a Stoß (that is a rule violation, R 7.2.4) — but he may give the Retour.
- A Stoß changes no thresholds: the declaring side still needs 61, and 31 to avoid Schneider (*"Spieler bleibt Spieler"*).
- Stoß doubles the amount, Retour quadruples it (R 6.2.8).
- **Tournament: Spritze (Kontra) is not allowed** (T 1).

## Result (R 6.1)

| | Declaring side (*Spielerpartei*) | Defence (*Gegenspielerpartei*) |
|---|---|---|
| Wins with | **≥ 61** | **≥ 60** |
| Loses Schneider with | **≤ 30** | **≤ 29** |
| Schwarz | took no trick | took no trick |

So 60:60 is a loss for the declaring side. The declaring side needs 31 to be *schneiderfrei*, the defence 30. Schwarz means **no trick at all** — a trick of 0 Punkte prevents Schwarz (R 6.1.4).

Etiquette (R 5.4.2): Schneider is a matter of honour and must be announced and paid by the losers unasked; Schwarz must be claimed by the winners.

## Payout (R 6.2)

Tariffs are free; the rulebook describes the common practice. A tariff has three prices:

- **Rufspiel** price, commonly 10 or 20 ct,
- **Einzelspiel** price (Solo, Wenz, Farbwenz alike), commonly 50 ct,
- **Grundeinheit** (unit) for Schneider, Schwarz and each Laufender, commonly 10 ct.

In abstract units: unit **G** = Grundeinheit, Rufspiel = 1–2 G, Einzelspiel **E** = 5 G.

### Laufende (R 6.2.2–4)

Consecutive top trumps held by one side (combined hands in a Rufspiel), counted from the highest trump down without a gap. Held by the declaring side: *"mit drei"*; held by the defence: *"ohne drei"* — both count and are paid to **whichever side wins**.

| Game | Laufende paid from |
|---|---|
| Rufspiel, Solo | 3 (EO GO HO) |
| Farbwenz | 3 (EU GU HU) |
| Wenz | 2 (EU GU) |

Maximum per the rulebook: 14 in a Rufspiel, 8 in a Solo or Farbwenz, 4 in a Wenz. (By the definition above a Solo run could reach 14 and a Farbwenz run 11; the rulebook's lower figures are quoted as written — if it matters, say so and ask which applies.) Laufende are paid only if the winners claim them before the next cut; over-claimed Laufende can be reclaimed double (R 6.2.4).

### Amount per game

| Component | Amount |
|---|---|
| Rufspiel | Rufspiel price |
| Solo, Wenz, Farbwenz | E |
| Schneider | + G |
| Schwarz | + G (in addition to Schneider) |
| each Laufender | + G |
| Tout | 2 × (E + Laufende); Schneider/Schwarz usually not counted |
| Sie | 4 × (Solo with 8 Laufende) = 4 × (E + 8 G); Schneider/Schwarz usually not counted |
| Stoß / Retour | × 2 / × 4 on the final amount |

**Who pays:** Rufspiel — two winners, two losers, **each loser pays one winner** the amount. Single game — each of the three defenders pays the declarer, or the declarer pays each of them (R 6.2.9).

**Example** (Rufspiel 10 ct, E = 50 ct, G = 10 ct): Gras-Solo won Schneider, "mit vier" (EO GO HO SO), Stoß: (50 + 10 + 4 × 10) × 2 = 200 ct from each defender.

**Example**: Rufspiel lost 60:60, "ohne drei": 10 + 3 × 10 = 40 ct, each of the two losers pays one winner.

## Rule violations (R 7)

Typical violations (R 7.2): any utterance or behaviour revealing game-relevant information or prompting a co-player; breaking the bidding rules; invalid announcement; Stoß by the called partner; Stoß/Retour after the second card; playing out of turn (*vorwerfen*; allowed in the last trick); revoking (breaking Bedienpflicht); the partner leading a small card of the Ruffarbe with fewer than four cards before it was searched; playing the Rufsau before it was searched or before Davonlaufen; holding a wrong number of cards; looking further back than the last trick; showing or laying down cards early.

Penalties are left to the table or organiser (R 7.3.1); the deciding question is whether the violation revealed the game. If the innocent side chooses to play on, the actual result counts (R 7.3.2). In tournaments, cheating or repeated revoking leads to disqualification (T 12).

Accidents (R 7.1): a card turned during the deal → reshuffle; wrong number of cards after the deal → redeal; dealing out of turn is void unless someone has looked at a card, in which case it is played; an accidentally exposed card during pickup is ignored.

## Common mistakes

These are the points where intuition from other card games leads astray:

- **Ober and Unter change suit with the game.** In Rufspiel and Solo they are trump and belong to no suit, so `EO` cannot follow an Eichel lead; in Wenz/Farbwenz only the Unter are trump and the Ober are ordinary suit cards (Geier: the reverse). Decide suit membership per game before checking Bedienpflicht.
- **The Zehn ranks above the König**, directly below the Sau.
- **No obligation to trump or overtake** — only to follow suit.
- **The thresholds are asymmetric**: the declarers need 61 (the defence 60) and 31 to escape Schneider (the defence 30). Schwarz means zero tricks, not zero Punkte.
- **Rufspiel calls**: never Herz, never one's own Sau, always with a plain card of that suit. The Rufsau must be played when its suit is first led, and Davonlaufen needs four cards of the suit.
- **Tournaments differ**: no Kontra, no Geier, 4 × 2 deal, the same dealer redeals after all pass — see [references/tournament.md](references/tournament.md).

## Sources

- Schafkopfschule e.V., *Schafkopfregeln*, Stand April 2024 — https://schafkopfschule.de/regeln.html
- Schafkopfschule e.V., *Turnierregeln*, January 2020 — same page.
