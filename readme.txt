About the Data: 
This data contains player data from the 2024 NBA Playoffs that spanned from April 2024 to June 2024.
This dataset was downloaded from: https://www.basketball-reference.com/playoffs/NBA_2024_per_game.html
This dataset only contains players that actually played in the games. People who sat on the bench and DNP do not count!

Cleaning the Data:
1.) Remove any unnecessary columns that won't really help out with our data
    - Removed: 'Rk' column, it stands as an index and pandas has built in indexes
    - Everything else is useful
2.) Convert and check for incorrect column data types
3.) Change column names so they are more useful and readable
    - Player -> Player Name
    - Pos    -> Position
    - G      -> Games Played
    - GS     -> Games Started
    - MP     -> Minutes Played
4.) Split Player Name into Two columns

etc.

5.) Clean text columns
    - Not sure if necessary, but use str.strip() for whitespaces on the text columns

6.) Create new per game statistics for: 
    - Points
    - Rebounds
    - Assists
    - Minutes Played
    - Turnovers
    - Personal Fouls
7.) Create new tables for:
    - Offensive Stats
    - Defensive Stats

Analyzing the Data:
Use mean(), min(), max(), count(). etc.
Questions:
1.) How many different teams played in the NBA Playoffs? (This is super easy)
2.) Find min/max/avg or Points and PPG for players who started at least 1 game
    a.) Total Points
    b.) Points Per Game
3.) Offensive Stat Leaders: 
Players that lead the NBA Playoffs in PPG, RPG, APG (Averages are calculated on players who were starters ONLY)
    a.) PPG Leaders
    b.) RPG Leaders
    c.) PPG/RPG/APG Leaders (17 players)
    d.) PPG/RPG/APG Leaders: top 75 percentile in all three averages (5 players)
    e.) SPG/BPG Leaders: top 75 percentile in Steals per game and Blocks per game
        Tried to incorporate bottom 25 percentile in Fouls per game as well but that made it so no one was returned
        6 Players total fit leading in SPG/BPG
4.) Simple Pivot Tables in pandas
    a.) APG/RPG/PPG for all Teams in playoffs
    b.) Number of unique players that started for each team in the NBA Playoffs during each taem's playoff run
    c.) APG/RPG/PPG maxes of all Positions



