# Knight Center MOOC : "[Data Visualization for Storytelling and Discovery](https://journalismcourses.org/DE0618.html)"
###### 11/6/18 - 8/7/18

Alberto Cairo

## Syllabus
### Module 1: What is data visualization
This week offers an introduction to visualization, what it is, how it works, and what ethical considerations are involved in its design. It also teaches how to prepare data before visualizing it. This week you will learn:

* What data visualization is
* Visualization ethics: How visualization may mislead, and how it can tell the truth
* Data preparation: an explanation of the software videos this week

WK1 Exercise :

"_Based on what you’ve learned on the video lectures and the readings, see the following two graphics and write a critique of at least one of them; then, engage in conversation with other students_"

![Who's Buying What?](WhoIsBuyingWhat.png "original")

![Who's Buying What?](Screenshot_2018-04-23_18.00.22.png "final redesign, from IGDV1115")

![Life Expectancy Singapore](LifeExpectancySingapore.png "original")

![Life Expectancy Singapore](LifeExpectancySingapore_redesign.jpg "research, critique notes, redesign sketches")

---

### Module 2: Data exploration
This week covers how visualization can be used to explore and discover features that often hide behind data. We’ll use software tools that will allow us to import a data set and then visualize it in multiple ways to reveal patterns and exceptions to those patterns. This week you will learn:

* INZight for data exploration
* How to find outliers when analyzing data.
* Using histograms and seeing summary statistics
* Scatter plots. Trends and outliers
* Using maps

**WK2 Exercise** :

"_Look for an interesting data set in public sources (https://data.worldbank.org/ or any other public source for global, national, or local data), explore it, and write down what interesting features you've find in it. Send your contribution to the forum. Comment on at least the contributions of 3 other students_"

**[DE0618][MDAB][Mod2] WorldBank > SDGs > Poverty%** :

><As requested, I've provided links to the visuals I mention (rather than inserting them). Also links to my wrangled csv datasets. If I missed any links, the files are all in [https://github.com/mbeveridge/DE0618]>

>**I used data.worldbank.org and iNZight**, to support the choices of the MOOC (and what I assumed other people would be doing, or want to try and copy)

>data.worldbank.org pointed at 17,420 datasets in the Data Catalog [https://datacatalog.worldbank.org/], with "**Sustainable Development Goals**" [https://datacatalog.worldbank.org/dataset/sustainable-development-goals] in "Featured Data" at the top. That said 217 Economies over 50+ years (1960-2017), so hopefully had something interesting

>--

>Data was actually only for 1990-2017 (with a lot of gaps). But was unwieldy for this Exercise (SDGData.csv is 30MB, with ~94000 rows that include 357 Series), so chose one 'interesting' Series (as iNZight Lite has 5MB limit) ...SI.POV.DDAY : "**Poverty headcount ratio at $1.90 a day (2011 PPP) (% of population)**", that I'll call 'Poverty%'

>DataWrangler (in browser) was 'unresponsive' when I tried, but with Trifacta Wrangler I eventually got a 970KB 'Tidy' csv file that loaded into iNZight Lite ...[SDGData_Poverty_TIDY.csv]. That kept freezing when I tried to Visualize/explore the data, so I moved to iNZight on desktop

>The data was a little disappointing (and I'd seen similar before, from other 'sources'), and iNZight a bit 'tricky'. Ultimately the only fields I had available to explore were Year and 'Poverty%' for 263 Countries (and it was **complicated by frequent uncertainty of missing values). In the absence of a Region field, I manually selected the Countries for regions of MiddleEast, south-central-asia and finally south-of-sahara** (several times) ...creating small multiples for value v's Year and maps

>MiddleEast : **declining in Iran (but always fairly small %'s), rising fast in Yemen (but only 3 data points)**

>[value_Year_MiddleEast.pdf]

>south-central-asia : a number of **'ex-Soviet' countries had similar patterns of high-points ~2000 (USSR dissolved 1991?), then sharp falls (but pre-2000 data was scarce)**

>[value_Year_south-central-asia.pdf]
>[value_Year_south-central-asia_maps.pdf]

>south-of-sahara : A bit more up&down, rather than down for all countries. And the rates are higher. **DR Congo and some others had some v high Poverty% values, probably related to war/refugee**

>[value_Year_south-of-sahara.pdf]
>[value_Year_south-of-sahara_maps.pdf]

>--

>**Let's try looking at more than one Series on the same chart**. SO need more data

>Using Trifacta to make the initial SDGData.csv 'Tidy' for Years (but keeping all the series, in rows) created a 359MB csv file. Again that seemed too unwieldy for this, so I kept only the years ending '2' and '7' (6 of 28 Years), giving 77MB csv file ...[SDGData_92-17_TIDY.csv]

>I hoped to plot a trellis chart (small multiples of scatter plot) of 'all' the variables (before gradually removing some), to identify some pairs that looked worth investigating further. I couldn't figure out how to do that with iNZight (which I think is because I needed to pivot the data ...though that would try to create more columns than I think allowed by the free Trifacta Wrangler, or DataWrangler)

>I ended up plotting value v's Year for all the indicators, to see if any had an interesting range of values ...But **all that showed was that I had a few GDP/GNP indicators**

>[value_Year_IndicatorCode.pdf]

>--

>**Finally, then, I decided to just pick an extra Series (GDP)**, and used Trifacta to make the initial SDGData.csv 'Tidy' for Years (unpivot), with values for Poverty% and GDP in 2 separate columns (pivot) created a 349kB csv file ...[SDGData_Poverty+GDP_TIDY.csv]

>**Plotted Poverty% v's GDP** subset by Year (I don't know why it plots 7-year groups together), which gives 4 plots of an **unsurprising shape (showing negative correlation between Poverty and GDP)**, that might benefit from filtering by Region and colouring/sizing the points (which I didn't find in desktop version of iNZight yet)

>[Poverty_GDP_Year.pdf]

>At this point, I called an end to it. I had more ideas, but not the hours to spend

>--

>**Ultimately then, this was frustrating**. I got a little more familiar with the tools and data, but the breadth of the data and limitations of tools (and lost/repeated work) meant slow progress/wasted time. (To get an attractive/ satisfying/ quick outcome I'd have chosen both differently, but I also expected that at the start.) To complete this course **I can't spend more than the last couple of days on this Exercise, so (so far) have little to show you - sorry**

---

### Module 3: Visualization for communication
This week explains how visualization can be used to communicate with the public. We’ll use a new tool, Flourish, to design static and interactive maps and charts, and then put them together in sequential narratives. This week you will learn:

* How to choose graphic forms for your data
* Stories with charts and maps
* Visual design for communication
* Software tools: an introduction to this week’s practical videos

**WK3 Exercise** :

"_Take the U.S county data set I used in the Flourish tutorials — or any other similar data set you wish. Select one of the potential stories you spotted, do more research about it, and then design a visualization or a series of visualizations to tell that story. Send a message to the discussion forums with a link to your project and a short description of it. Critique at least TWO other projects by other students_"

**"[DE0618][MDAB][Mod3] County.csv + Flourish for story structure"** :

![Mod3_Exercise](Mod3_Exercise_notebook.jpg "initial notes on fields and chart types")

[https://public.flourish.studio/story/11341/](https://public.flourish.studio/story/11341/)

>_[I did this on 11/7, but unfortunately lost my original post/notes when the platform shut down. So I'll make brief comments, and try to answer questions if there are any.]_

> I'd been through the Flourish tutorials, and wanted to practice with that tool. I had the County data and was interested to see if it was interesting!

>I wanted to avoid simply creating extra columns in Excel to get around difficulties/unfamiliarity. I was willing to look for other datasets if I found a story (especially if I could combine them in Flourish).

>The data (and absence of a time field) limited the chart types I considered would be interesting. I also couldn't make Flourish aggregate the County data into State/Region totals (the way I think Tableau could?).

>I wanted to try out the structure of a story, even if the data didn't support something 'compelling' ...and I don't think it did.

>So, I tried to set the scene and then looked at whether Poverty% might be linked to voting patterns. (And I tried other variables too, but didn't save them.)

>I found Flourish quite 'clunky' for this - trying to keep in mind what point I was trying to make, across several slides, when it was so slow to load each one and didn't show thumbnails of the actual charts. (And I'd have used colours in some slide titles, but couldn't find a way. Same for some other things. I'd have liked to put comments on the face of charts, but couldn't, so think I would next put a lot more detail in the slide title ...which I don't think it was designed for).

---

### Module 4: Final project and next steps
We’ll use this week to design a visualization based on a topic and datasets of your choice. This week you will learn:

* Other resources you can consult to keep learning about visualization.
* Live Hangout: An Interview with Google News Lab’s Simon Rogers

**WK4 Exercise** :

"_Do your research and design your visualization. Submit it via the discussion forums as a link and a short description. Give feedback to at least TWO other students_"

**"[DE0618][MDAB][M4] Singapore Life Expectancy"** :

>TL;DR : [https://public.flourish.studio/story/11610/](https://public.flourish.studio/story/11610/) : link to the story in Flourish

>--

>In Module 1 (Option 2) we critiqued a visualisation about Life Expectancy (1990, 2000, 2009 data), from the "Affordable Excellence" book about the Singapore healthcare system. It included sketching a couple of redesigns

>In Module 3 we used the Gapminder (1952-2012) dataset (and Gapminder2012 extract) and the Flourish tool

>--

>In Module 4 I wanted to bring this back to Module 1 :

>1. to see if it was possible to create the Mod1 redesigns in Flourish, by importing the '2' Gapminder datasets (and without deleting/filtering data pre-import ...which would reduce the scope for exploration and require many more files to be managed)

>2. to consider whether increased Singapore Life Expectancy demonstrates the success of the Singapore healthcare system...

>[From my Mod1 post] : What are we most interested in? : Purpose seems to be demonstrating the success of Singapore ["In just 50 years, Singapore transformed itself ... from a country with poor health outcomes to one of the best in the world" -- "Affordable Excellence" book]. The 29-year charts don't cover that 50-year period and most countries appear to have improved decade-on-decade

>--

>And to re-assess how 'easy' it is to work on a Story in Flourish

>[https://public.flourish.studio/story/11610/](https://public.flourish.studio/story/11610/)

---

![certificate](DE0618_Certificate.png "certificate")