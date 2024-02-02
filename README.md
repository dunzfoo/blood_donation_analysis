>> Objective:
1) Build an automated data pipeline using Python to ingest and analyze daily updated blood donation data from the MoH. *Using both aggregate and granular data
2) To analyze Malaysia's blood donation trends and regularity
3) Output to be dataviz sent directly to a Telegram group by a bot


>> Data Source:
1) Aggregate data: https://dub.sh/ds-data-aggregate > 'donations_state.csv'
2) Granular data: https://dub.sh/ds-data-granular


>> Outputs:
1) (i) Malaysia: Yearly Blood Donations (2006-2023) | (ii) Cumulative Total Blood Donations by State (2006-To Date)
2) Malaysia: Total Contribution from Regular Blood Donors by Year (2006-2023)
3) Daily Blood Donations for the Past 90 Days
4) (i) Yearly Blood Donations by Region (2006-2023) | (ii) Cumulative Total Blood Donations by State, Sorted by Region (2006-To Date)


>> Notes:
1) Completed the whole project using aggregate data as there are some limitations with the granular data. Limitations include:
- Absent of state data
- Start year of granular data as of 2012 as compared to 2006 of aggregate data
- - While the total number of donation is accurate, the number of regular(within 2y)/new/irregular(greater than 2y) donor could not be calculated accurately. Refer to file > bd_analysis_rev00_granular.ipynb
