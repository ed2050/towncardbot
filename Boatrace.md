# Frozen Fortune (Township) - What the Data Says, and How to Play It Smart

## Top Takeaways

From a few hundred logged spins across two accounts, here are the practical takeaways :

- Expected value (EV) per token is roughly 70 points per token, regardless of multiplier (1x, 5x, 10x, 50x).
- Multipliers do not change EV per token. They only change how much your results swing.

- for a good chance to finish all 3 boats, each player needs about 120 tokens a day.  That's 8 mid-level tasks (15 tokens each) or 6 top tier tasks (20 tokens each).  Very doable.

Higher multipliers mean you need more tokens to guarantee success.  To have an 80% chance to finish:
- **1x**: about **1,210 tokens**
- **5x**: about **1,260 tokens**
- **10x**: about **1,290 tokens**
- **50x**: about **1,450 tokens**

At 1x you need only slightly more than the mean to get to 80 percent success.
At 50x you need a lot more tokens, because the results are much more volatile.

### Best Strategy

- Early in the race (before midway point of a boat) :
  - EV looks to be around 75 points per token.
  - Use 1x spins:
    - More spins = more chances to hit Super or Free.
    - Results are smoother and closer to the average - no "big misses".
    - Best chance to reach the end if 70 to 75 points per token gets you there (depends how many tokens you generate).

- Later in the race (after midway point of a boat):
  - EV seems to drop to roughly 65 points per token.
  - If you are on pace (tokens you will earn * 65 >= points remaining):
    - Stick with 1x for consistency.
  - If you are behind pace (tokens you will earn * 65 < points needed):
    - Switch to 10x or 50x as a "Hail Mary":
      - Bigger swings, might spike some big results.
      - You could catch up, or just crash and burn.
      - This strategy makes sense when spinning 1x guarantees failure anyway.

Rule of thumb:
- If you are on track, spin 1x.
- If you are behind on tokens and out of time, use 5x or 10x and pray.

There also appears to be a real split between first half and second half:
- First half : EV is about 75 points per token.
- Second half : EV is about 65 points per token.

This split seems to come mostly from "Super 200" showing up more often in the first half of race (before midway point). Data is not conclusive yet, but so far it suggests the first half / second half spread is real.

---

## Frozen Fortune - Setup And Mechanics

Frozen Fortune is a 10 day cooperative Township boat event where:

- You have 3 boats, each shared with one other player.
- The goal is to move each boat to the finish lline.
- You earn tokens from tasks and bonus rewards
- You spend tokens to spin a wheel
- Each spin moves your a boat that many spaces toward the goal
- Reach milestones for rewards, and finish all 3 boats for the grand prize.

### The Wheel

The wheel visually has 10 segments, in this order (as they appear in game):

> 5 - 20 - 10 - 100 - 5 - Free - 10 - 30 - 5 - Super

Outcomes:

- 5, 10, 20, 30, 100: move the boat by that many points.
- Free: gives 3 more spins on the same wheel, with the same multiplier, no extra tokens.
- Super: gives one spin on a special Super wheel, which pays 100 or 200 points.

The wheel appears to have 3 segments within each space where a spin can land.  However these spaces are misleading; the chances of landing on a space are not the same as the number of spots shown on the wheel.  The wheel is just a visual indicator of results.

### Multipliers

Before spinning, you choose a multiplier:

- 1x: costs 1 token, standard values (5, 10, 20, 30, 100, Free, Super).
- 5x: costs 5 tokens, all wheel values are multiplied by 5 (25, 50, 100, 150, 500, etc).
- 10x and 50x: same idea, values are 10 or 50 times higher.

Free spins inherit whatever multiplier was active when Free was triggered.
Super results (100 or 200) are also multiplied.

Key fact:
- A 10x spin is just "10 times the points" for "10 times the tokens".
- That is why expected points per token is the same for all multipliers.
- However spinning with higher multipliers and limited tokens means less bites at the apple, so fewer opportunities to hit bonuses.

---

## How We Collected Data

Two accounts, lots of logging.

### 1. Spin By Spin Outcome Data

For every spin (including free spins), I recorded:

- Which base space I landed on:
  - 5, 10, 20, 30, 100, Super, Free
- For Super, I also recorded what value the Super wheel spin gave:
  - Super-100 or Super-200

We did this separately for two accounts:

- Account 1: mostly spent tokens in the second half of boat races.
- Account 2: only spent tokens in the first half of boat races.

#### Account 1 - Spin Counts (Mostly Second Half)

Total spins (including free spins): 258

Spin outcomes:

| Result      | Count |
|------------|------:|
| 5          | 53    |
| 10         | 36    |
| 20         | 33    |
| 30         | 35    |
| 100 (base) | 49    |
| Super->100 | 13    |
| Super->200 | 21    |
| Free       | 18    |

- Free events: 18, each gives 3 free spins, so 54 free spins.
- Paid spins (tokens used) = 258 - 54 = 204 tokens.

#### Account 2 - Spin Counts (Only First Half)

Total spins (including free spins): 128

Spin outcomes:

| Result      | Count |
|------------|------:|
| 5          | 25    |
| 10         | 16    |
| 20         | 17    |
| 30         | 16    |
| 100 (base) | 20    |
| Super->100 | 6     |
| Super->200 | 18    |
| Free       | 10    |

- Free events: 10, so 30 free spins.
- Paid spins (tokens used) = 128 - 30 = 98 tokens.

### 2. Tokens Versus Points Data

Separately, I logged blocks of:

- Starting tokens and starting points.
- Ending tokens and ending points.

That allows a very simple EV estimate:

> EV per token = (points gained) / (tokens spent)

Example from one run on Account 2:

- Tokens: 98 -> 0
- Points: 7500 -> 14860

So:

- Points gained = 14860 - 7500 = 7360
- EV per token = 7360 / 98 = 75.1 points per token

We did this for several blocks on Account 1 and Account 2, and then compared those results with what the spin counts suggest.

---

## Observed Probabilities

From the spin count tables we can calculate how often each base outcome appears.

We treat every spin (including free ones) as one sample of the main wheel.

### Second Half (Account 1)

Using 258 spins:

| Base Outcome | Count | Approx Probability |
|--------------|------:|-------------------:|
| 5            | 53    | 20.5 percent       |
| 10           | 36    | 14.0 percent       |
| 20           | 33    | 12.8 percent       |
| 30           | 35    | 13.6 percent       |
| 100 (base)   | 49    | 19.0 percent       |
| Super        | 34    | 13.2 percent       |
| Free         | 18    | 7.0 percent        |

So in the second half we see:

- 5 and base 100 are "top tier" outcomes, both around 20 percent.
- 10, 20, 30, and Super are a "middle tier", all around 13 to 14 percent.
- Free is clearly the rarest space at about 7 percent.

From the tokens versus points totals on this account:

- Total tokens across four logged blocks: 389
- Total points gained: 25935
- Empirical EV = 25935 / 389 = about 66.7 points per token

In this account, using only spins in the second half of a race (after midway point), EV calculation gives about 62 points per token.  This is close to the observed 66 to 67 when you factor in that roughly 50 spins were in the first half of a race (I didn't keep exact data on this point, because I didn't notice the possible split yet).

---

### First Half (Account 2)

Using 128 spins:

| Base Outcome | Count | Approx Probability |
|--------------|------:|-------------------:|
| 5            | 25    | 19.5 percent       |
| 10           | 16    | 12.5 percent       |
| 20           | 17    | 13.3 percent       |
| 30           | 16    | 12.5 percent       |
| 100 (base)   | 20    | 15.6 percent       |
| Super        | 24    | 18.8 percent       |
| Free         | 10    | 7.8 percent        |

Here again:

- 5 and base 100 are strong.
- 10, 20, 30 are a mid tier, about 12 to 13 percent each.
- Free is rare, around 8 percent.

But Super is special:

- In the first half, Super hits almost as often as 5, with probability near 19 percent.
- That is clearly higher than 10, 20, or 30, and higher than Super in the second half.

From the tokens versus points totals for this account:

- Tokens spent: 98
- Points gained: 7360
- Empirical EV = 7360 / 98 = 75.1 points per token

Using the above spin probabilities and Super wheel bias, an EV calculation gives about 74.5 points per token for the first half, which closely matches the empirical 75.1 (as it should since it's derived from this data).

---

### The Super Wheel Bias (100 Versus 200)

From both accounts combined:

- Super->100: 19 spins
- Super->200: 39 spins

So:

- P(200 in Super) = 39 / 58 = about 67 percent
- P(100 in Super) = 19 / 58 = about 33 percent

This is nowhere near 50/50. Super strongly favors 200.

Split by phase:

- First half (Account 2):
  - 6 times 100, 18 times 200
  - So P(200 given Super) = 75 percent

- Second half (Account 1):
  - 13 times 100, 21 times 200
  - So P(200 given Super) is still about 62 percent

So Super is always good, but it seems to be more generous in the first half of the race.  First half /second half samples are small, so result is uncertain.  But 200 is definitely more
frequent than 100 in either scenario.

---

## A Simple Tier Based Model

We cannot see the real code, but the data suggests that the odds look roughly like this.
We assume that the game programmers use a simple model that's easy to program using nice round numbers.

### First Half (Boosted Phase)

Approximate tiers and chances:

- Tier 1 (high):
  - Slots: 5, 100, Super
  - Rough chance: about 20 percent each

- Tier 2 (mid):
  - Slots: 10, 20, 30
  - Rough chance: about 13 percent each

- Tier 3 (low):
  - Slot: Free
  - Rough chance: about 8 percent

Super wheel in this phase:

- P(200 in Super) around 75 percent
- P(100 in Super) around 25 percent

### Second Half (Toned Down Phase)

Approximate tiers:

- Tier 1 (high):
  - Slots: 5, Super
  - Rough chance: about 20 percent each

- Tier 2 (mid):
  - Slots: 100
  - Rough chance: about 15 percent each

- Tier 2 (mid):
  - Slots: 10, 20, 30
  - Rough chance: about 13 to 14 percent each

- Tier 3 (low):
  - Slot: Free
  - Rough chance: about 7 percent

In other words it seems like Super goes up roughly 5% and regular 100 goes down roughly 5%.

Super wheel here:

- P(200 in Super) is still higher than 100, but more like 60 to 65 percent.

These rounded values line up quite well with the observed spin frequencies and with the drop from around 75 EV in the first half to about 62 to 66 EV in the second half.

---

## Computing EV (Light Math Version)

We'll keep this conceptual and skip long derivations.

Let mu be the expected number of points from one paid spin at 1x.

### Step 1: EV Ignoring Free

First, pretend Free does not exist and compute:

- E0 = sum over all non Free outcomes of:
  - probability(outcome) * points(outcome)

For example, in the first half:

- E0 includes:
  - 5, 10, 20, 30, 100 at their observed probabilities
  - Super at its observed probability, multiplied by the average Super result
- For Super we use:
  - E[Super] = P(100 given Super)*100 + P(200 given Super)*200

This gives E0 values somewhere around:
- E0_first_half = about 57
- E0_second_half = about 49

(Exact numbers depend on the precise probabilities you plug in)

### Step 2: Add Free Spins

Let pF be the probability of landing on Free.

- Each time you hit Free, you get 3 more spins.
- Each of those spins is worth mu points on average.

So Free contributes, on average, 3 * pF * mu extra points to each paid spin.

This gives the equation:

- mu = E0 + 3 * pF * mu

Rearrange:

- mu * (1 - 3 * pF) = E0
- So mu = E0 / (1 - 3 * pF)

Plugging in the approximate model values:

- First half:
  - E0 roughly 57, pF about 0.078
  - mu = 57 / (1 - 3 * 0.078) which is about 74.5

- Second half:
  - E0 roughly 49, pF about 0.07
  - mu = 49 / (1 - 3 * 0.07) which is about 62

These values close approximate the averages we saw from real token and point data:
- Around 75 points per token early
- Around 65 points per token later

---

## Multipliers: Same EV, Bigger Swings

Let X be the points from a single 1x spin, including all chained Free and Super effects.

- 1x spin:
  - Points = X
  - Cost = 1 token

- 10x spin:
  - Points = 10 * X
  - Cost = 10 tokens

Free spins and Super results are always scaled by the same multiplier as the spin that triggered them.

So:

- E[points from 1x spin] = E[X] = mu
- E[points from 10x spin] = E[10 * X] = 10 * mu

EV per token:

- For 1x: EV = mu / 1 = mu
- For 10x: EV = (10 * mu) / 10 = mu

Conclusion: multipliers do not change EV per token.

What they do change is variance, that is, how spread out your results are.

### Example: Spending 100 Tokens

Assume we are in the first half and EV is about 75 points per token.
So expected total from 100 tokens is:

- 100 * 75 = 7500 points

Now look at how those 100 tokens are used:

- At 1x:
  - You get 100 independent spins.
  - Lots of small random ups and downs average out.
  - Most results will fall in a band from 6000 to 9000 points.
  - It's very uncommon to end way below 5000 or way above 10000.

- At 10x:
  - You only get 10 paid spins (each one is worth 10x more).
  - If you miss several Supers and hit mostly small numbers:
    - Your total could be far below 7500.
  - If you hit multiple Super->200 chains:
    - Your total could be far above 10000.
  - The spread of possible outcomes is much wider.

- At 50x:
  - Only 2 paid spins.
  - Outcomes range from:
    - Both spins weak: maybe 1500 to 3000 total.
    - One strong, one weak: maybe 8000 to 12000.
    - Both extremely strong: 15000 or more.
  - You almost never get close to the "average" of 7500. You are usually way under or way over.

### What This Means For Actual Play

- If EV times your tokens is enough to reach the prize, you want stability, not drama:
  - Use 1x most of the event.
  - Many small spins give you the most reliable progress and the highest chance to finish.

- If you are behind schedule and even EV with 1x is not enough any more:
  - Playing it safe guarantees you will not finish.
  - In this case it makes sense to switch to 5x or 10x:
    - You accept a high chance of failing hard.
    - But you gain a small chance to roll high and catch up.

- 50x is almost pure casino behavior:
  - Enormous swings, usually bad, sometimes amazing.
  - Useful for memes and screenshots, but rarely the best strategy unless you're way behind.

---

## Tokens Needed To Finish

Now that we have an approximate EV of about 70 points per token, we can ask a very practical question:

How many tokens do you need per day to stay on pace, and how does that change with multipliers?

### Total Points You Need

From the event setup:

1. Each boat needs 55,000 points to finish the race.
2. Each boat is shared with one other player.
   - So a fair share for each player is half of that:  
     55,000 / 2 = 27,500 points per boat.
3. Each player has 3 boats.
   - So total points needed per player over the whole event is:  
     3 * 27,500 = 82,500 points.
4. The event lasts 10 days.

So the goal we will use is:

- Total target per player, all 3 boats:  
  **D = 82,500 points**

### Tokens Per Day At 1x With EV = 70

If EV per token is about 70 points, then the average number of tokens needed is simply:

- T_mean = D / EV = 82,500 / 70 = about 1,180 tokens total

Spread over 10 days:

- Tokens per day = 1,180 / 10 = about **118 tokens per day**

Now translate that into tasks.

Typical task rewards:

- Mid tier tasks (115 to 125 points): about **15 tokens** each
- High end tasks (140 to 150 points): about **20 tokens** each

So, to get about 118 tokens per day:

- Using only mid tier tasks (15 tokens each):  
  118 / 15 = 7.9, so about **8 mid tasks per day**
- Using only high tier tasks (20 tokens each):  
  118 / 20 = 5.9, so about **6 high tasks per day**

In practice you will be doing a mix, so a good ballpark is:

- Aim for **6 to 8 tasks per day** if you want to play mostly at 1x and stay on pace.

### Building In Some Cushion For Luck

The 1,180 tokens number is a "mean only" value. In reality, spins are random. Some runs will be hot, others cold.

We can use a normal approximation with our mixed first half / second half model:

- EV per token mu is about 70 points.
- Standard deviation per token sigma is about 85 points.
- Target D is 82,500 points.

Using that, we can estimate the total tokens needed so that:

- You finish with about 80 percent chance.
- You finish with about 90 percent chance.

For 1x spins:

- 80 percent success: about **1,210 tokens**
- 90 percent success: about **1,230 tokens**

Per day over 10 days:

- 80 percent success: about 121 tokens per day
- 90 percent success: about 123 tokens per day

Translated to tasks:

- 80 percent success:
  - Mid tasks: 121 / 15 = 8.1 -> about **8 mid tasks per day**
  - High tasks: 121 / 20 = 6.1 -> about **6 high tasks per day**
- 90 percent success:
  - Mid tasks: 123 / 15 = 8.2 -> about **8 or 9 mid tasks per day**
  - High tasks: 123 / 20 = 6.2 -> about **6 to 7 high tasks per day**

So from a "human" point of view:

- **If you can comfortably do 6 to 8 tasks per day**, mostly mid or high tier, you are in the right ballpark to finish all three boats using mostly 1x spins, with a decent safety margin.

### How Multipliers Change The Tokens Needed

Remember:

- Multipliers do not change EV per token.
- They only change how wide the distribution is (the variance).

Using the mixed EV model (mu = 70, sigma about 85), and a normal approximation, we can estimate how many tokens you would need for a given chance to finish if you use a single multiplier for all tokens.

For each multiplier m (1x, 5x, 10x, 50x), we solve:

- P(total points from T tokens >= 82,500) = desired probability

Results below are rounded to the nearest 10 tokens.

#### Tokens Needed For About 80 Percent Chance To Finish

- **1x**: about **1,210 tokens**
- **5x**: about **1,260 tokens**
- **10x**: about **1,290 tokens**
- **50x**: about **1,450 tokens**

All of these have the same mean (82,500 points if you hit EV), but:

- At 1x you need only slightly more than the mean to get to 80 percent success.
- At 50x you need a lot more tokens, because the results are much more volatile.

#### Tokens Needed For About 20 Percent Chance To Finish

Now look at the other side: how few tokens could you get away with if you are willing to accept only a 20 percent chance of finishing?

- **1x**: about **1,140 tokens**
- **5x**: about **1,100 tokens**
- **10x**: about **1,070 tokens**
- **50x**: about **960 tokens**

Notice the pattern:

- At **1x**, the 20 percent and 80 percent token levels are quite close:
  - 20 percent success: about 1,140 tokens
  - 80 percent success: about 1,210 tokens
  - The spread is only about 6 percent.

- At **50x**, the spread is huge:
  - 20 percent success: about 960 tokens
  - 80 percent success: about 1,450 tokens
  - The spread is more than 50 percent.

This illustrates the variance effect very clearly:

- High multipliers like 50x can "get lucky" with fewer tokens (the 20 percent line is lower).
- But to be reasonably sure of finishing (80 percent or 90 percent), you need many more tokens than at 1x.

### Practical Takeaways For Tokens And Multipliers

Putting it all together:

- **Steady plan (1x)**:
  - Aim for about **1,200 to 1,250 tokens total** for a comfortable chance to finish all three boats.
  - That is around **120 tokens per day**, or roughly **6 to 8 tasks per day**.

- **Using 5x or 10x a lot**:
  - You still need roughly the same number of tasks (EV per token has not changed), but:
  - To reach the same 80 percent or 90 percent success chance, you need more total tokens because variance is higher.

- **Using 50x heavily**:
  - If you do not have many tokens, 50x gives you a small chance to spike an amazing run, but:
  - To have a high chance of finishing (80 percent or 90 percent), the token requirement grows fast.
  - This is why 50x is best treated as a last ditch gamble, not a main strategy.

In short:

- If you can generate **around 120 tokens per day** and mostly spin **1x**, you are in good shape.
- Use high multipliers only when:
  - You are behind pace,
  - You know that EV at 1x is no longer enough to finish,
  - And you are intentionally taking on more risk to chase a high roll.
---

## Final Takeaways

From a few hundred logged spins across two accounts, the main points are:

- EV per token is nowhere near the naive 40 to 50 range you would expect from a uniform wheel with the number of spaces shown in game. EV is closer to 70 overall.
- Early in the race:
  - Super appears more often.
  - Super gives 200 points much more often than 100.
  - EV is around 75 points per token.

- Later in the race:
  - Super is less frequent.
  - It still favors 200, but not as strongly.
  - EV is around 65 points per token.

- Multipliers do not change EV per token. They only change how wild the swings are.

Practical advice:

- Spin 1x early and while you are on pace.
- If you fall behind and do not have enough tokens to finish at 70 points per token, switch to 5x or 10x as a last resort.
- Treat 50x as a fun gamble, not a serious strategy.


