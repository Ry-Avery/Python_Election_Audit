# Python Election Audit
Using election results to futher learn Python  

---

## Overview of Election Audit
Previously, I was tasked with writing a script to count the number of votes each candidate received in the election_results.csv file and declare a winner. Now, building off the Python I script already coded, I need to add the voter turnout for each county, the percentage of votes from each county out of the total count, and the county with the highest turnout to my analysis.  

## Election-Audit Results

How many votes were cast in this congressional election?  
- There were 369,711 total votes cast in the election.  

```

Total Votes: 369,711

```

Provide a breakdown of the number of votes and the percentage of total votes for each county in the precinct.  
- Jefferson county had 38,855 voters, which makes up "10.5%" of the total voters.  
- Denver county had 306.055 voters, which makes up "82.8%" of the total voters.  
- Arapahoe county had 24,801 voters, which makes up "6.7%" of the total voters.  

```

County Votes:
Jefferson: 10.5% (38,855)
Denver: 82.8% (306,055)
Arapahoe: 6.7% (24,801)

```

Which county had the largest number of votes?  
- Denver county had the largest voter turnout in the election.  

```

Largest County Turnout: Denver  

```

Provide a breakdown of the number of votes and the percentage of the total votes each candidate received.  
- Candidate Charles Casper Stockham received "23.0%" of the vote and 85,213 number of votes.  
- Candidate Diana Degette received "73.8%" of the vote and 272,892 number of votes.  
- Candidate Raymon Anthony Doane received "3.1%" of the vote and 11,606 number of votes.  

```

Charles Casper Stockham: 23.0% (85,213)
Diana DeGette: 73.8% (272,892)
Raymon Anthony Doane: 3.1% (11,606)

```

Which candidate won the election, what was their vote count, and what was their percentage of the total votes?  
- The winner of the election is candidate Diana Degette, who received "73.8%" of the vote and 272,892 number of votes.  

```

Winner: Diana DeGette
Winning Vote Count: 272,892
Winning Percentage: 73.8%

```

## Election-Audit Summary
Not only can this script be used to tally the results of a local Colorado election, but with some minor modifications, this code could be used with any election dataset .cvs file. A change that you would need to make, would be to change the file paths where the script is reading from and writing to. In lines 9 and 11, you would change the code like this-  

```

file_to_load=os.path.join('folder_name','file_name.csv')
file_to_save=os.path.join('folder_name','file_name.txt')

```

Then, depending on how your dataset is formatted, you would need to change what columns the candidate and county names are being read from. You can easily do this by changing what row each variable is equal to (each comma separates each column). In lines 40 and 42-  

```

candidate_name=row[Column # in dataset starting from 0]
county_name=row[Column # in dataset starting from 0]


```
