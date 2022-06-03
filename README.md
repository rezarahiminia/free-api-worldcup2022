![](https://english.cdn.zeenews.com/sites/default/files/2020/07/15/872723-fifa-world-cup-2022.jpg )
# free-api-worldcup2022
## World Cup 2022

Grab your football API data for FIFA World Cup 2022 competition!

# Teams

A request on Team endpoint returns all information about the All Team

>**Http Metod : GET** http://cup2022.ir:9080/api/v1/team
>
A request on Team endpoint returns all information about the by Team

>**Http Metod : GET** http://cup2022.ir:9080/api/v1/team/{id}

### Request
```sh
curl --location --request GET 'http://http://cup2022.ir:9080/api/v1/team' \
--header 'Authorization: Bearer <token>' \
--header 'Content-Type: application/json' \
```

### Responce

```sh
{
	"status": "success",
	"data": [
		{
			"_id": "62965f29800713e332e613f8",
			"name_en": "Iran",
			"name_fa": "ایران",
			"flag": "https://en.wikipedia.org/wiki/File:Flag_of_Iran.svg",
			"fifa_code": "IRN",
			"iso2": "IR",
			"groups": "B",
			"id": "6"

		}]
}
```



# Matchs

A request on Matches endpoint returns all Matches information
>**Http Metod : GET** http://cup2022.ir:9080/api/v1/match

A request on Team endpoint returns all information match's very day  [day match's]
>**Http Metod : GET** http://cup2022.ir:9080/api/v1/bymatch/{id}

A request on Team endpoint returns all information about the Match [match]
>**Http Metod : GET** http://cup2022.ir:9080/api/v1/match/{id}


### Request
```sh
curl --location --request GET 'http://cup2022.ir:9080/api/v1/match' \
--header 'Authorization: Bearer <token>' \
--header 'Content-Type: application/json' \
```

### Responce

```sh
{

	"status": "success",
	"data": [
		{
		"id": 1,
		"type": "group",
		"group": "A",
		"home_team_id": "3",
		"away_team_id": "4",
		"home_score": 0,
		"away_score": 0,
		"home_scorers": null,
		"away_scorers": null,
		"persian_date": "1400-08-30 13:30",
		"local_date": "2022-11-21 1:00 PM",
		"stadium_id": "1",
		"time_elapsed": "Final",
		"finished": "true",
		"matchday": 1,
		"home_team_fa": "سنگال",
		"away_team_fa": "هلند",
		"home_team_en": "Senegal",
		"away_team_en": "Nederland",
		"home_flag": "https://upload.wikimedia.org/wikipedia/commons/thumb/f/fd/Flag_of_Senegal.svg/125px-Flag_of_Senegal.svg.png",
		"away_flag": "https://upload.wikimedia.org/wikipedia/commons/thumb/2/20/Flag_of_the_Netherlands.svg/125px-Flag_of_the_Netherlands.svg.png"
		}]
}
```


# Standings

A request on Matches endpoint returns all Standings information
>**Http Metod : GET** http://cup2022.ir:9080/api/v1/standings

A request on Team endpoint returns all information Standings by group  [day match's]
>**Http Metod : GET** http://cup2022.ir:9080/api/v1/standings/{group name : A,B,...}


### Request
```sh
curl --location --request GET 'http://cup2022.ir:9080/api/v1/standings' \
--header 'Authorization: Bearer <token>' \
--header 'Content-Type: application/json' \
```

### Responce

```sh
{
"status": "success",
"data": [
		{
		"group": "A",
		"teams": [
						{
						"team_id": "1",
						"mp": "0",
						"w": "0",
						"l": "0",
						"pts": "0",
						"gf": "0",
						"ga": "0",
						"gd": "0",
						"name_fa": "قطر",
						"name_en": "Qatar",
						"flag": "https://upload.wikimedia.org/wikipedia/commons/thumb/6/65/Flag_of_Qatar.svg/125px-Flag_of_Qatar.svg.png"
						},
						{
						"team_id": "2",
						"mp": "0",
						"w": "0",
						"l": "0",
						"pts": "0",
						"gf": "0",
						"ga": "0",
						"gd": "0",
						"name_fa": "اکوادور",
						"name_en": "Ecuador",
						"flag": "https://upload.wikimedia.org/wikipedia/commons/thumb/e/e8/Flag_of_Ecuador.svg/125px-Flag_of_Ecuador.svg.png"
						},
						{
						"team_id": "3",
						"mp": "0",
						"w": "0",
						"l": "0",
						"pts": "0",
						"gf": "0",
						"ga": "0",
						"gd": "0",
						"name_fa": "سنگال",
						"name_en": "Senegal",
						"flag": "https://upload.wikimedia.org/wikipedia/commons/thumb/f/fd/Flag_of_Senegal.svg/125px-Flag_of_Senegal.svg.png"
						},
						{
						"team_id": "4",
						"mp": "0",
						"w": "0",
						"l": "0",
						"pts": "0",
						"gf": "0",
						"ga": "0",
						"gd": "0",
						"name_fa": "هلند",
						"name_en": "Nederland",
						"flag": "https://upload.wikimedia.org/wikipedia/commons/thumb/2/20/Flag_of_the_Netherlands.svg/125px-Flag_of_the_Netherlands.svg.png"
						}]

		}]

}
```
