# D3scripts

This is my attempt to create an interactive scatterplot script using D3js

To use ScatterplotUniversal.html (Requires python for step 2):

1. Save ScatterplotUniversal.html to a location of your choosing.
2. Start running a local server on your machine. 
	- Remember the location (current directory) in which you start the local server. It is easiest to start the local server in a 			directory 'above' where you saved ScatterplotUniversal.html
	- See http://chimera.labs.oreilly.com/books/1230000000345/ch04.html#_terminal_with_python for information on doing this.
3. Use a web browser to navigate to:
	- http://localhost:8888/path/to/ScatterplotUniversal.html
		- 8888 refers to the port you started the local server on
		- path/to/ScatterplotUniversal.html is the path to the script **from the location you setup your local server**
4. Fill in the boxes:
	- Path to file:
		- This is the path to the file containing the data you want to visualize.
		- **Again, this refers to the path relative to where your local server was setup.
		- Example:
			- If the file to visualize is located at:
				/home/zwhitfield/Desktop/CodingPractice/d3Projects/DataForAnalysis/Practice/CoveragePractice.tsv
			- And your local server was set up at:
				/home/zwhitfield/
			- Then, 'Path to file:' is (forward slash at front is important):
				/Desktop/CodingPractice/d3Projects/DataForAnalysis/Practice/CoveragePractice.tsv

	- Column number containing x-axis data:
	- Column number containing y-axis data:
		- Enter 0 if pointing to first column of data, 1 for second column etc...
		- So, if trying to visualize a three-column file, with the 1st column on the x-axis and the 3rd column on the y-axis, 
			you would enter 0 for x-axis column and 2 for y-axis column

	- Lower X boundry:
	- Upper X boundry:
		- Data will be filtered and plotted based on data passed to x-axis. These are the min and max values to be plotted on the x-axis

	- Lower Y boundry:
	- Upper Y boundry:
		- These are the desired upper and lower limits of the y-axis

	- Type of Y axis("log" or "linear"; without quotes,case sensitive):
		- As it says, type either log or linear in the box to make the y-axis either a log10 scale or a linear scale.

5. Click Update Axes
	- This will create a graph with the specifications that were entered
	- Use Max Values
		- If this is checked, values entered in Lower and Upper X/Y boundry boxes will be ignored. Instead, the maximum and minimum X 			and Y values (for the entire dataset) will be calculated and used instead.

6. Update Sample button
	- Use this to keep the specifications in the boxes, but update the sample to be plotted by changing the file path to another sample.
	- The points will animate to illustrate the differences between the old and new sample. If visualizing too many points at one (ie 
		xaxis range is large), animation will probably stutter and may not be useful. In that case, just hit "Update axes" button, 			which will still use the path to the new file.
	- ****IMPORTANT: Only use this button if the two datasets being switched between have the SAME NUMBER OF DATAPOINTS. Right now, NAs are 		not tolerated, I plan to fix this soon.
