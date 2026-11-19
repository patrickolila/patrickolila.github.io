# Foul Watch

`foul-watch.html` is one web page that watches live NBA and college basketball games. It tells you when **both teams are in the bonus** in the same quarter (NBA) or half (NCAAB). That's the moment to look at live quarter totals, half totals and player quarter points.

It runs entirely in your browser and reads ESPN's public scores and play-by-play directly. There's no account, server or install.

## Open it

**On your computer.** Double-click `foul-watch.html`. It opens in your browser and starts loading games. Keep the tab open, and bookmark it.

**On your phone.** A phone browser needs a web address, so put the file on your GitHub Pages site:
1. On github.com, open your `polila.github.io` repository. Choose **Add file → Upload files**, drop in `foul-watch.html`, then **Commit changes**.
2. A minute or two later, open **https://polila.github.io/foul-watch.html** in Safari.
3. Tap **Share → Add to Home Screen** so it opens like an app.

The page contains nothing about you. Your settings and starred games are saved only in the browser you use.

## Finding a game

Teams are shown by their full names: NBA teams as "New York Knicks", and college teams by school, the way sportsbooks list them ("Florida International", not "FIU").

To jump to a game, type in the **Find a team** box at the top. Part of the school name, the nickname or the short code all work, so "florida", "panthers" and "fiu" find the same game. If the game hasn't started, the page tells you when it does.

## Alerts

An alert fires once per game per quarter or half when both teams reach the bonus. By default it needs at least 3:00 left (NBA) or 4:00 (NCAAB).

| League | Both teams have | From then on |
|---|---|---|
| NBA | 4 team fouls in the quarter (3 in OT) | Every common foul by either team is 2 FTs |
| NCAAB | 6 team fouls in the half | Every non-offensive foul is a 1-and-1 |
| NCAAB | 9 team fouls in the half | Every non-offensive foul is 2 shots |

**The page has to stay open for alerts to fire.** In **Settings**:
- **Sound:** turn it on. On an iPhone, if you hear nothing, take the phone off silent.
- **Keep screen on (phone):** a locked screen pauses the page.
- **Browser notifications (computer only):** phones can't show notifications from a web page.
- **NBA / NCAAB alerts:** choose All games, Starred or Off. On busy college nights, set NCAAB to Starred and tap ☆ on the games you follow.

Browsers slow down tabs that are in the background, so keep this one in front for the quickest updates.

## Reading a card

- **Badges:**

  | Badge | Meaning |
  |---|---|
  | AT LIMIT | NBA team at 4 team fouls |
  | PENALTY | NBA team at 5+ team fouls |
  | FOUL TO GIVE | NBA, last 2:00 of a period |
  | BONUS NEXT | NCAAB team at 6 team fouls |
  | BONUS | NCAAB team at 7–8 team fouls |
  | DOUBLE NEXT | NCAAB team at 9 team fouls |
  | DOUBLE BONUS | NCAAB team at 10+ team fouls |

  The outlined pip marks where free throws start.
- **Quarter or half total:**
  - **so far:** points scored in the current quarter or half
  - **at this pace:** plus the time left at this game's scoring rate
  - **with the bonus:** plus what the bonus adds (below)
- **On the floor (NBA):** each team's two players on the court with the most free-throw attempts so far, with their FTA, points this quarter and fouls.

## What the bonus is worth

The projection was fitted on 2,631 NBA and 4,453 college games, from the 2024-25 season to Nov 12, 2026. It was then checked on games it wasn't fitted on.

"At this pace" is what the rest of the quarter or half usually scores in a game like this one with neither team in the bonus. It takes in the time left, the game's scoring rate and pregame total, the score margin, how often fouls are being called, free-throw shooting, and players in foul trouble. "With the bonus" adds what the bonus is worth:
- **NBA:** worth more the longer it lasts before the last-2:00 foul to give. That's about **+1.1** with 3:00 left, **+1.9** at 4:00 and **+2.6** at 5:00.
- **College 2nd half:** about **+1.3** with 4:00 left, rising to **+2.4** with 8:00 left. It's a little more at the double bonus.
- **College 1st half:** about **+1.1**.

On those held-out games, the projection was within a few tenths of a point of the result on average. That held in every quarter, half, time left, score margin and foul state checked. A single quarter still swings about ±5 points, and a college half about ±7.

For a 4th-quarter or 2nd-half line where overtime counts, the log form adds the expected overtime points. In a close game that's worth 2–4 points.

Each team's top foul-drawer on the floor scored about 0.13 more points a minute, or about +0.5 over 4 minutes.

## Testing the edge

Winning a few days in a row doesn't show much. Seven wins in ten bets happens 17% of the time on coin flips. The **Edge test** section at the bottom of the page keeps a proper score.

1. **Log every kiosk line you check, bet or not.** On the game's card, tap **Log kiosk line**. Enter the line and odds, pick Over or Under, and tap **I bet it** with your stake if you bet. Logging the ones you pass on too stops the test from only counting the good-looking spots.
2. **It grades itself.** When the quarter or half ends, the page gets the result from ESPN. You don't need to do anything, and it works even if you closed the page and come back later.
3. **Read the verdict.** It compares how far your side beat the line, on average, with what the vig needs at your odds, and gives a 95% range. It says the edge looks real only once that whole range is above what the vig needs. A 2-point edge takes about 50 graded lines to show. The table splits the results by league, by half, and by how far the kiosk line was from the page.
4. **Overtime.** For a 4th-quarter or 2nd-half line, set **Overtime counts on this line** to match the kiosk's rules.

Separately, the page records its own numbers at every both-in-the-bonus alert and grades them after the quarter or half. That's the **Page check**. If its average drifts away from 0 over a few weeks, the page's numbers need retuning for this season.

The records stay in the browser you log them in, so log from one device (your phone at the kiosk). **Download CSV** saves a copy. Clearing the browser's data deletes them.

## Try it any time

Go to **Settings → Try it on a finished game**. Enter an ESPN game id and press **Replay**. The id is the number at the end of an ESPN game link; 401909294 is POR @ LAL from Nov 7.

The game plays back at 10x, as if it were live. Its alerts are real but marked "Replay", and kiosk lines logged during a replay aren't kept.

## Limits

- ESPN can trail the TV broadcast, so check the scorebug before you bet.
- Some small-conference college games have no ESPN play-by-play. Their fouls can't be counted, and they're listed separately.
- ESPN's public data comes with no guarantees. If ESPN changes it, the page shows "Can't reach ESPN".
- **Accuracy check:** the counting was checked against the free throws that followed in 49 past games. In the NBA, it predicted correctly whether free throws followed on 434 of 438 non-shooting fouls.
