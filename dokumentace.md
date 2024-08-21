Dokumentace API
Kolekce 1: Ukol- Veronika Obrtelová
1. Add - Záporná čísla
Metoda: GET
URL: https://czechitas-api.vercel.app/api/math/add?a=-3&b=-4
Popis: Tento request odesílá dva záporné parametry a očekává správný součet čísel. Test je úspěšný, pokud se vrátí správný výsledek.
Očekávaný výstup: Součet -3 a -4
2. Add - Mix čísel
Metoda: GET
URL: https://czechitas-api.vercel.app/api/math/add?a=3&b=-4
Popis: Tento request odesílá jeden kladný a jeden záporný parametr a očekává správný součet čísel. Test je úspěšný, pokud se vrátí správný výsledek.
Očekávaný výstup: Součet 3 a -4
3. Add - Neplatné vstupní hodnoty
Metoda: GET
URL: https://czechitas-api.vercel.app/api/math/add?a=-3&b=msdksfgmkdf
Popis: Testuje, zda aplikace správně zachytí a vyřeší neplatné vstupní hodnoty. Očekávaný výstup je chyba (bad request), protože hodnota není číslo.
Očekávaný výstup: Bad request
4. Add - Sčítání výsledků několikrát po sobě
Metoda: GET
URL: https://czechitas-api.vercel.app/api/math/add?a=3&b=3
Popis: Testuje, zda aplikace zvládne opakované sčítání stejného výsledku. Test je úspěšný, pokud se výsledek vrátí správně i při opakovaných požadavcích.
Očekávaný výstup: Součet 3 a 3
5. Add - Nulové hodnoty
Metoda: GET
URL: https://czechitas-api.vercel.app/api/math/add?a=0&b=0
Popis: Tento request odesílá nulové hodnoty a očekává se, že se vrátí nula. Test je úspěšný.
Očekávaný výstup: Součet 0 a 0
6. Add - Kladná čísla
Metoda: GET
URL: https://czechitas-api.vercel.app/api/math/add?a=3&b=4
Popis: Tento request odesílá dva kladné parametry a očekává správný součet čísel. Test je úspěšný, pokud se vrátí správný výsledek.
Očekávaný výstup: Součet 3 a 4
7. Add - Desetinné místo
Metoda: GET
URL: https://czechitas-api.vercel.app/api/math/add?a=abc&b=3
Popis: Tento request odesílá hodnotu, která není číslo, a očekává správný součet čísel. Test je úspěšný, pokud se vrátí správné chybové hlášení. Pokud zadáme hodnoty s desetinnými místy (např. 3.15 a 4.85), test nebude úspěšný.
Očekávaný výstup: Bad request, pokud hodnota není číslo
8. Add - Iracionální čísla
Metoda: GET
URL: https://czechitas-api.vercel.app/api/math/add?a=√2&b=π
Popis: Tento request odesílá iracionální čísla. Očekává se, že výstup bude chybný, protože hodnoty nejsou správně zpracovatelné.
Očekávaný výstup: Bad request
9. Add - Chybějící parametr
Metoda: GET
URL: https://czechitas-api.vercel.app/api/math/add?a=3&b
Popis: Tento request odesílá pouze jeden parametr. Očekává se, že výstup bude chybový, protože chybí druhý parametr.
Očekávaný výstup: Bad request, protože chybí parametr
10. další
Metoda: GET
URL: https://czechitas-api.vercel.app/api/math/add?a="abc"&b=3
Popis: Tento request odesílá hodnotu, která není číselná. Očekává se chybové hlášení.
Očekávaný výstup: Bad request
11. +
Metoda: GET
URL: https://czechitas-api.vercel.app/api/math/add?a=+&b=4
Popis: Tento request odesílá hodnotu s plusem a kladné číslo. Očekává se, že výsledek bude správný součet.
Očekávaný výstup: Součet, v tomto případě 4
12. -
Metoda: GET
URL: https://czechitas-api.vercel.app/api/math/add?a=-&b=4
Popis: Tento request odesílá hodnotu s mínusem a kladné číslo. Očekává se, že výstup bude chybný, protože mínus není platné číslo.
Očekávaný výstup: Bad request
13. New Request
Metoda: GET
URL: https://czechitas-api.vercel.app/api/math/add?a=\"abc\"&b=3
Popis: Tento request odesílá hodnotu s únikovým znakem. Očekává se, že výstup bude chybový.
Očekávaný výstup: Bad request
Kolekce 2: API lekce 12
1. Hlasky all
Metoda: GET
URL: https://czechitas-api.vercel.app/api/czechitas/hlasky/all
Popis: Tento request vrací všechny hlášky. Očekávaný výstup je seznam všech hlášek.
Očekávaný výstup: Seznam hlášek
2. Hlasky random
Metoda: GET
URL: https://czechitas-api.vercel.app/api/czechitas/hlasky/random
Popis: Tento request vrací náhodnou hlášku. Očekávaný výstup je jedna náhodná hláška.
Očekávaný výstup: Náhodná hláška
3. Hlasky id
Metoda: GET
URL: https://czechitas-api.vercel.app/api/czechitas/hlasky/:id
Popis: Tento request vrací hlášku podle zadaného ID. Je třeba nahradit :id skutečným ID hlášky.
Očekávaný výstup: Hláška s daným ID
4. Hlaska dva
Metoda: GET
URL: https://czechitas-api.vercel.app/api/czechitas/hlasky/dva
Popis: Tento request vrací druhou hlášku. Očekávaný výstup je druhá hláška.
Očekávaný výstup: Druhá hláška
5. Hlasky create
Metoda: POST
URL: https://czechitas-api.vercel.app/api/czechitas/hlasky/create
Popis: Tento request vytváří novou hlášku. Je třeba poskytnout potřebná data v těle požadavku.
Očekávaný výstup: Potvrzení vytvoření nové hlášky
6. New Request
Metoda: GET
URL: https://czechitas-api.vercel.app/api/czechitas/hlasky/:id
Popis: Tento request není specifikován. Je třeba doplnit podrobnosti podle potřeby.
Očekávaný výstup: Záleží na specifikaci
