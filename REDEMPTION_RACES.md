---
title: Redemption Races
---

Why redemption races require *two* knockouts.

## What is a redemption race?

When the second set of races in a rounds has groups of odd teams a redemption race
may occur between the loser of a higher group and the winner of a lower group.

For example when 21 teams compete a redemption race for 7th/8th may be run between
the loser of the higher group (1st-7th) and the winner of the lower group (8th-14th).

## Current Behaviour

The current approach assumes that the winner of the lower group is the team who won
all their races in the larger mini league.

For example in 21 races the winner of the 4 team mini league for 8th-14th is automaticlly
considered 8th and eligible for the redemption race.

## Problems

The winner of the larger mini league is only the best of that mini league, not the
whole group.

For example with 21 teams running the second set of races does not give enough
information to determine whether the winnner of the 4 team mini league or the 3
team mini league is the best of that 7.

This is because no races have occurred between the 3 and 4 team mini leagues.

As an extension of this it is possible for *all* teams in the 3 team mini league
to be better than the winner of the 4 team mini league.

## Additional context

### 8 Teams

Consider how you would determine the best of 8 teams with the below format

- 1 round of mini league races
- knockouts

In this case we would split the round into 2 4 team mini leagues. As an example
assume the below results after running the races.

```
| Group A    | Rank |
|------------|------|
| Plymouth 1 | 1st  |
| Aber 1     | 2nd  |
| Bristol 1  | 3rd  |
| Bath 1     | 4th  |

| Group B    | Rank |
|------------|------|
| Cardiff 1  | 1st  |
| UWE 1      | 2nd  |
| Swansea 1  | 3rd  |
| Swansea 2  | 4th  |
```

It should be obvious that we now run the below races to determine the final positions:

- 1st/2nd - Plymouth 1 vs Cardiff 1
- 3rd/4th - Aber 1 vs UWE 1
- 5th/6th - Bristol 1 vs Swansea 1
- 7th/8th - Bath 1 vs Swansea 2

This has issues as above (all teams from 1 league could be better than all teams from
the other) but this is a known downside of this divide and conquer approach and not
relevant to this discussion i.e. determining whoo was best of all 8 teams.

<a name="7teams"></a>
### 7 Teams

Now consider the exact same set of races but where Swansea 2 have not turned up i.e.

```
| Group A    | Rank |
|------------|------|
| Plymouth 1 | 1st  |
| Aber 1     | 2nd  |
| Bristol 1  | 3rd  |
| Bath 1     | 4th  |

| Group B    | Rank |
|------------|------|
| Cardiff 1  | 1st  |
| UWE 1      | 2nd  |
| Swansea 1  | 3rd  |
```

Again it should be obvious that we now run the below races to determine the final positions:

- 1st/2nd - Plymouth 1 vs Cardiff 1
- 3rd/4th - Aber 1 vs UWE 1
- 5th/6th - Bristol 1 vs Swansea 1
- 7th Bath 1 (no race)

We *do not* run the below races since we have not determined Plymouth 1 is better than *any*
of the teams from group B.

- 1st Plymouth 1 (no race)
- 2nd/3rd Cardiff 1 vs Aber 1
- 4th/5th UWE 1 vs Bristol 1
- 6th/7th Swansea 1 vs Bath 1

### 21 Teams

For a 21 team race the first set determines the broad group each team is in i.e.

- 1st - 7th
- 8th - 14th
- 15th - 21st

Once we have these sets we split these into 4 and 3 team mini leagues per
[7 teams](#7teams) above for the second set of races.

It should be clear that the best team of the 8th-14th is not simply the team who
won the 4 group mini league since they have not raced anyone from the 3 team mini
league. i.e. we must run the second set of races and then run a knockout between
the winner of the 4 group mini league and the 3 group mini league to determine
the best of that group.

This is true for *all* of the second set groups i.e. we expect

- 1st - 7th
  - 1st/2nd - winner of the 3 and 4 team mini leagues
  - 3rd/4th
  - 5th/6th
  - 7th
- 8th - 14th
  - 8th/9th - winner of the 3 and 4 team mini leagues
  - 10th/11th
  - 12th/13th
  - 14th
- 15th - 21st
  - 15th/16th - winner of the 3 and 4 team mini leagues
  - 17th/18th
  - 19th/20th
  - 21st

## Result

Ignoring the redemption race itself knockouts have to follow the structure above
to ensure accurate results i.e. knockouts start with best of group vs best of group
and work down. This correctly determines the winner through an approrpriate challenge.

In this and the majority (possibly all) cases we must *not* start with the worst
of group vs worst of group and work up possibly declaring an incorrect and
unchallenged winner.

This is true for all second set groups in which no two teams have yet raced each
other.

### Redemption Race Still Possible

Given the above the redemption is now dependent on a prior knockout. From a
logistics point of view while possible it is annoying as it would either

- require waiting for the winner of 8th/9th to come back up
- running 7th/8th out of order

It also begs the question of why we don't run redemptions on other boundaries for
example on 14th/15th in the 21 team example.

