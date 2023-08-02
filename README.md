# SQL-Project---DVD-Rental-database

1. prepare the data needed (title & description) to run a promotion for the store's Italian & French language films from 2005.
     SELECT title, description
      FROM film AS f
      INNER JOIN language AS l
      ON f.language_id = l.language_id
      WHERE name IN ('Italian' , 'French')
      AND release_year = 2005 ;
2. Prepare a list of top paying active customers.
     SELECT first_name, last_name, amount
      FROM payment AS p
      INNER JOIN customer AS c
      ON p.customer_id = c.customer_id
      WHERE active = 1
      ORDER BY amount DESC;
