# MN Fatal Merging

## 1. Research Question

Are Minnesota drivers worse at merging on the interstate? I have found data that can give numbers around fatal crashes and miles traveled on interstates and interstate junctions. This can be used to answer the question.

## 2. Hypothesis

Part 1: Fatal Crashes at interstate junctions per interstate Vehicle Miles Traveled.
Hypothesis:​
MN has a systematic difference in fatal crashes involving interstate
junctions than other states.

Null hypothesis:​
There is no difference in the number of fatal interstate junction
motor vehicle crashes. 


Part 2: Total Crashes per Year per Mile Traveled by State/year
Hypothesis. Minnesota shows a systematic difference in
number of fatal crashes per mile driven vs the rest of the united
States.

Null: There is no difference in total number of fatal crashes
per mile driven per year in MN vs the rest of the United States. 

## 3. Data Description

CDAN's FARS: Crash Data Analysis and Statistics (maintained by the Nation 
Highway Traffic Safety Administration, NHTSA)​:
FARS is the Fatality Analysis Reporting System, which contains every fatal crash in the US, 
and its extremely detailed. ​

DOT: Federal Highway Administration​:
This data reports the number of miles driven on different categories of roads (functional
systems"), and is often used my researchers to normalize crash counts and analyze roadway 
usage across roadway types and states. ​
The data is produced from a mix of permanent traffic counters, statistical estimations, and 
state DOT submissions to the FHWA, who audits and standardizes the data before
publishing.​

US Census Bureau​:
This data is just used for populations of states by year, merely to validate that Total Vehicle 
Miles Traveled is primarily impacted by the number of drivers in the state. 


How CDAN (FARS/NHTSA) defines Interstate Junction Crashes​:
A crash that occurred at an Interstate interchange or on any
component of the interchange system: ramps, merge points, ramp
terminals, gore points, or crossing structures.

## 4. Methods

Part 1: 
Labels assigned to data (State,
Year, Crash Rate) as MN or Not MN​

Permutation test looks at "Mean
Fatal Interstate Junction Crash
Rate in MN – Not MN", shuffling
the MN label for 10,000 loops. ​


Part 2:
Labels shuffled: MN or Non-MN​
Test Statistic: Fatal Crash per Mile​

Data unit: Yearly (2013-2023)​


Uncertainty: Fatal Crashes per Total Miles Traveled (Per Year by State) - Not CLT Compliant: Not large enough dataset: n = 11.
Minnesota's confidence interval
suggests we have the 2nd lowest rate of 
fatal crashes per mile traveled​.
Note that each state only has 11 data points 
for the 11 years in the data 2013-2023: This 
means that the CLT does not apply in this
case.​

The CLT requires that the data be sufficiently
large, and for each state, we have only n=11
data points.​
For each state, 5000 resampling loops
were ran, and the mean of
"crash_per_mile" was calculated.​

The Std Dev and Upper and Lower
bounds of the CI's were calculated for
each state.

Other Uncertainty Metric: Total crash per mile on state level yearly data - but dropping the state label. n=561, CLT compliant.
This Confidence Interval looks at total crashes per mile driven ​
Data is at a state/year level across 2013-2023. ​
5000 loops were used to resample the data and calculate the mean Crash per Mile for 
each bootstrapped sample.​
This is a CLT distribution this time, as n is sufficiently large, at 561​


## 5. Results

Part 1: p-value is 0.7631, we cannot reject the Null hypothesis. 

Part 2: p-value is 0.0. We can reject the null hypothesis. Additionally the CI for states shows a distinct difference in expected values for MN vs any other state (except MA)

## 6. Uncertainty Estimation

Resampling results:

State level Confidence Intervals:
* Resamples used: 5000
* The bootstrapped CI for all 50 states was extremely interesting, showing MN as a strong outlier vs almost every other state. 
* I interpret this as a strong support for the permutation test that MN is safer to drive in than other states per mile traveled.

## 7. Limitations

Main limitation is a lack of non-fatal data. I can't say with certainty that Minnesotans are NOT worse at merging than other states, but you are at least not MORE likely to experience a fatal accident while merging. I think non-fatal could be very eye opening as maybe merging accidents are just less fatal, and potentially more frequent. 

## 8. References

Dataset details listed above:
https://cdan.dot.gov/query
https://catalog.data.gov/dataset/vehicle-miles-of-travel-by-functional-system-and-state-1980-2023-vm-2
https://www.census.gov/programs-surveys/popest/technical-documentation/research/evaluation-estimates/2020-evaluation-estimates/2010s-state-total.html

---
