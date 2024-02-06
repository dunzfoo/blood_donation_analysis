## Objective:
1) To build an automated data pipeline using Python to ingest and analyze daily updated blood donation data from the MoH. *Using both aggregate and granular data
2) To analyze Malaysia's blood donation trends and regularity
3) Output to be dataviz sent directly to a Telegram group by a bot

## Data Source:
1) Aggregate data: https://dub.sh/ds-data-aggregate > 'donations_state.csv'
2) Granular data: https://dub.sh/ds-data-granular

## Outputs:
1) (i) Malaysia: Yearly Blood Donations (2006-2023) | (ii) Cumulative Total Blood Donations by State (2006-To Date)
2) Malaysia: Total Contribution from Regular Blood Donors by Year (2006-2023)
3) Daily Blood Donations for the Past 90 Days
4) (i) Yearly Blood Donations by Region (2006-2023) | (ii) Cumulative Total Blood Donations by State, Sorted by Region (2006-To Date)

## Definition:
**Donor Regularity** - Source: [KKMNOW Blood Donation Dashboard](https://data.moh.gov.my/dashboard/blood-donation)
| Categories | Definition | 
| ---------- | ---------- |
| New donor | First donation |
| Regular donor | Donated within 2 yrs |
| Irregular/lapsed donor | Donated > 2yrs ago | 

## Notes:
Completed the project using aggregate data as there are some limitations with the granular data. Limitations include:
- Absent of state data
- Start year of granular data as of 2012 as compared to 2006 of aggregate data
  - While the total number of donation is accurate, the number of regular/new/irregular donor could not be calculated accurately. Refer to file > [bd_analysis_rev00_granular.ipynb](https://github.com/dunzfoo/blood_donation_analysis/blob/main/bd_analysis_rev00_granular.ipynb)
  - *Added on 6/2/24: Wrongly assumed granular data were completely sorted by donor_id, values were close to aggregate data (more accurate) when sorted by donor_id before categorizing by donor regularity. This could then be incorporated to the project to generate output 1(i), 2 and 3* 
