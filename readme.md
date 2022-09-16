# Analytics Engineering Library


## Sections
- [To Read, To Process](#to-read-to-process)
- [Analytics Engineering](#analytics-engineering)
- [SQL](#sql)
- [Data Modeling](#data-modeling)
- [Version Control](#version-control)
- [Style Guides](#style-guides)`
- [Markdown](#markdown)
- [Visual Studio Code](#visual-studio-code)
- [Blogs, etc.](#blogs-etc)
- [AE Experts](#ae-experts)
- [Non-AE Aritcles](#non-ae)

<br>

---

## To Read, To Process (section now in google doc)
- [What is Operational Analytics (and how is it changing how we work with data)?](https://www.getcensus.com/blog/what-is-operational-analytics)
- [Learning SQL 201: Optimizing Queries, Regardless of Platform](https://towardsdatascience.com/learning-sql-201-optimizing-queries-regardless-of-platform-918a3af9c8b1)
- [SQL: Don't Do This](https://wiki.postgresql.org/wiki/Don%27t_Do_This)
- [An Opinionated Introduction to Data Warehouse Query Strategies, Part 1 of N](https://calogica.com/sql/2018/06/22/data-warehouse-query-strategies.html)
- [SQL Window Functions to Pass a Data Analytics Interview (Opinionated SQL Series Part 2/N)](https://calogica.com/sql/2018/07/01/sql-functions-for-data-analyst-interviews.html)
- [SQL Tutorial](https://www.geeksforgeeks.org/sql-tutorial/)

---

## Analytics Engineering (AE)

#### AE | General
- [Aspiring Analytics Engineers, Start Here](https://madisonmae.substack.com/p/aspiring-analytics-engineers-start)

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
- [Madison Schott](https://madisonmae.substack.com/)
- [Parker Tenpas](https://pdtenpas.github.io/)



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


---

## Style Guides:
- [Gitlab SQL Style Guide](https://about.gitlab.com/handbook/business-technology/data-team/platform/sql-style-guide/)
- [Mazur's SQL Style Guide](https://github.com/mattm/sql-style-guide)
- [Kickstarter SQL Style Guide](https://gist.github.com/fredbenenson/7bb92718e19138c20591)
- [dbt Style Guide](https://github.com/dbt-labs/corp/blob/main/dbt_style_guide.md)


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



## Non-AE

- [When Subtraction Adds Value](https://hbr.org/2022/02/when-subtraction-adds-value)
    >*interesting take on how to think about subtracting work instead of adding work when involved in Decision Making and Problem Solving.*
