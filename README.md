FILE			: main.ipynb
PROJECT			: Shaolin AI Assignment 2
PROGRAMMER		: Jack parkinson
FIRST VERSION	: 2024-Mar-24
DESCRIPTION		:
	This file reads in data from two .CSV files and cross-references them to create a report, then analyzes that report. Both the report and the analysis are output as .txt files.
	The PySteak.py file was included with the assignment (for context, I guess?) but I did not use it. I am including it here for posterity.

Program flow:
- Read in CSV data for Menu and Sales into list objects.

- Create a report dict to hold data for each thing on the menu. The report's keys will be unique strings like "spicy miso ramen" and each value being a dict.
	- The second layer dict's KVPs will be count, revenue, cost, profit

- For each sale row, save its description string as a separate variable and check if that's already in the report.
	- If not, add an entry to the report with count/revenue/cost/profit defaulted to 0.

- If the sales item and menu item match, calculate the count/revenue/cost/profit for the sale row. Sum these values with the existing values in the report.
	- If they don't match, output an error message.

- Write out the contents of the report to a text file.

- Analyze the report, then write the analysis to a text file.


 Assumptions:
- The instructions state to create a PySteak folder, and a main.ipynb file within both the root and PySteak folders. There is no mention of the PySteak folder or its .ipynb file elsewhere in the instructions. (Perhaps it's meant to hold the analysis? But that's only an estimation on my part.)
- The instructions say to save a sales item's quantity and menu item ID as seprate variables, but only the sales item ID is needed to check the presence of a sales item in the report. The quantity is not used as its own variable.
- The exact formatting of the error message does not work with the way I have made the for-loops, but the meaning is still the same.
- The loop that involves copying values to the final report could probably be organized better and have some logic exported to a function, but that would only a handful of lines of code.
- The instructions for data analysis mention calculating the most profitable menu item with the date and amount, but the exact date is not needed to determine this (profitability = revenue/time).
- The above is true for the most costly menu item.
