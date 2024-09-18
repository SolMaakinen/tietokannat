# Tietokannat

Yhteen tauluun kohdistuvat kyselyt  
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
