# Loggbok | Testar API
Albert Sparrman

## 2023-04-21

Idag skrev jag planeringen för arbetet och började jobba utifrån en tutorial på freeCodeCamp. Jag hann sätta upp ett projekt med express och ska fortsätta följa guiden under rubriken "REST API Best Practices" nästa gång. 

Länk till tutorial: https://www.freecodecamp.org/news/rest-api-design-best-practices-build-a-rest-api/

## 2023-04-25

Fortsatte jobba med tutorial och den skickar ut json nu. Ska forsätta efter installera body-parser nästa gång.   

## 2023-04-28

Gjorde klart tutorial och ska nästa gång försöka få upp APIn och använda innehållet på en annan sida. När jag är klar med det kommer jag börja jobba med att ändra innehållet i APIn så att det faktiskt är informationen jag ska använda.


## 2023-05-09

Har jobbat med hosting på Glitch. Sidan finns inte uppe en och det verkar beror på något typ av syntax fel. Från vad jag har läst så kan det vara någon ny funktion i javascript som Glitch inte har support för. Koden som jag använder verkar använda något som kallas optional chaining. 

Länk till glitch support: https://support.glitch.com/t/how-to-use-optional-chanining-in-node-v14/25874

## 2023-05-12

Hosting fungerar nu tog hjälp av artikeln på https://support.glitch.com/t/how-to-use-optional-chanining-in-node-v14/25874. Man behövde tydligen manuellt installera en nyare node-version med hjälp av nvm. Nedan är koden som fick det att fungera.

### Installera nvm and senaste node-versionen

```
curl https://pastebin.com/raw/UCvD6VUH | bash
source ~/.bashrc
nvm install node
```

### Lägg till engines i package.json
```
"engines": {
    "node": "12.x"
},
```
Jag la även till --harmony i start scriptet men vet ej om det är användbart eller exakt vad det gör. 



## Orginal json

```
{
    "status": "OK",
    "data": [
        {
            "id": "61dbae02-c147-4e28-863c-db7bd402b2d6",
            "name": "Tommy V",
            "mode": "For Time",
            "equipment": [
                "barbell",
                "rope"
            ],
            "exercises": [
                "21 thrusters",
                "12 rope climbs, 15 ft",
                "15 thrusters",
                "9 rope climbs, 15 ft",
                "9 thrusters",
                "6 rope climbs, 15 ft"
            ],
            "createdAt": "4/20/2022, 2:21:56 PM",
            "updatedAt": "4/20/2022, 2:21:56 PM",
            "trainerTips": [
                "Split the 21 thrusters as needed",
                "Try to do the 9 and 6 thrusters unbroken",
                "RX Weights: 115lb/75lb"
            ]
        },
        {
            "id": "4a3d9aaa-608c-49a7-a004-66305ad4ab50",
            "name": "Dead Push-Ups",
            "mode": "AMRAP 10",
            "equipment": [
                "barbell"
            ],
            "exercises": [
                "15 deadlifts",
                "15 hand-release push-ups"
            ],
            "createdAt": "1/25/2022, 1:15:44 PM",
            "updatedAt": "3/10/2022, 8:21:56 AM",
            "trainerTips": [
                "Deadlifts are meant to be light and fast",
                "Try to aim for unbroken sets",
                "RX Weights: 135lb/95lb"
            ]
        },
        {
            "id": "d8be2362-7b68-4ea4-a1f6-03f8bc4eede7",
            "name": "Heavy DT",
            "mode": "5 Rounds For Time",
            "equipment": [
                "barbell",
                "rope"
            ],
            "exercises": [
                "12 deadlifts",
                "9 hang power cleans",
                "6 push jerks"
            ],
            "createdAt": "11/20/2021, 5:39:07 PM",
            "updatedAt": "11/20/2021, 5:39:07 PM",
            "trainerTips": [
                "Aim for unbroken push jerks",
                "The first three rounds might feel terrible, but stick to it",
                "RX Weights: 205lb/145lb"
            ]
        },
        {
            "name": "Jumping (Not) Made Easy",
            "mode": "AMRAP 12",
            "equipment": [
                "jump rope"
            ],
            "exercises": [
                "10 burpees",
                "25 double-unders"
            ],
            "trainerTips": [
                "Scale to do 50 single-unders, if double-unders are too difficult"
            ],
            "id": "8f8318f8-b869-4e9d-bb78-88010193563a",
            "createdAt": "4/25/2022, 2:45:28 PM",
            "updatedAt": "4/25/2022, 2:45:28 PM"
        },
        {
            "name": "Burpee Meters",
            "mode": "3 Rounds For Time",
            "equipment": [
                "Row Erg"
            ],
            "exercises": [
                "Row 500 meters",
                "21 burpees",
                "Run 400 meters",
                "Rest 3 minutes"
            ],
            "trainerTips": [
                "Go hard",
                "Note your time after the first run",
                "Try to hold your pace"
            ],
            "id": "0a5948af-5185-4266-8c4b-818889657e9d",
            "createdAt": "4/25/2022, 2:48:53 PM",
            "updatedAt": "4/25/2022, 2:48:53 PM"
        },
        {
            "name": "Dumbbell Rower",
            "mode": "AMRAP 15",
            "equipment": [
                "Dumbbell"
            ],
            "exercises": [
                "15 dumbbell rows, left arm",
                "15 dumbbell rows, right arm",
                "50-ft handstand walk"
            ],
            "trainerTips": [
                "RX weights for women: 35-lb",
                "RX weights for men: 50-lb"
            ],
            "id": "3dc53bc8-27b8-4773-b85d-89f0a354d437",
            "createdAt": "4/25/2022, 2:56:03 PM",
            "updatedAt": "4/25/2022, 2:56:03 PM"
        }
    ]
}
```