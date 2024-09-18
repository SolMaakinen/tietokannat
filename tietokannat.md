# Tietokannat

Yhteen tauluun kohdistuvat kyselyt
select* from goal;

!(Screenshot 202024-09-18 20114117.png)

select name, type from airport where iso_country = "FI";

![Screenshot](Screenshot%2024-09-18%120901.png)

select name from airport where iso_country = "FI" order by name asc;'

![Screenshot](Screenshot%2024-09-18%121527.png)

select name, type from airport where iso_country = "FI" order by type, name;

![Screenshot](Screenshot%2024-09-18%121902.png)

select name from country where name like "F%";

![Screenshot](Screenshot%2024-09-18%122852.png)

select name from country where name like "%F%";

![Screenshot](Screenshot%2024-09-18%124559.png)

select location from game where screen_name = "Vesa";

![Screenshot](Screenshot%2024-09-18%124754.png)

select co2_consumed from game where screen_name = "Ilkka";

![Screenshot](Screenshot%2024-09-18%125031.png)

select distinct co2_budget from game;

![Screenshot](Screenshot%2024-09-18%125234.png)
