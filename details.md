# Data Driven Gambling with various tools 

    To build a probability model for the outcomes (win, loss, or draw) of the next three matches in the Brazilian Serie A, we'll consider several important parameters:

### Parameters

1. **Goals Scored**: Average goals scored per match by each team.
2. **Goals Conceded**: Average goals conceded per match by each team.
3. **Form**: Recent performance, usually the last 5 matches (points obtained).
4. **Home/Away**: Historical performance when playing at home or away.

## Step By Step Process
1. ### Data Collection:
    - Average goals scored and conceded for each team.
    - Recent form (last 5 matches results).
    - Home and away performance statistics.

2. ### Calculate Team Strength:
    - Offensive Strength (OS): Average goals scored per match.
    - Defensive Strength (DS): Average goals conceded per match.

3. ### Adjust for Home/Away:
   -  Home Advantage (HA): Factor to increase/decrease performance based on playing at home.
    - Away Disadvantage (AD): Factor to increase/decrease performance based on playing away.
4. ### Expected Goals Calculation:
    - Expected goals for home team (EG_home) = OS_home * DS_away * HA
    - Expected goals for away team (EG_away) = OS_away * DS_home * AD
5. ### Probability Calculation:
    - Use the Poisson distribution to calculate the probability of different scorelines.
    - Sum probabilities of scorelines to get win, loss, and draw probabilities.

## Example Data and Calculation
    Let's consider an example with two hypothetical teams, Team A and Team B.
### Data for Team A(Home)
1. Average goals scored: 1.8
2. Average goals conceded: 1.2
3. Last 5 matches points: 10 (3W, 1D, 1L)
4. Home performance: Generally stronger (HA factor = 1.1)

### Data for Team B (Away):
1. Average goals scored: 1.4
2. Average goals conceded: 1.6
3. Last 5 matches points: 7 (2W, 1D, 2L)
4. Away performance: Generally weaker (AD factor = 0.9)

### Expected Goals:
1. EG_home = 1.8 (OS_home) * 1.6 (DS_away) * 1.1 (HA) = 3.168
2. EG_away = 1.4 (OS_away) * 1.2 (DS_home) * 0.9 (AD) = 1.512

### Poisson Distribution:
- Calculate probabilities for various scorelines using Poisson distribution.

## Probability Calculation:
1. Sum probabilities of scorelines where home team wins.
2. Sum probabilities of scorelines where away team wins.
3. Sum probabilities of scorelines that are draws.

This process can be repeated for the next three matches to predict their outcomes. Do you have specific teams and matches in mind for which you'd like detailed calculations? If so, providing those details will help tailor the model precisely to those fixtures.

