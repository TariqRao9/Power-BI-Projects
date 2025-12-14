# Pakistan Super League (PSL) Dataset (2016 - 2024)

## Overview
This directory contains the raw data used for the PSL Performance Analysis dashboard. The data covers *PSL Seasons 1 through 9 (2016–2024)* and provides granular performance metrics for every player and team that has participated in the league.


## Data Source
- *Source:* [Kaggle - Pakistan Super League Datasets](https://www.kaggle.com/datasets/muhammadkhalid/pakistan-super-league-datasets)
- *Platform:* Kaggle
- *Dataset Name:* Pakistan Super League Datasets
- *Author:* Muhammad Khalid
- *Format:* CSV (Structured in sub-directories)

---

## Folder Structure & Contents

### 1. Batting records/
Contains individual batting statistics for all players.
* *Key Metrics:* Runs scored, Balls faced, Batting Average, Strike Rate, Centuries/Fifties.
* *Use Case:* Identifying consistent openers, power hitters (high Strike Rate), and reliable middle-order anchors.

### 2. Bowling records/
Contains individual bowling statistics.
* *Key Metrics:* Wickets taken, Economy Rate (runs conceded per over), Bowling Average, Overs bowled.
* *Use Case:* Analyzing bowler effectiveness in Powerplay vs. Death Overs.

### 3. Fielding records/
Contains data on fielding performance.
* *Key Metrics:* Catches taken, Stumpings, Run-outs.
* *Use Case:* Evaluating the "all-round" impact of players beyond just batting and bowling.

### 4. Team records/
Aggregated performance data for the franchises (e.g., Lahore Qalandars, Karachi Kings, etc.).
* *Key Metrics:* Win/Loss ratios, Toss decisions, Match results per venue.
* *Use Case:* High-level team strategy analysis (e.g., "Does winning the toss lead to winning the match?").

### 5. Timeline data/
Chronological match data linking games to dates and seasons.
* *Key Metrics:* Match Dates, Seasons (2016-2024), Venues.
* *Use Case:* Time-intelligence analysis (e.g., Year-over-Year trends).

---

## Data Dictionary (Common Abbreviations)

To ensure clarity in analysis, the following standard cricket abbreviations are used across these files:

| Abbreviation | Full Term | Definition |
| :--- | :--- | :--- |
| *Mat* | Matches | Total matches played. |
| *Inns* | Innings | Number of times the player actually batted or bowled. |
| *NO* | Not Out | Number of times a batter remained undefeated at the end of an innings. |
| *HS* | Highest Score | The most runs scored by a batter in a single innings. |
| *Ave* | Average | *Batting:* Total Runs / (Inns - NO)<br>*Bowling:* Runs Conceded / Wickets Taken |
| *SR* | Strike Rate | *Batting:* (Runs / Balls Faced) * 100<br>*Bowling:* (Balls Bowled / Wickets Taken) |
| *Econ* | Economy Rate | Average runs conceded per over bowled. |
| *4w/5w* | 4/5 Wicket Haul | Innings where a bowler took 4 or 5+ wickets. |

---

## Usage Notes
* *Data Cleaning:* Minor cleaning was performed in Power BI (Power Query) to handle null values in the "Not Out" columns and to standardize Team Name spellings across seasons.
* *Star Schema:* This data has been modeled into a Star Schema within the Power BI .pbix file, with Batting/Bowling as *Fact Tables* and Player/Team lists as *Dimension Tables*.

