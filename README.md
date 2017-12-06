# sqlmathfunctions
--Example of SQL queries with math and numeric functions
SELECT
	name,
    round( weight / (CAST(height AS numeric))^2) AS BMI
FROM character;

SELECT
   firstname,
    lastname,
    level,
    round(cast(height as numeric),2),
    floor(account_balance)
FROM player
JOIN character ON player.id = character.player_id
WHERE player.id  IN (1,5);

SELECT
	name,
	((strength + cast(hp/4.0 as numeric)) * abs(stat_modifier))AS damage
FROM character
where level >= 3
