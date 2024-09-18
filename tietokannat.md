# Tietokannat

Yhteen tauluun kohdistuvat kyselyt:
`select * from goal;`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/3c816e06e35bde5dddca210c2d98b49c047fa34d/Screenshot%202024-09-18%20114117.png)

`select name, type from airport where iso_country = 'FI';`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/0e0f2c48fb1a7819e591af2ee25b761a0bd336cd/Screenshot%202024-09-18%20120901.png)

`select name from airport where iso_country = 'FI' order by name asc;`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/0e0f2c48fb1a7819e591af2ee25b761a0bd336cd/Screenshot%202024-09-18%20121527.png)

`select name, type from airport where iso_country = 'FI' order by type, name;`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/0e0f2c48fb1a7819e591af2ee25b761a0bd336cd/Screenshot%202024-09-18%20121902.png)

`select name from country where name like 'F%';`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/0e0f2c48fb1a7819e591af2ee25b761a0bd336cd/Screenshot%202024-09-18%20122852.png)

`select name from country where name like '%F%';`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/0e0f2c48fb1a7819e591af2ee25b761a0bd336cd/Screenshot%202024-09-18%20124559.png)

`select location from game where screen_name = 'Vesa';`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/0e0f2c48fb1a7819e591af2ee25b761a0bd336cd/Screenshot%202024-09-18%20124754.png)

`select co2_consumed from game where screen_name = 'Ilkka';`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/0e0f2c48fb1a7819e591af2ee25b761a0bd336cd/Screenshot%202024-09-18%20125031.png)

`select distinct co2_budget from game;`

![Screenshot](https://raw.githubusercontent.com/SolMaakinen/tietokannat/0e0f2c48fb1a7819e591af2ee25b761a0bd336cd/Screenshot%202024-09-18%20125234.png)

Where-osan liitosehto:

select country.name as "country name",airport.name as "airport name" from airport, country where airport.iso_country = country.iso_country and country.name = "Iceland";

select airport.name as "airport name" from airport,country where airport.iso_country = country.iso_country and country.name = "France" and airport.type = "large_airport";

select country.name as country_name,airport.name as airport_name from airport, country where airport.iso_country = country.iso_country and country.continent = "AN";

select elevation_ft from airport, game where location = ident and screen_name = "Heini";

select elevation_ft*0.3048 as elevation_m from airport, game where location = ident and screen_name = "Heini";

select name from airport, game where location = ident and screen_name = "Ilkka";

select country.name from airport, game, country where location = ident and airport.iso_country = country.iso_country and screen_name = "Ilkka";

select name from goal, goal_reached, game where game.id = game_id and goal.id = goal_id and screen_name = "Heini";

select airport.name from airport, game, goal, goal_reached where ident = location and game.id = game_id and goal.id = goal_id and screen_name = "Ilkka" and goal.name = "CLOUDS";

select country.name from country, airport, game, goal, goal_reached where airport.iso_country = country.iso_country and ident = location and game.id = game_id and goal.id = goal_id and screen_name = "Ilkka" and goal.name = "CLOUDS";
