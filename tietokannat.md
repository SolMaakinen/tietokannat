# Tietokannat

# Yhteen tauluun kohdistuvat kyselyt:

1.
`select * from goal;`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/3c816e06e35bde5dddca210c2d98b49c047fa34d/Screenshot%202024-09-18%20114117.png)

2.
`select name, type from airport where iso_country = 'FI';`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/0e0f2c48fb1a7819e591af2ee25b761a0bd336cd/Screenshot%202024-09-18%20120901.png)

3.
`select name from airport where iso_country = 'FI' order by name asc;`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/0e0f2c48fb1a7819e591af2ee25b761a0bd336cd/Screenshot%202024-09-18%20121527.png)

4.
`select name, type from airport where iso_country = 'FI' order by type, name;`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/0e0f2c48fb1a7819e591af2ee25b761a0bd336cd/Screenshot%202024-09-18%20121902.png)

5.
`select name from country where name like 'F%';`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/0e0f2c48fb1a7819e591af2ee25b761a0bd336cd/Screenshot%202024-09-18%20122852.png)

6.
`select name from country where name like '%F%';`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/0e0f2c48fb1a7819e591af2ee25b761a0bd336cd/Screenshot%202024-09-18%20124559.png)

7.
`select location from game where screen_name = 'Vesa';`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/0e0f2c48fb1a7819e591af2ee25b761a0bd336cd/Screenshot%202024-09-18%20124754.png)

8.
`select co2_consumed from game where screen_name = 'Ilkka';`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/0e0f2c48fb1a7819e591af2ee25b761a0bd336cd/Screenshot%202024-09-18%20125031.png)

9.
`select distinct co2_budget from game;`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/0e0f2c48fb1a7819e591af2ee25b761a0bd336cd/Screenshot%202024-09-18%20125234.png)

# Where-osan liitosehto:

1.
`select country.name as "country name", airport.name as "airport name" from airport, country where airport.iso_country = country.iso_country and country.name = "Iceland";`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/18a4b96b70f56bdbcb6da8e0726b8d2653b24b83/Screenshot%202024-09-18%20134103.png)

2.
`select airport.name as "airport name" from airport, country where airport.iso_country = country.iso_country and country.name = "France" and airport.type = "large_airport";`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/18a4b96b70f56bdbcb6da8e0726b8d2653b24b83/Screenshot%202024-09-18%20134534.png)

3.
`select country.name as country_name, airport.name as airport_name from airport, country where airport.iso_country = country.iso_country and country.continent = "AN";`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/18a4b96b70f56bdbcb6da8e0726b8d2653b24b83/Screenshot%202024-09-18%20135451.png)

4.
`select elevation_ft from airport, game where location = ident and screen_name = "Heini";`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/18a4b96b70f56bdbcb6da8e0726b8d2653b24b83/Screenshot%202024-09-18%20135720.png)

5.
`select elevation_ft * 0.3048 as elevation_m from airport, game where location = ident and screen_name = "Heini";`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/18a4b96b70f56bdbcb6da8e0726b8d2653b24b83/Screenshot%202024-09-18%20140121.png)

6.
`select name from airport, game where location = ident and screen_name = "Ilkka";`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/18a4b96b70f56bdbcb6da8e0726b8d2653b24b83/Screenshot%202024-09-18%20140404.png)

7.
`select country.name from airport, game, country where location = ident and airport.iso_country = country.iso_country and screen_name = "Ilkka";`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/18a4b96b70f56bdbcb6da8e0726b8d2653b24b83/Screenshot%202024-09-18%20140709.png)

8.
`select name from goal, goal_reached, game where game.id = game_id and goal.id = goal_id and screen_name = "Heini";`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/18a4b96b70f56bdbcb6da8e0726b8d2653b24b83/Screenshot%202024-09-18%20140858.png)

9.
`select airport.name from airport, game, goal, goal_reached where ident = location and game.id = game_id and goal.id = goal_id and screen_name = "Ilkka" and goal.name = "CLOUDS";`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/18a4b96b70f56bdbcb6da8e0726b8d2653b24b83/Screenshot%202024-09-18%20141011.png)

10.
`select country.name from country, airport, game, goal, goal_reached where airport.iso_country = country.iso_country and ident = location and game.id = game_id and goal.id = goal_id and screen_name = "Ilkka" and goal.name = "CLOUDS";`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/18a4b96b70f56bdbcb6da8e0726b8d2653b24b83/Screenshot%202024-09-18%20141139.png)

# Join harjoitukset:

1.
`select country.name as "country name", airport.name as "airport name" from country inner join airport on airport.iso_country = country.iso_country where country.name = "Finland" and scheduled_service = "yes";`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/b1d26c4552f246bf21b2f9d6b7e24343c7245cb7/Screenshot%202024-09-24%20131541.png)

2.
`select screen_name, airport.name from game inner join airport on location = ident;`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/b2cf71aef023acf2b341b31d81332663ff8f8583/Screenshot%202024-09-24%20125528.png)

3.
`select screen_name, country.name from game inner join airport on location = ident inner join country on airport.iso_country = country.iso_country;`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/b2cf71aef023acf2b341b31d81332663ff8f8583/Screenshot%202024-09-24%20125851.png)

4.
`select airport.name, screen_name from airport left join game on ident = location where name like "%Hels%";`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/b2cf71aef023acf2b341b31d81332663ff8f8583/Screenshot%202024-09-24%20130427.png)

5.
`select name, screen_name from goal left join goal_reached on goal.id = goal_id  left join game on game.id = game_id;`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/b2cf71aef023acf2b341b31d81332663ff8f8583/Screenshot%202024-09-24%20131008.png)

# Sisäkysely harjoitukset:

1.
`select name from country where iso_country in( select iso_country from airport where name like "Satsuma%");`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/7109dfedbff4142312a0a34d2fee9cb84572896a/Screenshot%202024-09-24%20133954.png)

2.
`select name from airport where iso_country in(select iso_country from country where name = "Monaco");`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/7109dfedbff4142312a0a34d2fee9cb84572896a/Screenshot%202024-09-24%20134202.png)

3.
`select screen_name from game where id in (select game_id from goal_reached where goal_id in (select id from goal where name = "CLOUDS"));`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/7109dfedbff4142312a0a34d2fee9cb84572896a/Screenshot%202024-09-24%20134348.png)

4.
`select country.name from country where iso_country not in (select airport.iso_country from airport);`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/7109dfedbff4142312a0a34d2fee9cb84572896a/Screenshot%202024-09-24%20134537.png)

5.
`select name from goal where id not in (select goal.id from goal, goal_reached, game where game.id = game_id and goal.id = goal_id and screen_name = "Heini");`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/7109dfedbff4142312a0a34d2fee9cb84572896a/Screenshot%202024-09-24%20134706.png)

# Koostetieto kyselyt harjoitukset:

1.
`select max(elevation_ft) from airport;`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/8cfdd9a071a311c732bb591dcf0060ece680391a/Screenshot%202024-09-24%20135444.png)

2.
`select continent, count(*) from country group by continent;`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/8cfdd9a071a311c732bb591dcf0060ece680391a/Screenshot%202024-09-24%20135631.png)

3.
`select screen_name, count(*) from game, goal_reached where id = game_id group by screen_name;`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/8cfdd9a071a311c732bb591dcf0060ece680391a/Screenshot%202024-09-24%20135907.png)

4.
`select screen_name from game where co2_consumed in (select min(co2_consumed) from game);`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/8cfdd9a071a311c732bb591dcf0060ece680391a/Screenshot%202024-09-24%20140149.png)

5.
`select country.name, count(*) from airport, country where airport.iso_country = country.iso_country group by country.iso_country order by count(*) desc limit 50;`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/8cfdd9a071a311c732bb591dcf0060ece680391a/Screenshot%202024-09-24%20140511.png)

6.
`select country.name from airport, country where airport.iso_country = country.iso_country group by country.iso_country having count(*) > 1000;`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/8cfdd9a071a311c732bb591dcf0060ece680391a/Screenshot%202024-09-24%20140720.png)

7.
`select name from airport where elevation_ft in (select max(elevation_ft) from airport);`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/8cfdd9a071a311c732bb591dcf0060ece680391a/Screenshot%202024-09-24%20140859.png)

8.
`select name from country where iso_country in (select iso_country from airport where elevation_ft in (select max(elevation_ft) from airport));`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/8cfdd9a071a311c732bb591dcf0060ece680391a/Screenshot%202024-09-24%20141021.png)

9.
`select count(*) from game, goal_reached where id = game_id and screen_name = "Vesa" group by screen_name;`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/8cfdd9a071a311c732bb591dcf0060ece680391a/Screenshot%202024-09-24%20141125.png)

10.
`select name from airport where latitude_deg in( select min(latitude_deg) from airport);`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/8cfdd9a071a311c732bb591dcf0060ece680391a/Screenshot%202024-09-24%20141300.png)


# Päivityskysely harjoitukset:

1.
`update game set location = (select ident from airport where name = "Nottingham Airport"), co2_consumed = co2_consumed + 500 where screen_name = "Vesa"; select * from game;`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/10858de206c013eaf9fb463a07d8b907123eaa29/Screenshot%202024-09-24%20150326.png)


