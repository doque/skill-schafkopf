---
name: schafkopf
description: Rules, terminology and basic strategy of Schafkopf, the Bavarian trick-taking card game, following the official rules of the Schafkopfschule e.V. (successor of the Bavarian Schafkopf rules of 2007) and its tournament rules (Turnierregeln). Covers Rufspiel/Sauspiel, Solo, Wenz, Farbwenz, Geier, Farbgeier, Tout, Sie, bidding (Spielverhandlung), Rufsau duties, Davonlaufen, Laufende, Schneider/Schwarz, Stoß/Kontra, tariffs and tournament scoring, plus Bavarian card nicknames. Use when explaining, analysing, scoring, simulating or implementing Schafkopf, or when a user uses Schafkopf jargon.
---

# Schafkopf

Four-player trick-taking game from Bavaria. Tricks are worth card points (*Punkte*, *Augen*); the declaring side needs **61 of 120** to win, the defence only **60**. In the most common game (*Rufspiel*) the declarer picks a partner by calling an ace (*Sau*), and nobody knows who the partner is until that ace is played.

## Authority

This skill follows two documents of the **Schafkopfschule e.V.** (Munich), which maintains the Bavarian standard rules first adopted in 2007 and revised in 2024:

1. **Schafkopfregeln, April 2024** — the binding core of the game. Section numbers like *(R 5.1.5)* refer to it.
2. **Turnierregeln, January 2020** — additional rules for tournaments. Referenced as *(T 6)*.

The rulebook explicitly leaves tariffs, extra game types and handling of rule violations to each table (*Spielrunde*) or tournament organiser (R 3.1.2, R 7.3.1). Anything outside these documents is marked **not in the official rules**. When analysing or implementing, state which rule set applies; if the user plays at a private table, ask about their agreements.

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

Maximum per the rulebook: 14 in a Rufspiel, 8 in a Solo or Farbwenz, 4 in a Wenz. Laufende are paid only if the winners claim them before the next cut; over-claimed Laufende can be reclaimed double (R 6.2.4).

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

## Worked example: a Wenz

Dealer is Right, so Me is Vorhand. Hands (Wenz order):

| Seat | Hand |
|---|---|
| Me (Vorhand) | GU · E10 EO E8 · H10 HK · SK SO |
| Left | — · E7 · GK GO G8 · H8 · SA S9 S7 |
| Across | EU SU · EA · GA G10 · HA HO H7 |
| Right (dealer) | HU · EK E9 · G9 G7 · H9 · S10 S8 |

**Bidding.** Me would call the Schellen-Sau (legal: no SA, holds SK) and says "ich möchte spielen". Left "weiter". Across is *gesperrt* (holds EA and GA, no Schellen) but has a Wenz; as second interested player he needs at least a Farbwenz: "ich möchte auch spielen". Right "weiter". Across: "ich hätte (mindestens) einen Wenz"; Me (only a Rufspiel): "weiter"; Across: "ich spiele einen Wenz".

**Play** (leader first):

| # | Cards | Winner | Punkte |
|---|---|---|---|
| 1 | Me SK, Left SA, Across SU, Right S8 | Across — Schellen-frei, trumps | 17 |
| 2 | Across EU, Right HU, Me GU, Left S7 | Across — draws the last Unter | 6 |
| 3 | Across EA, Right E9, Me E8, Left E7 | Across | 11 |
| 4 | Across GA, Right G7, Me SO, Left G8 | Across — Me is Gras-frei, discards | 14 |
| 5 | Across G10, Right G9, Me EO, Left GO | Across — G10 beats the Ober in a Wenz | 16 |
| 6 | Across HA, Right H9, Me HK, Left H8 | Across | 15 |
| 7 | Across HO, Right S10, Me H10, Left GK | Me — H10 beats HO; Right and Left schmieren | 27 |
| 8 | Me E10, Left S9, Across H7, Right EK | Me | 14 |

**Result.** Across 79, defence 41: won, no Schneider (defence > 29). Laufende "mit 1" — fewer than 2, not paid. Tariff: 50 ct from each defender. Tournament: Across +6, each defender −2.

Legality notes: in trick 1 Across may trump because he has no Schellen. In trick 4 Me may play SO because in a Wenz the Ober is a Schellen card, not trump, and Me has no Gras. In a Rufspiel, the same EO in Me's hand would be trump and could **not** be played on an Eichel lead while Me holds E10 or E8.

## Rule violations (R 7)

Typical violations (R 7.2): any utterance or behaviour revealing game-relevant information or prompting a co-player; breaking the bidding rules; invalid announcement; Stoß by the called partner; Stoß/Retour after the second card; playing out of turn (*vorwerfen*; allowed in the last trick); revoking (breaking Bedienpflicht); the partner leading a small card of the Ruffarbe with fewer than four cards before it was searched; playing the Rufsau before it was searched or before Davonlaufen; holding a wrong number of cards; looking further back than the last trick; showing or laying down cards early.

Penalties are left to the table or organiser (R 7.3.1); the deciding question is whether the violation revealed the game. If the innocent side chooses to play on, the actual result counts (R 7.3.2). In tournaments, cheating or repeated revoking leads to disqualification (T 12).

Accidents (R 7.1): a card turned during the deal → reshuffle; wrong number of cards after the deal → redeal; dealing out of turn is void unless someone has looked at a card, in which case it is played; an accidentally exposed card during pickup is ignored.

## Tournament rules (Turnierregeln, Schafkopfschule 2020)

1. Rules of the Schafkopfschule apply. **Allowed: Rufspiel, Solo, Wenz, Farbwenz** (plus Tout and Sie). **No Spritze/Kontra.** No Geier.
2. Two rounds (*Durchgänge*) of **32 games** each, no time limit.
3. Deal **4 × 2**; instead of cutting, the player behind the dealer briefly re-shuffles (*nachmischen*) and hands the cards back face down.
4. If no game comes about, **the same dealer** deals again.
5. Tables and seats are drawn and must not be swapped.
6. **Tout and Sie must be approved by the supervisor (*Aufsicht*) before play.** Minimum for Tout: Solo **4 Laufende**; Wenz **2 Laufende or 3 Unter without the Gras-Unter**; Farbwenz **3 Laufende**.
7. Plus/minus scoring — every row sums to zero:

| Game | Declarer | Each other player |
|---|---|---|
| Rufspiel | winners +1 each | losers −1 each |
| Rufspiel Schneider | winners +2 each | losers −2 each |
| Rufspiel Schwarz | winners +3 each | losers −3 each |
| Solo/Wenz won | +6 | −2 |
| Solo/Wenz lost | −6 | +2 |
| Solo/Wenz Schneider | ±9 | ∓3 |
| Solo/Wenz Schwarz | ±12 | ∓4 |
| Solo/Wenz Tout | ±18 | ∓6 |
| Sie | +24 | −8 |

   (Farbwenz scores as Solo/Wenz.) **Laufende earn no points**, only money.
8. Money tariff alongside: 10 ct for Rufspiel, each Laufender, Schneider, Schwarz; 50 ct for Solo, Wenz, Farbwenz; Tout doubles, Sie quadruples. Laufende paid from 3 in Solo, from 2 in Wenz or Farbwenz (note: the general rulebook says from 3 in Farbwenz).
9. Play in person, every game to the last card; minimum age 16; no spectators (*Kiebitzen*); only the organiser's cards.
10. One player (usually seat 1 or 4) keeps the score sheet; solos and Wenzen are circled; all sign.
11. The supervisor decides disputes, appeal to the tournament management is final. Throwing cards away early loses the game.
12. Cheating, repeated revoking, loud protest, personal attacks or deliberately false scoring → disqualification.
13. Winner: highest plus total over both rounds. Ties: number of Sie, then won Tout, played Tout, won solos/Wenzen, played solos/Wenzen; then lot.

## Not in the official rules

Commonly heard at private tables; treat as house rules and confirm before using:

- **Kurzes Blatt**: 24 cards (no 7 and 8), 6 per player. The official rules cover only the long deck.
- **Ramsch**: played when all pass; everyone for himself, most Punkte loses.
- **Klopfen / Legen**: doubling after seeing the first cards. **Bock / Bockrunde**: rounds at doubled stakes.
- **Stock**: a pot, e.g. paid into when all pass — permitted by agreement (R 4.1.5).
- **Muss** / *"der Alte muss spielen"*: forced game when all pass — permitted by agreement (R 4.1.5).

## Glossary

| Term | Meaning |
|---|---|
| Punkte, Augen | Card points (120 total) |
| Stich | Trick |
| Ausspielen, anspielen, rauskommen | To lead |
| Zugeben, bedienen | To play to a trick; to follow suit |
| Stechen, überstechen | To win with a trump / beat the current winner |
| Schmieren | Give Sau or Zehn to a trick one's own side wins |
| Abwerfen | Discard while void |
| Frei | Void in a suit ("Gras-frei") |
| Blank | Single card in a suit ("blanke Zehn") |
| Durchlaufen, läuft | A plain card wins because nobody trumps ("die Sau läuft") |
| Trumpf ziehen | Lead trumps to draw them |
| Spielmacher | Declarer |
| Spielerpartei / Gegenspielerpartei | Declaring side / defence |
| Rufsau, Ruffarbe, der Gerufene | Called ace, its suit, the partner |
| Gesucht | The Ruffarbe has been led |
| Davonlaufen | Partner leads small from 4+ cards of the Ruffarbe |
| Gesperrt | Cannot call any Sau |
| Einzelspiel | Solo, Wenz, Farbwenz, Geier, Farbgeier |
| Laufende, mit/ohne n | Run of top trumps |
| Schneider, schneiderfrei, Schwarz | See *Result* |
| Tout, Sie | All tricks; all 8 Ober and Unter |
| Stoß (Kontra, Spritze), Retour | Doubling by defence / by declaring side |
| Weiter | Pass |
| Zusammenwerfen | Throw in the hand |
| Vorwerfen | Playing out of turn |
| Kiebitz | Spectator |
| Spatzen, Luschen | 0-point cards |

## Strategy basics

Not part of the rules; common practice.

**Choosing a game**

- **Rufspiel**: roughly 4+ trumps including at least one Ober, ideally a plain Sau or a void. Call a suit where you hold only one card, so the Rufsau is likely to win when searched and you become free in it.
- **Solo**: typically 6+ trumps with at least two top Ober, or 7 trumps with a plain Sau. Laufende reduce risk.
- **Wenz**: two or more Unter (EU and GU ideal) and long suits headed by Sau–Zehn. Being Vorhand matters a lot.
- **Farbwenz**: Unter plus length in the trump suit.
- **Tout**: only when every trick is certain (in tournaments, the minimums of T 6 apply anyway).
- **Stoß**: when the defence likely holds more trump strength than the declaring side; a wrong Stoß doubles the loss.

**Declaring side**

- Draw trumps early so plain Saus and Zehner run later.
- Count trumps (14 in Rufspiel and Solo) and Punkte silently.

**Defence**

- In a Rufspiel, search the Rufsau early: lead the Ruffarbe. It reveals the partner, and the caller often holds only one card of it.
- Schmieren onto tricks your side will surely win; don't feed Punkte the declarer can trump.
- Against a Wenz: lead suits where you hold the Sau, keep Zehner guarded, and avoid helping the declarer establish his long suit.

**Partner in a Rufspiel**

- Davonlaufen with the Sau plus three or more small cards — otherwise the Sau is likely trumped by a void defender when searched.
- Before the Sau falls, nobody knows you; infer the partner from who searches or avoids the Ruffarbe.

## Checklist for agents

- Default to the Schafkopfschule rules; in tournament context apply the Turnierregeln (no Kontra, no Geier, 4 × 2 deal, same dealer redeals, Tout approval, plus/minus points).
- Treat Ober/Unter per game type: trump in Rufspiel and Solo, only Unter in Wenz/Farbwenz, only Ober in Geier/Farbgeier.
- Check Rufspiel calls (not own Sau, at least one plain card of the suit, Herz never).
- Enforce Rufsau duties and the four-card Davonlaufen rule.
- Thresholds: 61 to win (60 for the defence); Schneider at ≤ 30 for the declarers, ≤ 29 for the defence; Schwarz = zero tricks.

## Sources

- Schafkopfschule e.V., *Schafkopfregeln*, Stand April 2024 — https://schafkopfschule.de/regeln.html
- Schafkopfschule e.V., *Turnierregeln*, January 2020 — same page.
