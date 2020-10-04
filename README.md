# Election_Analysis

## Overview of Election Audit
We were asked to assist a Colorado Board of Elections employee to accomplish tasks to complete an election audit of a recent local congressional election.  The tasks involved were the following:

1.  Calculate the total number of votes cast.
2.  Calculate the total votes for each county.
3.  Calculate the percentage of votes cast in each county.
4.  Determine the county with highest voter turnout.
5.  Get a complete list of candidates who received votes.
6.  Calculate the total number of votes each candidate won.
7.  Calculate the percentage of votes each candidate won.
8.  Determine the winner of the election based on popular vote.
9.  Print all the results to the terminal.
10. Print all the results to a text file for submission to the election commission.

## Sources
- Data Source: election_results.csv
- Software: Python 3.7.6, Visual Studio Code 1.49.3

## Election - Audit Results
The analysis of the election show that:
- There were 369,711 votes cast in the election.
- The county results were:
  - Jefferson with 38,855 number of votes cast at 10.5% of the total votes.
  - Denver with 306,055 number of votes cast at 82.8% of the total votes.
  - Arapahoe with 24,801 number of votes cast at 6.7% of the total votes.
- The county with the highest voter turnout was Denver with 306,055 number of votes cast at 82.8% of the total votes.\
**The section of code that determined this was:**
```
 # 6f: Write a decision statement to determine the winning county and get its vote count.
        if (CT_votes > county_largest_votes) and (CT_votes_percentage > county_largest_percentage):
            county_largest_votes = CT_votes
            county_largest = county_name
            county_largest_percentage = CT_votes_percentage
```
- The candidates were:
  - Charles Casper Stockham
  - Diana DeGette
  - Raymon Anthony Doane
- The candidate results were:
  - Charles Casper Stockham received 23.0% of the vote and 85,213 number of votes.
  - Diana DeGette received 73.8% of the vote and 272,892 number of votes.
  - Raymon Anthony Doane received 3.1% of the vote and 11,606 number of votes.
- The winner of the election was:
  - Diana DeGette, who received 73.8% of the vote and 272,892 number of votes.\
**The section of code that determined the winning candidate was:**
```
 # Determine winning vote count, winning percentage, and candidate.
        if (votes > winning_count) and (vote_percentage > winning_percentage):
            winning_count = votes
            winning_candidate = candidate_name
            winning_percentage = vote_percentage
```
The analysis can be found in [election_analysis](https://github.com/ABonuan/Election_Analysis/blob/master/analysis/election_analysis.txt).

## Election - Audit Summary
This script, or code, was successfully run on a local election's results.  It's runtime is minimal, showing its efficiency on a large dataset.  It is a flexible code, which can be easily modified because it is readable with comments for each section of the code to tell us what a specific code accomplishes.  It can be modified to used on different districts in the state.  We can run the code on any elections results that each district sends over, as long as they are formatted with the same information \(with Ballot ID, County and Candidate\).

The code can also be modified to be used on a state-wide level election.  It will stiil include Ballot ID, County and Candidate, but with the addition of Districts in the state.  In this case, there will be another column, which will translate to an addition to variables, lists and dictionaries for the districts to iterate through.
