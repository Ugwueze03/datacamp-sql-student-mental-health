# Analyzing Student's Mental Health with SQL
**DataCamp Project**: Day 4 of 100 Days of Data Analysis Journey
**Goal**: Analyze mental health diagnostic scores of international students by length of stay.
**Skills Used**: SQL, COUNT, ROUND, AVG, ORDER BY, GROUP BY, filtering.
**Key Query**:
```sql
SELECT 
  stay,
  COUNT(inter_dom) AS count_int,
  ROUND(AVG(todep), 2) AS average_phq,
  ROUND(AVG(tosc), 2) AS average_scs,
  ROUND(AVG(toas), 2) AS average_as
FROM students
WHERE inter_dom = 'Inter'
GROUP BY stay
ORDER BY stay DESC;
```
**Key Insight**: 
1-Students who stayed for a longer period (8-10 years) show higher depression scores, which indicates that the depression score is proportional to the length of stay. Though these groups(8-10 years) contain very few students, so conclusion must be made cautiously.
2-Most international students are relatively new, which indicates that the dataset is mostly focused on international students who have stayed for 1-3 years.
3-Students who stayed longer generally reported lower connectedness.
**Tools**: PostgreSQL, DataCamp Workspace
