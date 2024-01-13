1. What query would you run to get all the countries that speak Slovene? Your query should return the name of the country, language and language percentage. Your query should arrange the result by language percentage in descending order.
SELECT countries.name, languages.language, languages.percentage FROM countries JOIN languages ON countries.id = languages.country_id WHERE languages.language = "Slovene" ORDER BY languages.percentage DESC;

2. What query would you run to display the total number of cities for each country? Your query should return the name of the country and the total number of cities. Your query should arrange the result by the number of cities in descending order
SELECT countries.name AS name, COUNT(cities.id) AS cities FROM countries JOIN cities ON countries.id = cities.country_id GROUP BY countries.name ORDER BY cities DESC;
