# Analytics Engineering Library


## Sections
- [To Read, To Process](#to-read-to-process)
- [Style Guides](#style-guides)
- [Analytics Engineering](#analytics-engineering)
- [Command Line Interface (CLI)](#command-line-interface-cli)
- [dbt](#dbt)
- [SQL](#sql)
- [Data Modeling](#data-modeling)
- [Version Control](#version-control)
- [Markdown](#markdown)
- [Visual Studio Code](#visual-studio-code)
- [Blogs, etc.](#blogs-etc)
- [AE Experts](#ae-experts)
- [Non-AE Aritcles](#non-ae)

<br>

---

## To Read, To Process (section now in google doc)
- [What is Operational Analytics (and how is it changing how we work with data)?](https://www.getcensus.com/blog/what-is-operational-analytics)
- [SQL: Don't Do This](https://wiki.postgresql.org/wiki/Don%27t_Do_This)
- [An Opinionated Introduction to Data Warehouse Query Strategies, Part 1 of N](https://calogica.com/sql/2018/06/22/data-warehouse-query-strategies.html)
- [SQL Window Functions to Pass a Data Analytics Interview (Opinionated SQL Series Part 2/N)](https://calogica.com/sql/2018/07/01/sql-functions-for-data-analyst-interviews.html)
- [SQL Tutorial](https://www.geeksforgeeks.org/sql-tutorial/)

---

## Style Guides

- [3 things to include in any SQL style guide](https://www.kahandatasolutions.com/blog/3%20things%20to%20include%20in%20any%20style%20guide)
- [Gitlab SQL Style Guide](https://about.gitlab.com/handbook/business-technology/data-team/platform/sql-style-guide/)
- [Mazur's SQL Style Guide](https://github.com/mattm/sql-style-guide)
- [Kickstarter SQL Style Guide](https://gist.github.com/fredbenenson/7bb92718e19138c20591)
- [dbt Style Guide](https://github.com/dbt-labs/corp/blob/main/dbt_style_guide.md)


<br>

## Analytics Engineering (AE)

#### AE | What do AEs do?
>Some points from the co:rise AE with dbt Course:
>- *"While Data Analysts spend the majority of their time analyzing data, Analytics Engineers spend their time **transforming, testing, deploying, and documenting data."***
>- *"AEs review code like software engineers and learn **coding best-practices like making their code readable and modular"***

#### AE | General
- [Aspiring Analytics Engineers, Start Here](https://madisonmae.substack.com/p/aspiring-analytics-engineers-start)

- [What Companies REALLY Want in an Analytics Engineer](https://medium.com/geekculture/what-companies-really-want-in-an-analytics-engineer-1ac03ff4494a)
    >*author: madison schott. excellent article outlining where AEs should be spending their time when learning where to focus efforts (skills/tools) and how to land jobs and how to be effective as an AE.*

#### AE | Books Related to AE

- [The Analytics Setup Guidebook (currently reading)](https://www.holistics.io/books/setup-analytics/)
    >*the awesome people at Holistics put together a **free** 187 page guide designed to: "Restructure your knowledge of the complex data analytics landscape, and learn how to build scalable analytics & BI stacks in the modern cloud era."*

- [The Data Warehouse Toolkit, 3rd Edition](https://www.kimballgroup.com/data-warehouse-business-intelligence-resources/books/data-warehouse-dw-toolkit/)
    >*the definitive guide to dimensional modeling*

#### AE | Blogs
- [Learn Analytics Enginneering](https://madisonmae.substack.com/archive?sort=new)

- [dbt Developer Blog](https://docs.getdbt.com/blog)
    >*Technical tutorials from the dbt Community.*

#### AE Experts
- [Claire Carroll](https://clrcrl.com/)
- [Dave Connors](https://docs.getdbt.com/author/dave_connors)
    >*dave is interesting b/c he has worked in the consulting wing of dbt labs where he and his colleagues work on an unusually high number of dbt-projects. he has great content on understanding what a 'good' and 'mature' dbt project looks like and each of the milestones to hit along the way.*
- [Madison Schott](https://madisonmae.substack.com/)
- [Parker Tenpas](https://pdtenpas.github.io/)


<br>

## Command Line Interface (CLI)

- [Basics of BASH for Beginners](https://towardsdatascience.com/basics-of-bash-for-beginners-92e53a4c117a)
    >*suggested reading in the AE w/dbt course and a great overview to "learn about some of the most useful BASH commands and the utility they offer".*


<br>

## dbt


#### dbt | General

- [Never used dbt? Here’s how it can change your data game](https://www.getcensus.com/blog/never-used-dbt)
     >- ***great explanation:** dbt is a data transformation tool that leverages the power of SQL and Jinja to write modular data models within your data warehouse. It reads from the data within your data warehouse and writes to it without ever leaving, allowing you to test and document your code and promoting proper code maintenance along the way.*
    >- *dbt is an open-source tool that is completely free to use*
    >- *implementing dbt is nearly risk-free since it lives entirely in your data warehouse. It reads from your data warehouse and writes to it. In fact, dbt puts the T in ETL/ELT.*

#### dbt | Getting Help

- [dbt discourse](https://discourse.getdbt.com/)
    >**dbt hosted site for getting support with all things dbt (help, show/tell, discussion, etc.)*

#### dbt | Best Practices

- [Best practice guides](https://docs.getdbt.com/guides/best-practices)
    >*Learn how dbt Labs approaches building projects through our current viewpoints on structure, style, and setup.*


#### dbt | dbt Project Setup

- [Overview of building a dbt project](https://docs.getdbt.com/docs/building-a-dbt-project/projects)
    >*root of dbt-docs that outlines how to get up and running with dbt Cloud and dbt CLI*

- [Getting started with dbt Core](https://docs.getdbt.com/guides/getting-started/learning-more/getting-started-dbt-core)
    >*dbt-doc(s) with really awesome walk through of setting up a dbt-project using dbt CLI.*
    > - *very thorough documentation/tutorial on getting a dbt-project up and running start/finish*
    > - *has link(s) to a really thorough example of seting up and loading data from Google BigQuery. also, has examples for databricks, redshift, snowflake*
    > - has awesome FAQs sections with loads of pro-tips

- [Configuring your profile.yml](https://docs.getdbt.com/dbt-cli/configure-your-profile)
    >*awesome dbt-doc(s) w/ALL the details needed to properly setup the **profile.yml** file. includes a reference link to a doc w/ALL warehouses that dbt can connect to and how to setup profile.yml files for each.*

- [How to build a mature dbt project from scratch](https://www.getdbt.com/coalesce-2021/how-to-build-a-mature-dbt-project-from-scratch/)
    >*dave connors from dbt gives a presentation on how to build a dbt-project from the ground up.*


#### dbt | dbt certification

- [dbt Analytics Engineering Certification Exam](https://www.getdbt.com/certifications/analytics-engineer-certification-exam/)
    >*page to register for exam. very useful page b/c it has exam prep material: a) what's covered section; b) link to sample-questions; & c) link to a study-guide*



<br>

## SQL

#### SQL | General

- [CTEs versus Subqueries](https://www.alisa-in.tech/post/2019-10-02-ctes/)
- [The most underutilized function in SQL](https://www.getdbt.com/blog/the-most-underutilized-function-in-sql/)
    > *In this post I’m going to show you two uses for md5() that make it one of the most powerful tools in my SQL kit.*
- [The Three-Valued Logic of SQL](https://modern-sql.com/concept/three-valued-logic)
    >*SQL uses a three-valued logic: besides true and false, the result of logical expressions can also be unknown. SQL’s three valued logic is a consequence of supporting null to mark absent data. If a null value affects the result of a logical expression, the result is neither true nor false but unknown.*

- [SQL Fiddle](http://sqlfiddle.com/about.html)
    >*A tool for easy online testing and sharing of database problems and their solutions.*


#### SQL | Filtering Data

- [HAVING vs. WHERE in SQL: What You Should Know](https://learnsql.com/blog/sql-having-vs-where/)
    >*"In simple words, the WHERE and HAVING clauses **act as filters;** they remove records or data that don’t meet certain criteria from the final result of a query. However, they are **applied to different sets of data.** That’s the important point to understand about WHERE vs. HAVING: **WHERE filters at the record level,** while **HAVING filters at the "group of records" level."*** 🔥

- [What is the difference between HAVING and WHERE clause?](https://afteracademy.com/blog/what-is-the-difference-between-having-and-where-clause)
    >*Not the best article BUT I do like this clarifying statement: "If **GROUP BY** is used then it is **executed after the WHERE clause** is executed in the query. It means it selects the rows before grouping is done or aggregate calculations are performed. That's why, the WHERE clause is also called **Pre-filter.** But, **GROUP BY is executed before the execution of the HAVING clause.** It means it selects the rows after aggregate calculations are performed. That's why, the HAVING clause is also called as **Post-filter**."*


#### SQL | Assembling Data (Join/Union/Except/Etc.)

- [The problem of SQL fanouts](https://community.looker.com/technical-tips-tricks-1021/the-problem-of-sql-fanouts-30232)
    >*fanouts happen when joining tables having a one-to-many relationship; the primary table (left) is joined to the secondary table (right) and the result ends up having more rows than the left table began with.* this situation can cause errors when applying aggregate functions afterwards.  **three things to note:**
    > - **"no-fanout (one-to-one OR many-to-one):** you can trust aggregate functions on your primary table but not necessarily on your joined tables"
    > - **"fanout (one-to-many):** you cannot necessarily trust aggregate functions on either your primary table or your joined tables"
    > - **"help avoid fanouts (protip):** begin your joins with the most granular table (many-to-one)"

- [SQL Joins Using WHERE or ON](https://mode.com/sql-tutorial/sql-joins-where-vs-on/)
    >*Has a good illustration of filtering data prior to joining tables.*

- [Difference between WHERE and ON in SQL](https://dataschool.com/how-to-teach-people-sql/difference-between-where-and-on-in-sql/)
    >*Makes the case that the WHERE clause and the ON clause should ONLY be used for there intended purposes, to filter and to join data, respectively. The author says this in the intro: "ON should be used to define the join condition and WHERE should be used to filter the data. I used the word should because this is not a hard rule. The splitting of these purposes with their respective clauses makes the query the most readable". **100% Agree!!! Prioritizing readability is key 🔑***

- [An Introduction to Using SQL Aggregate Functions with JOINs](https://learnsql.com/blog/introduction-using-aggregate-functions-joins/)
    >*Key Insight(s): using conditions in the JOIN predicate (after the ON) is not the same as filtering in the WHERE (or using HAVING). These can create subtle (or not so subtle) differences in your summarized data, which could result in hard-to-spot errors.*
        - *WHERE conditions are applied **after** the JOIN*
        - *conditions (for filtering) applied in the JOIN predicate are 
        applied **before** the join*




#### SQL | Grouping Data

- [Write better SQL: In defense of group by 1](https://www.getdbt.com/blog/write-better-sql-a-defense-of-group-by-1/)


#### SQL | General Functions

- [SQL COUNT Function Explained with Examples](https://www.databasestar.com/sql-count/)
    >*Really nice article that goes over the syntax of count() and ALL of the nuances that matter when using it*

    ```sql
    -- what does count() do?
    COUNT(*)                   -- counts ALL rows, including duplicates and nulls
    COUNT(expression)          -- counts ALL rows excluding nulls
    COUNT(DISTINCT expression) -- counts ALL rows excluding duplicates and nulls
    
    -- basic syntax
    COUNT ( [ * | [ DISTINCT | ALL ] expression) [ over (analytic_clause) ]

    -- variations for how to call count()
    COUNT(*)
    COUNT(DISTINCT expression)
    COUNT(ALL expression)
    COUNT(*) OVER (analytic_clause)
    COUNT(DISTINCT expression) OVER (analytic_clause)
    COUNT(ALL expression) OVER (analytic_clause)
    ```

- [What is the Difference Between COUNT(*), COUNT(1), COUNT(column name), and COUNT(DISTINCT column name)?](https://learnsql.com/blog/difference-between-count-distinct/)
    >*Have you noticed there are different variations of the SQL COUNT() function? This article explains the various arguments and their uses.*

- [SQL Window Functions vs. SQL Aggregate Functions: Similarities and Differences](https://learnsql.com/blog/window-functions-vs-aggregate-functions/)


#### SQL | Window Functions

- [Let's Learn SQL Window Functions](https://madisonmae.substack.com/p/lets-learn-sql-window-functions)
    >*nice summary of window function's by Madison Mae (+with examples)*


- [[Video] Lead and Lag functions in SQL Server 2012](https://www.youtube.com/watch?v=l_Zn5sdkamM&ab_channel=kudvenkat)
    >*excellent overview of these two functions (should generalize to other SQL dialects)*
    > - **lead** function used to access subsequent row of data along w/current row of data.
    > - **lag** function used to access previous row of data along w/current row of data.
    > - **order by** clase is required.
    > - **partition by** clause is optional
    > - **syntax:** LEAD/LAG(col-name, offset, default-value) OVER(ORDER BY col1, col2, ...)

    

#### SQL | Training

- [learnsql.com | Learn & Practice SQL](https://learnsql.com/)
    >*one of my favorite online platforms for learning/practicing SQL*
- [learnsql.com | SQL Joins](https://learnsql.com/course/joins)
    >*Review and deepen your knowledge of SQL JOINs with 93 exercises. Practice common and less common ways of getting data from multiple tables.*
- [co:rise | Intro to SQL](https://corise.com/course/intro-to-sql)
    >*This course provides an introduction to SQL, a programming language that will unleash your ability to explore data. We'll cover all the fundamentals of SQL, and you'll leave knowing how to issue SQL queries and interact with databases, as well as how to translate English queries to SQL correctly and quickly. We'll approach SQL in a hands-on manner with real-life examples and we'll build complexity in our SQL queries week over week.*



#### SQL | Interviewing
- [Top Skills to Ace Every SQL Interview Question](https://medium.com/towards-data-science/top-skills-to-ace-every-sql-interview-question-33356b08845a)
    >***Madison Schott:** *"Once you nail a few key concepts you can pretty much answer any question, with lots of practice that is. Start with the basics for each of these concepts and work your way up to more difficult problems."*
        1) Master Joins;
        2) Master Aggregate Functions;
        3) Master Subqueries.
- [How to learn SQL for data science interview (the minimize effort maximize outcome way)](https://www.youtube.com/watch?v=vaD3ZFFNwhM&ab_channel=TinaHuang)
    >*scientifically-backed study plan to learn SQL most efficiently with the least amount of time and effort*
- [Analyzing 89 Responses to a SQL Screener Question for a Senior Data Analyst Position](https://mattmazur.com/2018/11/12/analyzing-89-responses-to-a-sql-screener-question-for-a-senior-data-analyst-position/comment-page-1/?unapproved=55959&moderation-hash=65cb4dbf0ddf1d2f87c78641dbcc59f7#comment-55959)
    >*Matt Mazur's analysis of candidate responses to a SQL Screener Question that was designed to weed out weaker candidates*
- [31 SQL Questions for Data Analysts [Updated for 2022]](https://www.interviewquery.com/p/sql-questions-data-analyst)
- [How to learn SQL for data science interview (the minimize effort maximize outcome way)](https://www.youtube.com/watch?v=vaD3ZFFNwhM&ab_channel=TinaHuang)
- [Three Tricky Analytics Interview Questions with Andrew](https://www.youtube.com/watch?v=uLCFCzVLi4Q&ab_channel=DataScienceJay)

   >*We tackle three analytics interview questions by solving them with SQL. Each one is progressively harder and Andrew explains his methodology towards solving each question!*


- [SQL Sundays (YouTube)](https://www.youtube.com/playlist?list=PLVD3APpfd1tuXrXBWAntLx4tNaONro5dA)
    > *9 Mock Interview videos with 9 different SQL problems*

- [Frequently Asked Questions About SQL](https://learnsql.com/blog/frequently-asked-questions-about-sql/)
    >*Not my favorite article BUT has a solid list of topics AND also some great links to other resources. Keeping in the library for now...*

#### SQL | History
- [Relational Database History, Edgar F. Codd](https://www.ibm.com/ibm/history/ibm100/us/en/icons/reldb/)


#### SQL | Experts
- [Tihomir Babic, Technical Writer for LearnSQL.com](https://learnsql.com/authors/tihomir-babic/)


#### SQL | Never Know, Might Need It

- [SQL Delete Join](https://www.educba.com/sql-delete-join/?source=leftnav)
    >*an advanced method for using the delete command came up in a leetcode problem. this article illustrates the 'sql-delete-join' - may not need this in AE but thought it was interesting so hanging on to it for now*


---


## Data Modeling

#### Cleaning / Tidying / Munging / Wrangling
- [Tidy Data, Hadley Wickham](https://cran.r-project.org/web/packages/tidyr/vignettes/tidy-data.html) 
    > *The principles of tidy data provide a standard way to organize data values within a dataset.*
- [The Quartz guide to bad data](https://github.com/Quartz/bad-data-guide)
    > *An exhaustive reference to problems seen in real-world data along with suggestions on how to resolve them.*

#### Slowly Changing Dimensions
- [Slowly Changing Dimensions in Data Science](https://www.fivetran.com/blog/slowly-changing-dimensions-in-data-science)


---


## Version Control

#### Git
- [Introduction to Git](https://www.datacamp.com/courses/introduction-to-git)
    >*Course recommended by Madison Schott*
- [Git Immersion](https://gitimmersion.com/index.html)
    > *A guided tour that walks through the fundamentals of Git, inspired by the premise that to know a thing is to do it.*
- [How to Write a Git Commit Message](https://cbea.ms/git-commit/)
    > *Commit messages matter. Here's how to write them well.*
- [Learn git concepts, not commands](https://dev.to/unseenwizzard/learn-git-concepts-not-commands-4gjc)
    > *An interactive git tutorial meant to teach you how git works, not just which commands to execute.*
- [Flight rules for Git](https://github.com/k88hudson/git-flight-rules)
    > *A guide for astronauts (now, programmers using Git) about what to do when things go wrong.*


<br>


## Markdown
- [Introduction to Markdown in Visual Studio Code (with Markdown worksheet!)](https://www.youtube.com/watch?v=pTCROLZLhDM)


## Visual Studio Code
- Shortcuts:
    - Open Preview: `CMD + K then V` (splits screen) OR `CMD + Shift + V`


## To Be Organized
- [Github: Start History Charts](https://star-history.com/#sqlfluff/sqlfluff&business-science/tidyquant&Date)


## Blogs, etc.
- [Locally Optimistic](https://locallyoptimistic.com/)
- [Modern SQL - A Lot has Changed Since SQL - 92](https://modern-sql.com/concept/three-valued-logic)
- [Kahan Data Solutions](https://www.kahandatasolutions.com/blog)



## Non-AE

- [When Subtraction Adds Value](https://hbr.org/2022/02/when-subtraction-adds-value)
    >*interesting take on how to think about subtracting work instead of adding work when involved in Decision Making and Problem Solving.*
