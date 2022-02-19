## Problem: we have a working app with SQL database on our backend side. At one point, we want to let users see the detailed statistics about the domain of the app. That statistics contains n aggregations, sums, counts, etc. Question: how would you handle that?
Expected answer: SQL Views
Inexperienced answer: handle that in business logic

## Problem: We are storing n million rows to one table every day. At the end of a week we want to form some statistics for the previous week. Our query is taking ~20-30 secs. Question: How would you optimize this, reducing the cost of the query?

Expected answer: There is really no expected answer here. This questions is to check the candidates knowledge, understanding and depth of sql. A high tier answer would be something like:
I'll index the createdAt column in the table
then I'll query and sort by createdAt desc , selecting only rows from previous 7 days
create a material view for the previous query
index the createdAt column in newly created view for even more speed