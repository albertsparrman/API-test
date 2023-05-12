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