# API-Projekt

# Hur Applikationen fungerar:
 
Jag har utvecklat en applikation som hämtar data från en databas via en API. Databasen som används tillhandahålls av OMDBs API. Genom att anropa API:et får jag tillgång till olika filmer och deras detaljerade information. För att presentera denna information på webbsidan använder jag HTML, CSS och JavaScript.

JavaScript-koden spelar en viktig roll i applikationen. När användaren interagerar med sidan och söker efter en specifik film, aktiveras JavaScript-funktioner som hämtar och visar filmer med matchande titlar. Användaren får sedan en lista med de olika filmerna att välja mellan.

När användaren har valt en film och klickar på den, omdirigeras de till en sida där mer omfattande information om filmen visas. Denna sida är utformad för att ge en djupare förståelse för filmens handling, skådespelare, betyg och andra relevanta detaljer.

Genom att kombinera teknikerna för att hämta data från OMDBs API, presentera informationen med HTML och CSS, samt använda JavaScript för att hantera användarinteraktionen, skapas en användarvänlig och informativ applikation för att utforska och upptäcka filmer.


# De viktigaste delarna av javascipten:

Hantering av sökning och laddning av filmer:

Funktionen loadMovies(searchTerm) ansvarar för att hämta filmer från OMDB API genom att bygga en URL med söktermen och API-nyckeln. Den använder fetch för att göra en asynkron HTTP-begäran och får tillbaka data i JSON-format. Om svaret är "True" anropas funktionen displayMovieList för att visa listan med filmer.
Visning av listan med filmer:

1. Funktionen displayMovieList(movies) tar emot en lista med filmer och genererar HTML-kod för varje film. Det skapar en ny <div> för varje film och fyller den med filminformation, inklusive bild, titel och år. Därefter läggs varje film till i searchList-elementet på sidan.
Laddning av filmdetaljer:

Funktionen loadMovieDetails() tilldelar en händelselyssnare till varje film i searchList. När en film klickas på göms söklistan, värdet i sökrutan rensas och en ny asynkron begäran görs för att hämta detaljerad information om den valda filmen från OMDB API. Den detaljerade informationen skickas sedan till funktionen displayMovieDetails för att visas på sidan.
Visning av filmdetaljer:

Funktionen displayMovieDetails(details) använder informationen om den valda filmen för att generera HTML-kod för att visa dess detaljer. Det skapar en <div> för filmens affisch och en annan <div> för att visa information som titel, år, betyg, releasedatum, genre, skådespelare, handling, språk och utmärkelser.
Hantering av användarinteraktion och döljning av sökresultat:

En händelselyssnare på window-objektet övervakar klickhändelser och om klicket inte sker på sökfältet, döljs söklistan.
