# Analytics Engineering Library


## Sections
- [To Read, To Process](#to-read-to-process)
- [SQL](#sql)
- [Data Modeling](#data-modeling)
- [Version Control](#version-control)
- [Style Guides](#style-guides)
- [Markdown](#markdown)
- [Visual Studio Code](#visual-studio-code)
- [Blogs, etc.](#blogs-etc)
- [AE Experts](#ae-experts)


---

## To Read, To Process
- [Learning SQL 201: Optimizing Queries, Regardless of Platform](https://towardsdatascience.com/learning-sql-201-optimizing-queries-regardless-of-platform-918a3af9c8b1)
- [SQL: Don't Do This](https://wiki.postgresql.org/wiki/Don%27t_Do_This)
- [Analyzing 89 Responses to a SQL Screener Question for a Senior Data Analyst Position](https://mattmazur.com/2018/11/12/analyzing-89-responses-to-a-sql-screener-question-for-a-senior-data-analyst-position/)
- [An Opinionated Introduction to Data Warehouse Query Strategies, Part 1 of N](https://calogica.com/sql/2018/06/22/data-warehouse-query-strategies.html)
- [SQL Window Functions to Pass a Data Analytics Interview (Opinionated SQL Series Part 2/N)](https://calogica.com/sql/2018/07/01/sql-functions-for-data-analyst-interviews.html)
- [SQL Tutorial](https://www.geeksforgeeks.org/sql-tutorial/)

---


## SQL

#### SQL | General

- [SQL COUNT Function Explained with Examples](https://www.databasestar.com/sql-count/)
    >*Really nice article that goes over the syntax of count() and ALL of the nuances that matter when using it*
 
    >*Key Takeaways for What Count() Does:*
        *1. COUNT(*) *– all rows, including duplicates and nulls.*
        *2. COUNT(expression) – all rows excluding null.*
        *3. COUNT(DISTINCT expression) – all rows excluding duplicates and nulls.*

    ```sql
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

- [CTEs versus Subqueries](https://www.alisa-in.tech/post/2019-10-02-ctes/)
- [The most underutilized function in SQL](https://www.getdbt.com/blog/the-most-underutilized-function-in-sql/)
    > *In this post I’m going to show you two uses for md5() that make it one of the most powerful tools in my SQL kit.*
- [The Three-Valued Logic of SQL](https://modern-sql.com/concept/three-valued-logic)
    >*SQL uses a three-valued logic: besides true and false, the result of logical expressions can also be unknown. SQL’s three valued logic is a consequence of supporting null to mark absent data. If a null value affects the result of a logical expression, the result is neither true nor false but unknown.*


#### SQL | Interviewing
- [31 SQL Questions for Data Analysts [Updated for 2022]](https://www.interviewquery.com/p/sql-questions-data-analyst)
- [How to learn SQL for data science interview (the minimize effort maximize outcome way)](https://www.youtube.com/watch?v=vaD3ZFFNwhM&ab_channel=TinaHuang)
- [SQL Sundays (YouTube)](https://www.youtube.com/playlist?list=PLVD3APpfd1tuXrXBWAntLx4tNaONro5dA)
    > *Real data science SQL interview question walk through with a FAANG data scientist.*

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


## AE Experts
- [Claire Carroll](https://clrcrl.com/)
- [Madison Schott](https://madisonmae.substack.com/)
- [Parker Tenpas](https://pdtenpas.github.io/)
