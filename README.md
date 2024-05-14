# FantasyFootballAnalysis

## Motivation
For decades fantasy football has dominated the landscape of sports betting by striking a perfect balance
between strategy, competition, and luck. It is a online game where participants can create their own football 
teams by selecting real life NFL players. Each participant, known as a manager, can draft these players from 
across the league, who will then earn points based on their real world game statistics every week. 

Although managers can continue to make changes to their team after the season starts, one of the most pivotal
moments of the game is the draft, where players generally select 16 players onto their initial roster in a 
snake draft. Over the years, many different strategies for drafting have emerged, such as waiting on a quarterback
(QB), drafting runningbacks (RB) and wide receivers (WR) in the earlier rounds, or waiting on a runningback to 
ensure the top talent in other positions.

Having a good draft has significant implications for the season overall. A manager is able to accept a player drafted
late to underproduce, as the draft capital for the player is not very high and could easily be cut for free agents.
However, if a player drafted within the early rounds (Rounds 1-6) underproduces, it causes significant turmoil since
the manager spent a high capital for the player and would not get equivalent return value for trading the player. 
On the other hand, drafting a sleeper player in the later rounds that massively overproduces becomes a valuable asset 
and is a critical piece of championship teams, as the overall strength of a manager's team is improved with the same 
draft cost in relation to the other teams.

A good draft strategy thus looks to minimize the risk of players within the early rounds, while is also good at finding 
the specific sleepers in the later rounds. 

Additional resources can be found here

* [https://www.espn.com/fantasy/football/story/_/id/34389554/fantasy-football-beginners-how-play-fantasy-football-2022]
* [https://www.espn.com/fantasy/football/story/_/id/39266124/2024-fantasy-football-draft-rankings-strategy-2023-takeaways]
* [https://www.si.com/fantasy/top-10-fantasy-football-rookies-nfl-draft-2024-01hxs07j8ck3]
* [https://www.rotoballer.com/rb-dead-zone-what-is-it-and-do-you-really-need-to-avoid-it/1192614]
* [https://draftwizard.fantasypros.com/football/mock-draft-simulator/settings/]
* [https://www.rotoballer.com/fantasy-football-teams-in-a-vacuum/1164424]

Based on the resources above, we have found the following questions to answer in order to determine the players strategy at 
a particular round.

* Does the runningback dead zone exist?
* Is drafting a quarterback or tight end within the first 3 rounds worth the investment?
* Which position has the most amount of sleepers?
* Which position, runningback or wide receiver provides the most return value in early rounds?

The objective of this project is to use statistics and data science to answer the questions above. We hope that through this
tutorial, the reader will gain a better understanding of the various draft strategies used in fantasy football as well as 
better understand how concepts within data science can more accurately model the performance of NFL players.

## Procedure

We will be using the following datasets

[NFL-Season-DATA](https://github.com/hvpkod/NFL-Data) dataset.
[Average-Draft-Positions](https://www.fantasypros.com/nfl/adp/ppr-overall.php) dataset.

Each dataset contains statistics of NFL players dating back to 2015, with the first dataset detailing their
in season performance and the second dataset containing their average draft positions on various fantasy 
football platforms.

We will track the following seasons: 2020, 2021, 2022, 2023, combining the two datasets together for each season. 

We will then create 4 different data frames represented for each season. If we need to measure a specific player, 
we will aggregate the 4 different dataframes together, and we would exclude players who have retired within the time
frame (2020-2023), meaning 1st, 2nd, and 3rd year players would be included.