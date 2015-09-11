## *Syllabus*

# Interacting With Data

	Brown University, Fall 2015
	BIOL2430-S04 (CRN:14763)
	Topics in Ecology and Evolutionary Biology
	
	Fridays 1-2:50p
	Khoo Multimedia Lab (Room N320), Granoff Center
	
	Instructor: Casey Dunn
	Office hours: Monday 12:30-2:30PM, Room 301, Walter Hall (80 Waterman St.)
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

### September 18 - Version control with git

Reading - Haddock and Dunn, chapter 4 and new chapter

### September 25 - Data wrangling

Reading - Tidy Data- http://www.jstatsoft.org/v59/i10/paper; Haddock and Dunn, chapter 1-3, pages 255-260

### October 2 - Executable manuscripts

- markdown
- knitr
- ipython notebook

### October 9 - Principles of design and static data visualization

Reading: Tufte (the whole book); Haddock and Dunn chapters 17-19

Raster vs. vector

Discussion points:
- Principles of design
- Fundamentals of interface design
- Theory of data representation
- Objectives, eg allowing the audience to imagine a place they could go to, exploring the sublime - http://www.studio360.org/story/how-hubble-brought-color-to-the-universe/

### October 16 - Static data visualization continued
Reading: http://99percentinvisible.org/episode/future-screens-are-mostly-blue/, http://worrydream.com/ABriefRantOnTheFutureOfInteractionDesign/, 

Suggested reading: https://www.youtube.com/watch?v=yJDv-zdhzMY, https://vimeo.com/71278954

Interface design 

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


