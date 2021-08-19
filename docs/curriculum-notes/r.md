# Curriculum Notes: R

## Michael Weisner's Notes on Teaching R

I heavily use the beta Data Carpentry R for Social Scientists curriculum. I think that does a great job because it teaches the basics of R in a way that's very practical. You focus on familiarity to R, basic commands, importing and using data, and then you get exposed to the modern paradigms of Tidyverse, dplyr, and ggplot2 that really make R useful to people. While it's obviously VERY fast I think these are the big points you need to hit and it's what I covered in my Textmining Workshop R Crashcourse.

I think where I differ from some people is that I like to teach people about R Markdown files and codechunks because I think they're better for learning - because you get an interactive notebook and it's easy for users to make notes and see the code in action. It's a little longer and can cause some headaches but I think that it's a more useful product to the learner, both in that they have a clear notebook and that they now know how to use R Markdown files, which are the real bread and butter of using R.

The other thing that I think is really essential is doing everything as live coding. While this is a standard Software Carpentry practice, it's very tempting to have prewritten code or slides but for R I think it's best to make them write it out. Making the code available can be helpful if people are struggling but I don't want people to just sit and run the code because that's not how you learn.

So to me the important steps are as follows:

### Why R?

- R uses powerful command line tools (like Unix)
- R is free and open source
- R is a statistical language rather than a full programming language
- R is great for creating very sharp and customizable graphics (and many other things)

#### Setup

- Familiarize yourself with RStudio's interface
- Understand Projects in R (this is where I show them that Git is very useful and simple from the RStudio IDE)
- Learn about R Markdown Files & Code Chunks
- Basics of R
- Math
- Objects and Variables
- Vectors - what they are, kinds of them e.g. numeric, string, factor
- Common commands to understand data (length(), typeof(), str())
- Subsetting Vectors (including dealing with missing data)
 
#### Data Frames

- What is a data frame (collection of vectors, each column is a vector of the same type and each row is an observation)
- Subsetting data frames

#### Modern R Tools

- Tidyverse - concept of tidy data e.g. tibbles and why they're important for standardizing your data across different tools
- dplyr and manipulating data (select, filter, mutate, group_by, agrrange, count)
- ggplot2 - understanding basic R graphing and why ggplot2 offers a more useful infrastructure for modular, customizable data

Tying it in with Unix and Git, I like to show that you can launch R from the command line and that you can run R scripts from the command line if there's time, but this is tricky because it depends on how they're using the command line.
