# Module_3_Challenge

## Election Results Audit

The Purpose of the Audit

	The purpose of the Election Audit was to show the results of the election for 3 different counties for the 3 Candidates.  The Election Commission also wanted to the percentage of votes for each candidate.  The percentage of votes from the county with the highest amount was also requested by the commission.

## The Results of the Audit

After the audit was completed, it was concluded that Diana DeGette had won the election with receiving 73.8% of the votes in the 3 counties.  Also from the results, it showed that the votes from Denver had the highest percentage of votes from the 3 counties.  In the following set of bullets, you will see what was asked and how it was calculated.

  Total votes of the election
	Each candidate’s total vote count and percentage was also reported
	for candidate_name in candidate_votes:
	.. code:: python
	        # Retrieve vote count and percentage
	        votes = candidate_votes.get(candidate_name)
	        vote_percentage = float(votes) / float(total_votes) * 100
	        candidate_results = (
	            f"{candidate_name}: {vote_percentage:.1f}% ({votes:,})\n")
	
	The winner of the election, winning vote count and winning percentage was reported
	winning_candidate_summary = (
	       f"-------------------------\n"
	        f"Winner: {winning_candidate}\n"
	        f"Winning Vote Count: {winning_count:,}\n"
	        f"Winning Percentage: {winning_percentage:.1f}%\n"
	        f"-------------------------\n")
	    print(winning_candidate_summary)
	
	Each county and its total vote count were printed to the terminal
	pct_countyvote = countyvote / total_votes * 100
	
	        county_results = (
	            f"{county}"
	            f": "
	            f"{pct_countyvote:.1f}% ("
	            f"{countyvote:,})\n")
	
	Each county and its percentage of total votes was printed to the terminal
	The county with the largest number of votes was also printed to the terminal
	 if (votes > winning_count) and (vote_percentage > winning_percentage):
	            winning_count = votes
	            winning_candidate = candidate_name
	            winning_percentage = vote_percentage


## The Summary of the Audit

	The commission can use this script for any election to get voter count and the percentage of votes per county and/or candidate.  It can also be used to get the percentage of votes for each candidate by county as well if the script is modified some.
