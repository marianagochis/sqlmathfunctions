# SQL - Math - Functions
## SQL queries with math and numeric functions

```sql

SELECT
name,
ROUND(weight / (CAST(height AS numeric))^2) as BMI
FROM character;

```
```sql

SELECT
  firstname,
  lastname,
  level,
  ROUND(CAST(height as numeric),2),
  FLOOR(account_balance)
FROM player
JOIN character ON player.id = character.player_id
WHERE player.id  IN (1,5);

```
```sql

SELECT
name,
((strength + CAST(hp/4.0 as numeric)) * ABS(stat_modifier)) as damage
FROM character
WHERE level >= 3

```
