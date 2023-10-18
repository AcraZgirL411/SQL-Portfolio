# SQL-Portfolio
Hi! Welcome to my portfolio; this is where I'll keep track of the lessons I learn! I'm really enjoying this line of work and can't wait to keep learning.
# CASE
The CASE statement goes through one or more conditions and returns a value as soon as a coniditon is met. <br/>
SELECT <br/>
        name, number_grade <br/>
        CASE <br/>
               WHEN number_grade >90 THEN "A" <br/>
               WHEN number_grade >80 THEN "B" <br/>
               WHEN number_grade >70 THEN "C" <br/>
               ELSE "F" <br/>
               END as "letter_grade" <br/>
FROM student_grades <br/>
GROUP BY "letter_grade";

# DISTINCT
SELECT DISTINCT fuel_type <br/>
FROM cars.car_info; <br/>
SELECT DISTINCT name <br/>
FROM playlist <br/>
ORDER BY playlist_id <br/>

# SUM
SELECT author, SUM(words) AS total_words <br/>
FROM books <br/>
GROUP BY author <br/>
HAVING total_words >1000000;

# AVG
SELECT author, AVG(words) AS avg_words <br/>
FROM books <br/> 
GROUP BY author <br/> 
HAVING avg_words >150000;

# LIKE
SELECT title FROM songs WHERE artist = "Queen"; <br/>
SELECT name FROM artists WHERE genre = "Pop"; <br/>
SELECT title FROM songs WHERE artist <br/> 
IN (SELECT name FROM artists WHERE genre LIKE "%Pop%");

# AND/OR
SELECT title <br/> 
FROM songs <br/>
WHERE released >1990 OR mood is "epic"; <br/>
SELECT title <br/>
FROM songs <br/>
WHERE released >1990 AND mood is "epic" AND duration < 240;
 
