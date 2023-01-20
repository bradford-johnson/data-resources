# data-resources
## Community Stuff
- [30 Day Map Challenge](https://30daymapchallenge.com/)
- [R For DS](https://www.rfordatasci.com/)
- [TidyTuesday](https://github.com/rfordatascience/tidytuesday)
- [Learn via Kaggle](https://www.kaggle.com/learn)
## Resources
### `R`
#### Youtube Channels
- [ggnot2](https://www.youtube.com/@ggnot2)
- [Posit](https://www.youtube.com/@PositPBC)
- [R Programming 101](https://www.youtube.com/@RProgramming101)
- [Business Science](https://www.youtube.com/@BusinessScience)
- [DataSlice](https://www.youtube.com/@dataslice)
#### Websites
- [rweekly.org](https://rweekly.org/)
- [EasyStats](https://easystats.github.io/easystats/)
- [tidyverse.org/blog](https://www.tidyverse.org/blog/)
- [programming with dplyr](https://dplyr.tidyverse.org/articles/programming.html)
- [programming with tidyr](https://tidyr.tidyverse.org/articles/programming.html)
- [programming with ggplot2](https://ggplot2-book.org/programming.html)
    - [ggplot2 book](https://ggplot2-book.org/index.html)
    - [fundamentals of data visualizing](https://clauswilke.com/dataviz/index.html)
- [forcats factors](https://blog.albertkuo.me/post/2022-01-04-reordering-geom-col-and-geom-bar-by-count-or-value/)
- [Making shareable documents with Quarto](https://openscapes.github.io/quarto-website-tutorial/)
- [mockup blog](https://themockup.blog/)
- [geniusr](https://ewenme.github.io/geniusr/)
- [Wannabe Rstats-fu](https://yutani.rbind.io/)
- [Hands-On Programming with R](https://jjallaire.github.io/hopr/)
- [R Packages](https://r-pkgs.org/)
- [mlr3book](https://mlr3book.mlr-org.com/)
- [Telling Stories with Data](https://tellingstorieswithdata.com/)
- [STA 210: Regression Analysis](https://sta210-s22.github.io/website/)
- [A Quarto tip a day](https://mine-cetinkaya-rundel.github.io/quarto-tip-a-day/)
- [A Quarto Page Layout Example HTML](https://quarto-dev.github.io/quarto-gallery/page-layout/tufte.html)
- [A Quarto Page Layout Example PDF](https://quarto-dev.github.io/quarto-gallery/page-layout/tufte.pdf)
- [Advanced-R-exercises](https://bookdown.org/IndrajeetPatil/Advanced-R-exercises/)
- [New R Pipe](https://www.infoworld.com/article/3621369/use-the-new-r-pipe-built-into-r-41.html)

### `SQL`
- [SQL Style Guide](https://www.sqlstyle.guide/)
- [PostgreSQL Courses](https://www.enterprisedb.com/training/free-postgres-training)

### `Tableau`
- [Free Training Videos](https://www.tableau.com/learn/training/20224)

## R Workflows - [Link](https://r4ds.hadley.nz/workflow-scripts.html#summary)
- Create one RStudio project for each data analysis project.
- Save your scripts (with informative names) in the project, edit them, run them in bits or as a whole. Restart R frequently to make sure you’ve captured everything in your scripts.
- Only ever use relative paths, not absolute paths.

## R Studio Config - [Link](https://r4ds.hadley.nz/workflow-scripts.html)
<img src = "https://r4ds.hadley.nz/diagrams/rstudio/clean-slate.png" width = "600px">

## Saving and Naming - [Link](https://r4ds.hadley.nz/workflow-scripts.html#saving-and-naming)
- File names should be machine readable: avoid spaces, symbols, and special characters. Don’t rely on case sensitivity to distinguish files.
- File names should be human readable: use file names to describe what’s in the file.
- File names should play well with default ordering: start file names with numbers so that alphabetical sorting puts them in the order they get used.

| bad names | good names |
|---|---|
| alternative model.R | 01-load-data.R |
| code for exploratory analysis.r | 02-exploratory-analysis.R |
| finalreport.qmd | 03-model-approach-1.R |
| FinalReport.qmd | 04-model-approach-2.R |
| fig 1.png | fig-01.png |
| Figure_02.png | fig-02.png |
| model_first_try.R | report-2022-03-20.qmd |
| run-first.r | report-2022-04-02.qmd |
| temp.txt | report-draft-notes.txt |

## Quarto Workflow - [Link](https://r4ds.hadley.nz/quarto-workflow.html)
- Quarto is also important because it so tightly integrates prose and code. This makes it a great analysis notebook because it lets you develop code and record your thoughts. An analysis notebook shares many of the same goals as a classic lab notebook in the physical sciences. It:
- Records what you did and why you did it. Regardless of how great your memory is, if you don’t record what you do, there will come a time when you have forgotten important details. Write them down so you don’t forget!
- Supports rigorous thinking. You are more likely to come up with a strong analysis if you record your thoughts as you go, and continue to reflect on them. This also saves you time when you eventually write up your analysis to share with others.
- Helps others understand your work. It is rare to do data analysis by yourself, and you’ll often be working as part of a team. A lab notebook helps you share not only what you’ve done, but why you did it with your colleagues or lab mates.
- Much of the good advice about using lab notebooks effectively can also be translated to analysis notebooks. We’ve drawn on our own experiences and Colin Purrington’s advice on lab notebooks (https://colinpurrington.com/tips/lab-notebooks) to come up with the following tips:
- Ensure each notebook has a descriptive title, an evocative file name, and a first paragraph that briefly describes the aims of the analysis.
- Use the YAML header date field to record the date you started working on the notebook:
- date: 2016-08-23
- Use ISO8601 YYYY-MM-DD format so that’s there no ambiguity. Use it even if you don’t normally write dates that way!
- If you spend a lot of time on an analysis idea and it turns out to be a dead end, don’t delete it! Write up a brief note about why it failed and leave it in the notebook. That will help you avoid going down the same dead end when you come back to the analysis in the future.
- Generally, you’re better off doing data entry outside of R. But if you do need to record a small snippet of data, clearly lay it out using tibble::tribble().
- If you discover an error in a data file, never modify it directly, but instead write code to correct the value. Explain why you made the fix.
- Before you finish for the day, make sure you can render the notebook. If you’re using caching, make sure to clear the caches. That will let you fix any problems while the code is still fresh in your mind.
- If you want your code to be reproducible in the long-run (i.e. so you can come back to run it next month or next year), you’ll need to track the versions of the packages that your code uses. A rigorous approach is to use renv, https://rstudio.github.io/renv/index.html, which stores packages in your project directory. A quick and dirty hack is to include a chunk that runs sessionInfo() — that won’t let you easily recreate your packages as they are today, but at least you’ll know what they were.
- You are going to create many, many, many analysis notebooks over the course of your career. How are you going to organize them so you can find them again in the future? We recommend storing them in individual projects, and coming up with a good naming scheme.
