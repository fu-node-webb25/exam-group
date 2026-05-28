# ☕ Bygg ett API för Airbean!

Airbean är den futuristiska kaffebaren där kaffe levereras med drönare (nåja… nästan!). I detta **grupparbete** ska ni bygga ett backend-API som gör det möjligt att lägga beställningar – men bara själva API:t. **Ingen frontend** ska byggas.

En inspelad presentation av uppgiften [hittar ni här]() (ej publicerad ännu!)

---

## 🧩 Uppgiften

Ni ska tillsammans bygga ett REST API för Airbean, där användare ska kunna:

- Se kaffemenyn  
- Lägga till/ta bort varor i en kundvagn
- Lägga en order
- Se tidigare ordrar kopplade till ett unikt användar-ID  
- Skapa konton och logga in  

Ni får en färdig meny att utgå från, och det är endast produkterna i den som ska kunna beställas. Menyn lägger ni till manuellt via MongoDBCompass.  
**Länk till menyn:**  
👉 [Airbean Products](airbean.products.json)

---

## ✅ Krav (för Godkänt)

- API:et ska vara byggt i **Node.js med Express**
- Databasen ska vara **MongoDB**  
- All input som kommer in via URL eller request body ska **valideras i middleware**:
  - Felaktig data ska returnera ett tydligt **felmeddelande**
- Endast produkter från menyn får läggas till i en beställning
- När ett **användarkonto** skapas ska det få ett **slumpat användar-ID**  
- Orderhistorik ska kunna hämtas med användar-ID (**inte** användarnamn)
- Koden ska vara **välstrukturerad och läsbar**
- Era endpoints och er logik MÅSTE följa dokumentationen som [ni hittar här](https://gist.github.com/Santosnr6/a47f8ae17ac4d01f89c579e7ddb488f7). Det är enligt denna logik jag kommer testa ert API när jag rättar så se till att följa den.
- Alla anrop förutom `/api/keys` skall vara låsta bakom en API-nyckel.
- Ni skall skapa Swaggerdokumentation för **hela** ert API.
- Att du som gruppmedlem deltagit aktivt under arbetet. AI-genererad kod är förbjuden i denna uppgift, och jag kommer kontrollera så att alla bidragit genom att granska era commits.

**Viktigt!**
Ni får INTE använda er av kryptering för att säkra lösenord, eller tokens för användarautentisering i denna examination. Istället vill jag att ni sätter ```global.user = user``` när ni har en inloggad användare.

---

## 👥 Grupparbete

### 📄 Gruppkontrakt

Varje grupp skriver ett **gruppkontrakt** där ni själva bestämmer vilka punkter som gäller. Använd gärna [detta dokument](https://docs.google.com/document/d/1HZc1a_mxGOrEE77rFTZ3LydQ_zZfBlfm/edit?usp=sharing&ouid=117251319654116712560&rtpof=true&sd=true) som mall.  
Detta används om konflikter skulle uppstå. Om ett kontrakt inte finns, riskerar hela gruppen att bli underkänd vid problem. I denna uppgift vill jag att ni inte sitter tillsammans, utan snarare delar ut uppgifter som löses indivduellt. Vissa delar får ni göra tillsammans om ni så önskar.

### 📁 Repo & arbetsyta

- En gruppmedlem skapar ett **GitHub-repo** och bjuder in övriga
- Sätt upp en **projekttavla** i GitHub Projects eller Trello  
- Till er hjälp har ni följande [user stories](https://github.com/users/Santosnr6/projects/27)

---

## 🧪 Tips

- Testa era endpoints i **Postman** eller **Insomnia**
- Ge era users en **role**-property (det kommer underlätta inför den individuella examinationen)
- Dela upp arbetet: t.ex. konton, beställningar, validering
- Lägg all valideringslogik i **middleware**
- Ha en tydlig projektstruktur: mappar, routes, felhantering
- Blir era *routes* för stora så kan ni skapa en controllersmapp som fungerar som en "mellanhand" mellan era routes och resten av applikationen, och där ni kan lägga logiken.

---

## 📥 Inlämning

Alla i gruppen lämnar in en **länk till ert gemensamma GitHub-repo** på Azomo  
**Deadline: Torsdag 4/6 kl 23:59**

⚠️ Glöm inte:
- Att bjuda in mig till ert repo
- Att dela er projekttavla med mig
- Att skapa en User till mig, samt ge mig Network Access till er databas. Min IP-adress: **2.248.92.11**
- Lägga in era kompletta connection strings både för Compass och Drivers i kommentarerna för er inlämning. **Glöm inte** att fylla i mina inloggningsuppgifter i er connection string.
- Använd följande "nycklar" i er .env-fil så att jag slipper leta i er kod: ```PORT``` & ```CONNECTION_STRING```

---
