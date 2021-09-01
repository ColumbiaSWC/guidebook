# Curriculum Notes: Unix

## Alan Croswell's notes on the Software Carpentry curriculum

- man pages missing from git-bash on windows. Fix: "google man ls"
-   macos `ls \--help` doesn't work (it's too BSDish to have the
        `--help` switch)
- `sort -n lengths.txt` gives the same result without `-n`
        because wc's output is left-padded and spaces collate
        differently on MacOS vs. Linux. See
        [*\#810*](https://github.com/swcarpentry/shell-novice/issues/810).
        LANG=C vs. LANG=en\_US.UTF8. A better example would use
        left-aligned numbers.

- Tab completion doesn't appear to work in git bash on Windows

## Monica Thieu's notes

In my experience, going at a pace that fully novice learners report to be comfortable, modules tend to take about _twice as long_ as their estimated duration listed on the Carpentries lesson plan.

### Recommended lesson order

These are listed for a half-day (3 hr) session.

1. Introducing the Shell
2. Navigating Files and Directories
        1. Introduce directory structure, pwd, ls
        2. Introduce paths, cd
        3. Introduce args, flags, and shell cmd syntax, ls -F etc
3. Working with Files and Directories
        1. mkdir
        2. (QUICKLY!) Create files for the purpose of moving them around
        3. mv
                1. rename file
                2. move file
                3. move multiple files to same destination
        4. cp
                1. copy single file
                2. copy directory
        5. rm
        6. cp, mv, and rm with wildcards
4. Finding Things (if you get there)

I have generally only gotten through the first three of these lessons, but I try to be thorough with those. Don't sweat getting through "a lot" of content! It's most important that learners can fully execute the objectives from the early lessons that are the core prerequisites for subsequent lessons outside of shell. Learners will need to be able to parse and follow file paths, and call some apps through command line. That's really about it for most people. Most learners will eventually use Python or R for much of what is taught in the greater Unix lesson anyway, and learners who do need more intense shell functionality can learn it elsewhere.

**Read the lesson plans before you teach, and sketch out what you will cover and in what order.**

**Do not read directly from the lesson plans when teaching.** In this lesson, you will find that you need to circle back and re-explain various concepts based on learner progress, so be prepared to depart from and return to the lesson plans.

### Recommended modifications

#### Introducing the Shell

I skip the lesson framing featuring Nelle Nemo, a fictional marine biologist. The framing gets useful in much later lesson modules where students are doing more hardcore file manipulation and actually executing scripts, but I have never gotten that far when I've taught this lesson. Accordingly, I skip the introduction of the Nelle framing because it never becomes relevant to learners.

#### Navigating Files and Directories

The lesson generally does this already, but I try to save any mention of flags until people feel comfortable `cd`-ing and `ls`-ing around. I also skip the exercises where learners are asked to guess the behavior of new flags, in lieu of demonstrating reading the relevant man pages.

#### Working with Files and Directories

I know this is a hot take, but **I prefer not to teach an inline text editor.** Learners who will go on to use text editors like Nano (as demonstrated by the SC lesson plan), Vim, or Emacs will be able to learn them elsewhere. The vast majority of learners will be using terminals on a computer where they simultaneously have access to every other GUI app on their machine, including GUI text editors like Notepad (Windows) or TextEdit (Mac). The SC lesson uses Nano exclusively to demonstrate opening a text editor from the command line, creating files, and editing pre-existing files. In my opinion, Nano (or any inline text editor) is not uniquely useful enough to the lesson to justify its intimidating appearance to novices. Thus, I sub it out.

Windows: Learners can open a Notepad window by calling `notepad` in Git Bash
Mac: Learners can open a TextEdit window by calling `open -e` in the terminal
Linux (including Chromebook): Learners should be able to open a gedit window by calling `gedit` in the terminal, but this may not work on some systems since gedit is not installed on every Linux distribution by default.
