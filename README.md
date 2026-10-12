# Brent-and-WTI-spot-prices-spread-
Analysis of the Brent-WTI crude oil, the two major oil benchmarks, spread (1987 to 2026) in Python including regimes, structural breaks and z-scores.

# Background

Brent, named that as it comes from the Brent Field in the North Sea, serves as a benchmark price for any oil sold in the region. The two biggest benchmarks in the world are Brent and WTI, standing for West Texas Intermediate, and a sizeable portion of the world's oil is priced at those benchmarks, there are others but it makes sense to compare the two biggest and also because they are very similar types of Oil. Brent is a very sweet type of oil, meaning it has a very low sulphur content, WTI is also sweet but not to such an extent that Brent is, though close enough to warrant comparison. They also have similar API gravity, both are very light. API gravity is a measure of how heavy the oil is compared to water, higher than 10 means it floats and is light, less than 10 being the opposite. So they are similar types of oil but are transported in different ways. Brent is drilled from the North Sea, meaning it can directly be transferred off the offshore oil rigs and transported across the world. On the other hand, WTI is inland and so requires higher transport costs to move it to the coast if it was to be traded intercontinentally. You can assume the spread is therefore pretty uniform, spread being the difference in spot oil price. The question we want to answer is, does the spread diverge? The answer is almost certainly yes, Real word events influence how oil is traded, so the follow-up question is, if so why does it diverge and when? What key events can we say causes the spread to diverge?

# Data

Both Brent and WTI spot prices can be found on FRED, the Federal Reserve Bank of St. Louis, for free and mostly daily. They can be downloaded as csv or excel, though I chose to use csv specifically to use pandas. It should be noted that not every day was traded on, nor did they start recording at the same time. The data must be cleaned before we can actually plot and analyse. This is where python and pandas is useful.

# Methodology

The first job is clean the data. I cleaned the data using pandas, indexing the data by date and removing days they did not have in common. I then removed any day that was not traded on by either benchmark, so no NaN data in the dataframes as they cannot be plotted. The next step was to then plot the spread. Though, you will see I plotted both benchmarks too as I wanted to illustrate where the spread comes from and identify key events in the historical data. I then calculated the mean and standard deviation using the describe function. I shall explain a limitation of this later. The next step is to calculate a z-score using the historical mean and standard deviation. This shows us how far any spot oil price deviates from the historical mean as a multiple of the historic standard deviation.

# Findings
