# Curriculum Notes

## Michael's Notes on Teaching R

I heavily use the beta Data Carpentry R for Social Scientists curriculum. I think that does a great job because it teaches the basics of R in a way that's very practical. You focus on familiarity to R, basic commands, importing and using data, and then you get exposed to the modern paradigms of Tidyverse, dplyr, and ggplot2 that really make R useful to people. While it's obviously VERY fast I think these are the big points you need to hit and it's what I covered in my Textmining Workshop R Crashcourse.

I think where I differ from some people is that I like to teach people about R Markdown files and codechunks because I think they're better for learning - because you get an interactive notebook and it's easy for users to make notes and see the code in action. It's a little longer and can cause some headaches but I think that it's a more useful product to the learner, both in that they have a clear notebook and that they now know how to use R Markdown files, which are the real bread and butter of using R.

The other thing that I think is really essential is doing everything as live coding. While this is a standard Software Carpentry practice, it's very tempting to have prewritten code or slides but for R I think it's best to make them write it out. Making the code available can be helpful if people are struggling but I don't want people to just sit and run the code because that's not how you learn.

So to me the important steps are as follows:

## Why R?

- R uses powerful command line tools (like Unix)
- R is free and open source
- R is a statistical language rather than a full programming language
- R is great for creating very sharp and customizable graphics (and many other things)

### Setup

- Familiarize yourself with RStudio's interface
- Understand Projects in R (this is where I show them that Git is very useful and simple from the RStudio IDE)
- Learn about R Markdown Files & Code Chunks
- Basics of R
- Math
- Objects and Variables
- Vectors - what they are, kinds of them e.g. numeric, string, factor
- Common commands to understand data (length(), typeof(), str())
- Subsetting Vectors (including dealing with missing data)
 
### Data Frames

- What is a data frame (collection of vectors, each column is a vector of the same type and each row is an observation)
- Subsetting data frames

### Modern R Tools

- Tidyverse - concept of tidy data e.g. tibbles and why they're important for standardizing your data across different tools
- dplyr and manipulating data (select, filter, mutate, group_by, agrrange, count)
- ggplot2 - understanding basic R graphing and why ggplot2 offers a more useful infrastructure for modular, customizable data

Tying it in with Unix and Git, I like to show that you can launch R from the command line and that you can run R scripts from the command line if there's time, but this is tricky because it depends on how they're using the command line.

## Alan Croswell's notes on the Software Carpentry curriculum

### Unix Shell

- man pages missing from git-bash on windows. Fix: "google man ls"
-   macos `ls \--help` doesn't work (it's too BSDish to have the
        `> --help` switch)
- `sort -n lengths.txt` gives the same result without `-n`
        > because wc's output is left-padded and spaces collate
        > differently on MacOS vs. Linux. See
        > [*\#810*](https://github.com/swcarpentry/shell-novice/issues/810).
        > LANG=C vs. LANG=en\_US.UTF8. A better example would use
        > left-aligned numbers.

- Tab completion doesn't appear to work in git bash on Windows

- Python

- Use of jupyter lab vs. notebook -- doesn't really matter but
        > since the syllabus uses Lab, we should too.
- Someone asked about web scraping, which isn't covered in this
        > lesson. There's is a LC lesson on web scraping with Python and
        > the use of Xpath, which may be a good more advanced workshop
        > to run during the semester.

- There was one case I noticed in the Beta Python lesson that the
        > exercises referenced datasets that were not included in the
        > setup data, which made it non-useful.

## Non-US Keyboard

- French Mac has no \~ (googled: use option-N but that doesn't
        > work on US keyboard). In SWC slack the answer was these keys
        > are on option-numbers. Certainly not the case on my US
        > keyboard.... Added [*this int\'l keyboard info to the
        > workshops
        > wiki*](https://github.com/carpentries/workshop-template/wiki/Configuration-Problems-and-Solutions#international-keyboards).

- international students don't always know the names for single
        > vs. double quotes, tilde, etc.

### Git

- git lesson setup page doesn't say to create a github.com
        > account; only in the git download instructions. Might be
        > better to say it here as well.

- We didn't get to collaboration via github PR's, merges, etc. due
        > to poor time management. We need to stick to the syllabus and
        > limit the digressions. *Note from Patrick: kind of feel like it's fine to not get to everything. Better they understand what you cover, in my opinion.*

- Windows users get a GUI GitHub login prompt when trying to do a
        > git push to a remote, rather than being prompted on the
        > terminal

- One student confused the `!` in the GitHub welcome email as part
        > of their username, which caused git bash to freak out with a
        > broken pipe error when they tried to push to Github. Worth
        > noting in case anyone else has this issue.

### LaTeX

- Out of the entire class, only one student uses LaTeX to write
        > her papers and was lamenting how her colleagues waste a lot of
        > time trying to center figures in Word, etc. **Should we offer
        > a LaTeX workshop?** Does somebody already? Did you know you
        > can export a Jupyter notebook as LaTex? And, of course,
        > matplotlib and R can export figures in any number of vector formats (svg, eps, etc.) that render nicely with TeX. She uses [*https://www.overleaf.com*](https://www.overleaf.com/) but apps like TeXShop are pretty nice and fit the "run it all on your laptop" model.

