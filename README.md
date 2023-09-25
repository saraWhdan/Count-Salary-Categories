# 1907. Count Salary Categories
### Problem Link & Description :  [Count Salary Categories](https://leetcode.com/problems/count-salary-categories/description/?envType=study-plan-v2&envId=top-sql-50)
## Solution 
```sql
select'Low Salary' as category
,sum (case when income < 20000 then 1 else 0 end) accounts_count
from Accounts
union
 select'Average Salary' as category
,sum (case when income between  20000 and 50000 then 1 else 0 end) accounts_count
from Accounts
union 
select'High Salary' as category
,sum (case when income > 50000 then 1 else 0 end) accounts_count
from Accounts
