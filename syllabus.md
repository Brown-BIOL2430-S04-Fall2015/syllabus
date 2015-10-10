## *Syllabus*

# Interacting With Data

	Brown University, Fall 2015
	BIOL2430-S04 (CRN:14763)
	Topics in Ecology and Evolutionary Biology
	
	Fridays 1-2:50p
	Khoo Multimedia Lab (Room N320), Granoff Center
	
	Instructor: Casey Dunn
	Office hours: Monday 1:00-2:30PM, Room 301, Walter Hall (80 Waterman St.)
	Prepend the subject line of all course related emails with "data: "


Science is becoming more data intensive, and at the same time new tools are allowing scientists to interact with data in new ways. This seminar will explore the potential impacts of these new ways of interacting with data on the practice of science, how these approaches can be used most effectively (with an emphasis on design and human perception), and introduce students to some tools that embody these changes, including version control (https://git-scm.com/), executable manuscripts (http://yihui.name/knitr/), and interactive visualizations (http://d3js.org/).

Please complete the [survey](http://goo.gl/forms/wf8AyzW8nw) if you register for or intend to sit in on the seminar.

## Class format

Classes will consist of discussions, labs that examine particular tools tools, and student presentations. The schedule includes topics for each class, and conversation points to seed class discussions. There will be a strong focus on human perception as it relates to insight and on principles of design.

After the first meeting, and prior to the project presentations, the discussion for each class will be led by one or more students. These students will meet with me during office hours on the Monday preceding the class to map out the plan for the discussion.

## Course site

All materials for the course, including the syllabus, are available at the [course site](https://bitbucket.org/caseywdunn/data_interaction). The [syllabus](https://bitbucket.org/caseywdunn/data_interaction/src/master/syllabus.md) will be updated as the course progresses, please check it weekly. Please submit suggestions and corrections for the class via the [issue tracker](https://bitbucket.org/caseywdunn/data_interaction/issues).

## Projects

Each student will create an interactive analysis/visualization based on their own work, publicly available data, or a published scientific paper. This project will presented in class at the end of the course. They will be developed and submitted in a git repository.


## Reading

Reading includes book chapters, online resources, and videos to be watched ahead of class. The dates the readings will be discussed in class are listed in the schedule, but some will be useful to you much earlier as you work on your projects. In addition, the reading load is very uneven. On light weeks, it is good to get a jump on reading for future weeks.

Tufte, ER (2001). The Visual Display of Quantitative Information, 2nd edition. [amazon](http://www.amazon.com/The-Visual-Display-Quantitative-Information/dp/0961392142)

Murray, S (2013). Interactive Data Visualization for the Web. [online](http://chimera.labs.oreilly.com/books/1230000000345/index.html)

Haddock, SHD and CW Dunn (2011). Practical Computing for Biologists. [amazon](http://www.amazon.com/Practical-Computing-Biologists-Steven-Haddock/dp/0878933913/ref=sr_1_1)


## Schedule

### September 11 - The practice of working with data and the landscape of scientific publishing

Reading: Murray - chapters 1, 2
Assignment: In the next couple days, use the issue tracker to submit a visualization or two that you particularly like.

Intro to class, description of final projects

Investigators interact with data in several ways:

- Data management and wrangling
- Data exploration
- Data explanation
- Communication and sharing of data and results

Designing analyses, implementing analyses, and running analyses are often treated as different tasks. In many studies, the investigator moves data through each stage of analysis by hand, which takes a long time and is error prone. Automated and interactive analyses separate the design/implementation of analyses from running analyses, and make running analyses very easy and reliable. This means that you can repeatedly run analyses before you collect your data (using simulations or other datasets), as you collect your data (to check data quality and assess how many more data are needed), and after you collect your data (to refine and extend analyses). This doesn't just speed up analyses, it fundamentally changes the way they are approached.



There used to be a small number of models of scientific publication, now there are many.

These models vary in a few key dimensions:

- Access. Paid, open.
- Data availability. Proprietary, available on request, public archives.
- Analysis method availability. Proprietary, described in human readable form, described in machine readable form.
- Static vs. dynamic. eg one-time publishing, iterated changes with version control, comments, etc
- Review. Editor selected anonymous, non-anonymous, private vs public reviews, crowd sourced

Other recent developments:
- Register projects before they are done to ensure complete reporting of results

What are missing publication models?

### September 18 - Version control with git; Survey of visualizations 

Reading - Haddock and Dunn, chapter 4 and new chapter

Walk through git example

Intro to markdown

Discuss participant-submitted visualizations


### September 25 - Data wrangling; web fundamentals

Reading - Tidy Data- http://vita.had.co.nz/papers/tidy-data.html ; 
Haddock and Dunn, chapter 1-3, pages 255-260;
Murray chapter 3

Before class, install:

- [Sublime Text](http://www.sublimetext.com/3)

#### Tidy data

See Haddock & Dunn Figure 15.1 for examples of messy and tidy data.

Key points from Wickham's Tidy data paper:


- *Tidy data* have the following properties: Each variable forms a column, each observation forms a row, each type of overvational unit forms a table.

- *Melting* is the process of stacking data such that data from different columns is then in different rows. it results in a dataset with fewer columns and more rows. A completely moltedn dataset is a triple store (three columns that store object, attribute, and value).

- *Casting* is the process of unstacking data so that information for a single observation that is spread across multiple rows is placed in multiple columns.

- *Tidy tools* input tudy data and output tidy data. If you have tidy data and tidy tools, no munging is needed to format the output of one analysis step so that it is ready for the next analysis step. i.e., all your code relates is focused on analysis.

- *Visualization* is the process of mapping variables to aesthetic attributes of a graph (eg, defining which variables specify position).

#### Regular expressions

See `regex` folder.

#### Web fundamentals

To view web sites locally, rather than just double click the html file it is best to run them through a web server. This makes sure that javascript etc renders correctly. The simplest is python's simple server:

    cd website_dir/
    python -m SimpleHTTPServer

Where `website_dir` is the directory with your site files. Once it is running, enter the url (eg http://localhost:8000/) into your prowser to see the rendered page.

Download the [example code](http://bit.ly/V25Xw6) for the Murray book expand it, then `cd` to the folder and launch the simple server. Explore the examples in your browser.

### October 2 - Executable manuscripts

Reading: Murray chapters 2,4,5,6


Before class, install:

- [R](https://cran.cnr.berkeley.edu/)
- [R Studio](https://www.rstudio.com/)
- [knitr](http://yihui.name/knitr/), install via the R package manager rather than as a separate download
- [pandoc](http://pandoc.org/)


The two topics today have a lot in common. We embed R code in markdown documents that changes the document according to data when executed by knitr. We embed d3 javascript in html documents that changes the document according to data when executed by the browser.

#### Executable manuscripts

Markdown

- A markup language for writing text that plays particularly well with executable manuscripts and git. Includes formating information for rendering to other file formats, eg pdf, html, or docx. But looks good as plain text too. Comes in several flavors.
- `pandoc` is a great tool for rendering markdown to other formats. Can accommodate bibliographic data as well.
- [Bitbucket flavored markdown](https://bitbucket.org/tutorials/markdowndemo). This is a good general intro to the most commonly used features, and is consistent with most other flavors.
- [`pandoc` flavored markdown](http://pandoc.org/demo/example9/pandocs-markdown.html). Includes functionality relevant to academics, eg bibliographies.
- [Original markdown flavor](https://daringfireball.net/projects/markdown/).
- There are a variety of realtime markdown editors, like [Mou](http://25.io/mou/).

Executable manuscripts with knitr

- R code is embedded in document text. Document text can be formatted with latex or markdown. The document threfore contains a mix of executable R and marked up text. Markdown documents with embedded R code have a `.rmd` extension.
- Document is executed with the R `knitr` package, which renders code and code output to latex or markdown. This produces a document that is just marked up text.
- The marked up text document can then be rendered to another format, eg pdf, with a render engine like pandoc.
- Most R code is in chunks, multiline code blocks, whose formatting can be controlled as a unit.
- A variety of options are available to control what is done with chunks. `eval` specifies if the code is evaluated (ie, run). `echo` controls if the code itself is included in the final document. `include` controls if the results of running hte code (eg plots) are shown in the document.
- R code can also be inline with text. This is useful for putting particular results right into sentences etc.
- Many more details available in `knitr` [documentation](http://yihui.name/knitr/).
- See [example](https://bitbucket.org/caseywdunn/executable_paper)
- RStudio has native support for 


#### D3 continued

There are a variety of great online courses for learning javascript. If you don't have experience with javascript, check them out. See, for example, the courses at [code agademy](https://www.codecademy.com/tracks/javascript) and [code school](https://www.codeschool.com/paths/javascript). 

The basics of drawing with data.

### October 9 - Principles of design and static data visualization

Reading: Tufte (the whole book); Haddock and Dunn chapters 17-19

#### Principle of design

Visualization is the act of mapping data to aesthetic properties. The principles of design clarify which aesthetic properties we have to work with.

Some examples:

- [example](http://p2cdn3static.sharpschool.com/UserFiles/Servers/Server_2879574/File/teacher-documents/Performing_Visual_Arts/Middleton/2-D%20II/Elements%20and%20Principles%20Overview.jpg)
- [example](http://paper-leaf.com/blog/2012/10/principles-of-design-quick-reference-poster/)


#### Tufte discussion

Different participants will discuss different chapters:

1. Robert Lamb, Cat Munro
2. Chris Arellano, Becca Wang
3. Tyler Dae Devlin, Jack Diedrich
4. Xiaojun Meng
5. Alejandro Damian Serrano, Carlos Silva
6. Yi (Jamie) Zhang, Bianca Brown
7. Joaquin Nunez
8. KC Cushman, Stephen Rong, Daniel Kunin
9. Denise Yoon, Adam Spierer, Yun-hsuan 'Leslie' Lai

Counter point - Jer Thorp: I have millions of pixels

#### Raster vs. vector

- Time point 2:40 of http://acko.net/tv/pixelfactory/

#### Further discussion


Thoughts:

- Tufte's "minimum ink" is really about stripping out aesthetic elements that aren't mapped to data.
- Sometime valuable to have ink that doesn't map to data when it improves the visual metaphore. eg, when longitude and latitude of data points are mapped to x y coordinates in a plot, geographical features help put the position aesthetic in context.
- Sometime valuable to have ink that doesn't map to data when it succeeds in making the plot more visually compelling. Minimal isn't always the most beautiful, or most quickly understood.
- "Minimum ink" is a very useful reference point. It defines what is essential to portraying the data. Good to figure out what that point is for your visualization, then back off of it as needed.
- Dynamic plots allow more minimal visual style. With zoom/ filter/ details on demand, there can be less information on the screen at any given point in time for a visualization to convey the same amount of information overall.
- Motion can be an aesthetic mapped to data (eg magnitude and frequency of jiggle). Or it can be for continuity in transitions, in which case motion can simplify the aesthetic representation of data since fewer mappings are shown in any given view.


Best practices for modern media:

- Don't map any given datam to more than one aesthetic property. Creates redundancy.
- Be deliberate about using aesthetic properties that don't map to data.
- Minimize the number of aesthetic properties that map to data in any given view.
- Be as consistent as possible about aesthetic mappings across views. eg, if different views depict different things on the y, use color in the same way across views.


### October 16 - Tufte continued, d3 continued

Reading: Tufte (all), Murray chapters 7-9.


### October 23 - Interactive data visualization

Reading: Murray (the whole book); Jer Thorpe video; Bret Victor video; "Visual Information-Seeking Mantra: overview first, zoom and filter, then details on demand." [Shneiderman 1996](http://www.mat.ucsb.edu/~g.legrady/academic/courses/11w259/schneiderman.pdf)

Dynamic interactions:

- Allow the user to decide which view they see
- Allow motion as a design element
- Transitions to improve continuity and cohesion between views

A spectrum of approaches:

- graphic - single view, constrained perspective
- animation - multiple views, constrained perspective
- interactive - multiple views, flexible perspective

Exploration needs to be very unconstrained, exposition requires that the author direct the audience perspective through constraint. The extreme of constrained dynamic perspective is a video.

Imagine a VR movie without any constraint, where the audience could roam anywhere they like. They would be far from all the key action and have no idea what the movie was "about". Maybe the best exposition is fully constrained. These trade-offs are well illustrated by http://www.fallen.io/ww2/ . 


### October 30 - Interactive data visualization continued

### November 6 - Topic To Be Determined

### November 13 - Open lab to work on projects

### November 20 - Summary, open discussion

- How will lines blur between data management, exploration, explanation, and publishing?

### December 4
Project presentations

### December 11
Project presentations



### Other things (further reading, stuff that doesn't fit cleanly into above topics)

Reading: http://99percentinvisible.org/episode/future-screens-are-mostly-blue/, http://worrydream.com/ABriefRantOnTheFutureOfInteractionDesign/, 

Suggested reading: https://www.youtube.com/watch?v=yJDv-zdhzMY, https://vimeo.com/71278954

Interface design 

