## Schemas

`Process`

1. Hand out tasks (`MECE`)
(So what, why so? `Target`? Metric? `Indications`?)

2. Setting Purpose / terminate goals

3. Searching for data
- monopoly data
- by joining multipoly data

**: setting condition(filtering) / extraction / transformation / summarization(calculation .etc)**

- validation
- feedback / utilization

SQL query is used for the process within `exploration` and `validation`.

**Checking the stored data schema does matter**


## Before writing SQL query lines

Consider:

-How the data is arranged / organized

-What kind of data is stored

-What is the meaning of individual columns

**Heading to actually extracting the data, should know how it is organized and what we should look for.**

## How to know how it is organized?

to look for `ERD(Entity Relationship Diagram)`

Explore table, column, the PK column to join/merge, meaning of each column values, number of rows

> Make definition about frequently used tables

**Eg Data Schema:**

1. Database used for service
- user table
- delivery table
- order table
- product table

2. App/Web Log data(process)

3. official data, third-party data
- weather
- advertising data

[edu-url](https://www.inflearn.com/course/lecture?courseSlug=%EC%B4%88%EB%B3%B4%EC%9E%90%EB%A5%BC-%EC%9C%84%ED%95%9C-%EB%B9%85%EC%BF%BC%EB%A6%AC-sql-%EC%9E%85%EB%AC%B8&unitId=209828&tab=curriculum)
2-1, 2-2