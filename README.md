# Election_Analysis

## Project Overview
Scenario: A Colorado Board of Elections employee has given a list of task to complete as part of an audit of a local congressional election.

1. Calculate the total number of votes cast.
2. Get a complete list of candidates who recieved votes.
3. Calculate the total number of votes each candidate received.
4. Calculate the percentage of votes each candidate won.
5. Determine the winner of the election based on popular vote.

## Resources
- Data Source: election_results.csv
- Software: Python 3.6.1, Visual Studio Code, 1.50.0

## Audit Results
The analysis of the election show that:
- There were 369,711 votes cas in the election.
### County
 - The counties were:
    - Jefferson
    - Denver
    - Arapahoe
- The candidate results were:
    - Jefferson received 10.5% of the vote and 38,855 number of votes.
    - Denver received 82.8% of the vote and 306,055 number of votes.
    - Arapahoe received 6.7% of the vote and 24,801 number of votes.
- The county with the largest turnover:
    - Diana DeGette, who received 82.8% of the vote and 306,055 number of votes.
    
### Candidates
- The cadidates were:
    - Charles Casper Stockham
    - Diana DeGette
    - Raymon Anthony Doane
- The candidate results were:
    - Charles Casper Stockham received 23.0% of the vote and 85,213 number of votes.
    - Diana DeGette received 73.8% of the vote and 272,892 number of votes.
    - Raymon Anthony Doane received 3.1% of the vote and 11,606 number of votes.
- The winner of the election was:
    - Diana DeGette, who received 73.8% of the vote and 272,892 number of votes. 
 
## Audit Summary
The script can be modified in many ways to make it viable to analyze any election at any level, provided the correct input format of the data.
### Input
The .csv file of the data must follow the format below and be named "election_results.csv":
> Ballot ID,Region-Level,Candidate

### Region-Level
The current codes counts the votes at the region level and prints the results to a .txt file. After making the change in the Input format the code needs to be modified to be versitile to different levels of elections.
To do this, the program can read the headers of the .csv columns and determine if the elections are county, state or national. This specification can then be used to specific if "county" or "state" or "district" should be the title in the print out.

### Region-Level Statistics
As the program already collects the votes cast in each county and votes cast for each candidate, using a dictionary of dictionaries to store the data would allow for a breakdown of the voting statistics by counties.
This would involve creating a dictionary with each country being the key. Each key would lead to another dictionary, where the keys would be the possible candidates and they would lead to the votes. Then the existing code for vote counting can be utilized using the dictionary of dictionaries to collect the data of the voter breakdown of candidates by county. 
> election_stats = {County:{Candidate:Number_Of_Votes}}

This election breakdown by region-level can then be used to provide analysis of the national elections and account for the electoral college system by providing state by state wins. It would also be useful to provide data on which regions won or lost. 
