[!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/rahiminia)


# WORLD CUP API - 2022 DATA SET
## Live Scores(Real-time player stats)

![](https://english.cdn.zeenews.com/sites/default/files/2020/07/15/872723-fifa-world-cup-2022.jpg )
![](https://komarev.com/ghpvc/?username=raminmr&style=flat-square)


# free-api-worldcup2022
## World Cup 2022

Grab your football API data for FIFA World Cup 2022 competition!
# Register
To use the services, you must register (free registration)
You need a token to call services
>**Http Metod : POST** http://api.cup2022.ir/api/v1/user
### Request
```sh
curl --location --request POST 'http://api.cup2022.ir/api/v1/user' \
--header 'Content-Type: application/json' \
--data-raw '{
"name" : "Reza RAhiminia",
"email": "r.rahiminia@gmail.com",
"password": "******",
"passwordConfirm" : "******"
}'
```

### Response

```sh
{
	"status": "success",
	"message": "User created",
		"data": {
		"token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI2MjliMjJlYTZiOGYwZTVlNGNkZDcxZDMiLCJpYXQiOjE2NTQzMzQxODYsImV4cCI6MTY1NDQyMDU4Nn0.zgWUXkDCcche_5G9UnPB4VeXP68IKIRZm1UfjM457tU"
		}
}
```


# Login
Be sure to log in to use the services
You need a token to call services

>**Http Metod : POST** http://api.cup2022.ir/api/v1/user/login


### Request
```sh
curl --location --request POST 'http://api.cup2022.ir/api/v1/user/login' \
--header 'Content-Type: application/json' \
--data-raw '{
"email": "r.rahiminia@gmail.com",
"password": "12345678"
}'
```

### Response

```sh
{
"status": "success",
	"data": {
	"token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJfaWQiOiI2MjliMjJlYTZiOGYwZTVlNGNkZDcxZDMiLCJpYXQiOjE2NTQzMzQzMTgsImV4cCI6MTY1NDQyMDcxOH0.fP6smP8HB_QHQhAPktB08FEMor_BqOQhzlgXNkN756U"
	}
}
```
# Teams

A request on Team endpoint returns all information about the All Team

>**Http Metod : GET** http://api.cup2022.ir/api/v1/team
>
A request on Team endpoint returns all information about the by Team

>**Http Metod : GET** http://api.cup2022.ir/api/v1/team/{id}

### Request
```sh
curl --location --request GET 'http://api.cup2022.ir/api/v1/team' \
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
>**Http Metod : GET** http://api.cup2022.ir/api/v1/match

A request on Team endpoint returns all information match's very day  [day match's]
>**Http Metod : GET** http://api.cup2022.ir/api/v1/bymatch/{id}

A request on Team endpoint returns all information about the Match [match]
>**Http Metod : GET** http://api.cup2022.ir/api/v1/match/{id}

A request on Team endpoint returns all information about the Match [date match]
>**Http Metod : POST** http://api.cup2022.ir/api/v1/bydate
```sh
{"date":"12/2/2022"}
```

### Request
```sh
curl --location --request GET 'http://api.cup2022.ir/api/v1/match' \
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
		"time_elapsed": "finished",      notstarted | h1 | hf | h2 | finished
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
>**Http Metod : GET** http://api.cup2022.ir/api/v1/standings

A request on Team endpoint returns all information Standings by group  [day match's]
>**Http Metod : GET** http://api.cup2022.ir/api/v1/standings/{group name : A,B,...}


### Request
```sh
curl --location --request GET 'http://api.cup2022.ir/api/v1/standings' \
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
						"d": "0",
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
						"d": "0",
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
						"d": "0",
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
						"d": "0",
						"name_fa": "هلند",
						"name_en": "Nederland",
						"flag": "https://upload.wikimedia.org/wikipedia/commons/thumb/2/20/Flag_of_the_Netherlands.svg/125px-Flag_of_the_Netherlands.svg.png"
						}]

		}]

}
```

### standings info

```sh

 "mp" =>  matches played
 "w"    =>  matches won
 "l"      =>  matches lost
 "pts"  =>  point / score
 "gf"   =>   goals for
 "ga"  =>   goals against
 "gd"  =>   goals difference
 "d"  =>     drawn

```


###The number of users using this service until 28 Oct 2022


|        country       | account |
|:--------------------:|:-------:|
| united States        | 4289    |
| china                | 3394    |
| brazil               | 1318    |
| vietnam              | 738     |
| germany              | 548     |
| poland               | 450     |
| israel               | 352     |
| switzerland          | 290     |
| argentina            | 259     |
| chile                | 231     |
| netherlans           | 190     |
| taiwan               | 189     |
| nepal                | 171     |
| canada               | 161     |
| united kingdom       | 155     |
| france               | 143     |
| iran                 | 116     |
| india                | 93      |
| colombia             | 91      |
| morocco              | 86      |
| finland              | 86      |
| denmark              | 81      |
| mexico               | 75      |
| australia            | 68      |
| japan                | 63      |
| bangladesh           | 62      |
| paraguay             | 58      |
| uruguay              | 49      |
| united arab          | 49      |
| sweden               | 49      |
| indonesia            | 48      |
| korea                | 43      |
| belgium              | 40      |
| guatemala            | 36      |
| ecuador              | 34      |
| russian   federation | 30      |
| thailand             | 29      |
| malaysia             | 29      |
| romania              | 26      |
| venezuela            | 25      |
| ireland              | 21      |
| bolivia              | 19      |
| peru                 | 18      |
| egypt                | 17      |
| egypt                | 17      |
| egypt                | 17      |
| turkey               | 16      |
| saudi arabia         | 12      |
| kenya                | 10      |
| south africa         | 9       |
| pakistan             | 9       |
| jordan               | 9       |
| austria              | 9       |
| czechia              | 8       |
| costa rica           | 8       |
| panama               | 6       |
| ukraine              | 4       |
| myanmar              | 4       |
| uzbekistan           | 3       |
| iceland              | 3       |
| tunisia              | 2       |
| oman                 | 2       |
| lithuania            | 2       |
| kazakhstan           | 2       |
| italy                | 2       |
| new zeland           | 1       |
| moldova              | 1       |
| lebanon              | 1       |
| kyrgzstan            | 1       |
| iraq                 | 1       |
| greece               | 1       |
| ghana                | 1       |
| bulgaria             | 1       |
| armenia              | 1       |
| albania              | 1       |



### ChangeLog
## 2022-09-1 : Add 3 Teams => Costa Rica , Wales , Australia
## 2022-10-31 : Add api Matches by date date
