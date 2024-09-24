![image](https://github.com/user-attachments/assets/434a938e-2c77-4e73-b1a9-bc7a3a06c0bd)# Tietokannat

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



3.
`select screen_name, airport.name from game inner join airport on location = ident;`

4.
`select screen_name, country.name from game inner join airport on location = ident inner join country on airport.iso_country = country.iso_country;`

5.
`select airport.name, screen_name from airport left join game on ident = location where name like "%Hels%";`'

6.
`select name, screen_name from goal left join goal_reached on goal.id = goal_id  left join game on game.id = game_id;`
