# Tietokannat

Yhteen tauluun kohdistuvat kyselyt
select* from goal;

![Screenshot](Screenshot%202024-09-18%20114117.png)

select name, type from airport where iso_country = "FI";

select name from airport where iso_country = "FI" order by name asc;

select name, type from airport where iso_country = "FI" order by type, name;

select name from country where name like "F%";

select name from country where name like "%F%";

select location from game where screen_name = "Vesa";

select co2_consumed from game where screen_name = "Ilkka";

select distinct co2_budget from game;
