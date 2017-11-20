# Udacity-Nanodegree-Visualization
<h2> Summary  </h2> 
This chart follows directly from the 'Data Exploration' in R Project and combines two of the 

<h2> Design: Round 1 </h2>

I initially made my designs on Tableau, so that they would be easily shareable on all my colleagues' computer. Here are the links:
https://public.tableau.com/profile/abhishek.pandit1694#!/vizhome/Anandshala_Sample/Disparity?publish=yes
Here was the initial set of decisions:

<h3>Chart Type</h3>
The visualization would be a combination of two charts. 
<br>The first- for the number of students enrolled per grade- would be a bar chart, since this is a count of a categorical variable.
<br> The second- the average academic score achieved in the Hindi language- would be a line chart, since we're measuring a continuous variable over time.

<h3>Visual Encodings </h3>
The chart is a simple line chart, so we have: 
<br>For Chart 1: 
<ol><li> Position X- The school grade </li>
	<li> Position Y- The number (count) of students in that grade </li>
</ol>

<br>For Chart 2: 
<ol><li> Position X- The school grade </li>
	<li> Position Y- The average academic score in that grade</li>
</ol>

<h3>Hierarchy</h3>
There is no hierarchy inbuilt as of now. 

<h3>Legends</h3>
I am not using any colours, shape, etc at the moment. So this is unnecessary.

<h3> Layout </h3>
As stated above, there are 2 charts placed together- one below the other- to make the trends more obvious. I did not want to superimpose the axes on top of each into one graph, as they would .

<h2> Feedback </h2>

After an initial design, I sent it out to some colleagues in email with the following questions:
<ul>
  <li>What do you notice in the chart? Any interesting relationships or trends?</li>
<li> What questions do you have about the data/ graphic? </li>
<li> What do you think is the main takeaway from this chart?</li>
<li> What could make it prettier/ easier to understand?</li>
  </ul>

<h3> Colleague 1 </h3>
Well, i see that as there is increase in students, there is decrease in performance (exam) at the same time, for grade 5-6.
Initially it took me 4 mins to understand the graph then I could understand.
The main takeaway is the rise in number of students as positive, the decrease in result as negative
Yes, definitely this can be made better by following a visual color palette, color tint difference between blocks(i.e. color grows darker from one block to another.) and the trend line in contrast color.or use padding between the blocks. 

<h3> Colleague 2 </h3> 
Hmm... I see a steep rise in enrolment from 5 to 6 grades; a decline in enrolment from grade 7 to 8 (besides Khanpur, the others like less stark / negligible). 
For the marks section, why doesn't the Y axis show till 100%; a line high on the graph seems misleading at first sight, especially since it's showing in percentage.
Also why is the first grade colored differently?

<h3> Colleague 3 </h3>
The percentage chart isn't the right choice. You should be asking 'for Class 5, which are the highest performers.' I would want to know where I have the highest number of students. 5th, 6th, 7th, 8th- which school is getting the best marks?

<h3> Colleague 4 </h3>
When I saw this, it's very evident it's giving enrollment vs  percentage performance. Self-explanatory. For me- as an external person- maybe I haven't seen these kinds of graphs. So for me I'm able to relate to the bigger picture. More than giving me text, this data is really evidence. Shows me a trend between performance and enrollment. So to relate that to the problem is very important.

What did I realize from this process?
<ul>
  <li> At a very obvious level, I didn't want to be misleading. The scale for academic performance had to be from 0 to 100%</li>
  <li> Adding any informatin about Blocks would cause visual overload </li>
  <li> No one was 'getting' the trend I wanted them to see, unless I forced them to! </li>


<h2> Design Round 2 </h2>

After going through feedback, I realized that the movement through time was not evident in the graph. It just appeared as a static line. So the line segment between grades 5 and 6 had had to be highlighted with vertical lines. Almost all my colleagues had asked me immediately what those lines and the shaded area between them represented. Then, as an experiment, I showed them what the graph would look like without the lines. They admitted that the movement would not be obvious. So we were in a catch-22 situation. Couldn't do with the line, couldn't do without it either.

That's when I decided to overhaul the process to a great extent. I wanted the moments through grades to be shown as a story. So animation had to enter the picture. Also, not all data points had to be shown at once. If viewers understood that a large movement had occurred, that too would be sufficient.

A lot of other feedback asked about whether the variable 'Block' may be needed to establish that the line trend occurs in all blocks (and hence universally). None of my colleagues had worked with this data before. So the names of the blocks were alien to them, and added little to the storytelling. So I decided to dispense with that variable.

Instead, there were certain elements of the 'plot' (pun intended) that were being lost. One was the changing gender distribution over time in each grade. The other was the size of the classroom. It was important to highlight that the enrollment numbers truly ballooned in Grade 6. And that one term- balloon- gave me a hint on what to take up next in Dimple.  

<h3>Chart Type</h3>
As per the Dimple website, what I was attempting now was a combination of a bubble chart, pie chart and line chart- an 'animated bubble pie'.

<h3>Visual Encodings </h3>
<ol><li> Position X- The school grade </li>
	<li> Position Y- The average academic score in that grade</li>
	<li> Size of the Pie Chart- size of that grade (number of students)</li>
	<li> Segments of the Pie Chart- percentage belonging to each gender</li>
	<li> Color in the Pie- Gender type. While not essential, it helps make the gender aspect stand out </li>

<h3>Hierarchy</h3>
District blocks are not included. So again, there is no hierarchy to these elements.  

<h3>Legends</h3>
A legend on the right explains the colours of the pie chart.

<h3> Layout </h3>
The entire message is explained in one chart, instead of two. Grades are evenly spread along the x axis. The area to the right of the chart features a legend for gender. 


<h2> Resources </h2>
<ul>
<li>Changing the aggregation method
https://stackoverflow.com/questions/33091706/dimple-d3-plot-average-of-the-values-quick-command-fix</li>

<li>Storyboard Animation:
http://dimplejs.org/advanced_examples_viewer.html?id=advanced_storyboard_control</li>

<li>Vertical Lines in Dimple:
https://stackoverflow.com/questions/29352970/dimple-js-add-vertical-line</li>

<li>2 Dimple Charts on one page:
https://stackoverflow.com/questions/27830399/d3-dimple-how-to-show-multiple-dimple-charts-on-same-page</li>

<li>Titles
https://stackoverflow.com/questions/25416063/title-for-charts-and-axes-in-dimple-js-charts</li>
</ul>
