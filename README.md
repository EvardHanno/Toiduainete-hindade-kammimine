# Toiduainete hindade kammimine e-poodidest

Veebikammimise programm, mis käib läbi e-poed, ja kammib kokku toitude hinnad. Programmi saab sisestada otsingusõna, mille järgi otsitakse kõik tooted nendes e-poodides ja pannakse tabelisse. Otsingu teostamiseks sisestatakse otsingusõna e-poe oma otsingusse ning saadud tulemused kammitakse.

Programm kasutab RSelenium paketti (selenium-server-standalone-3.5.3), ChromeDriverit (chromedriver-win64) ja Chrome brauserit.

Tulemuseks saab tabeli järgnevate veergudega: 
* Pood
* Tootenimi
* Hind,€
* Hind,€/kg
* Kliendikaardiga,€

NB! Hind,€/kg antud väärtust ei pruugi olla €/kg vaid ka näiteks €/L või €/tk, olenevalt tootest.

Poed, kust kammitakse: 
* Prisma e-pood
* Rimi e-pood
* Selveri e-pood
* Barbora (Maxima e-pood)
* Bolt Market Soola (Tartu)
* Wolt Market Karlova (Tartu)

Edasiste arenduste suunad:
1. Põhjalikum testimine erinevate toodetega/otingusõnadega 
2. Hetkel eeldab kohati program, et ostetakse Tartus
3. Hetkel programmist puudu olevad poed: Wolt ja Bolt vahendavad ka Coopi, Selveri, Prisma, Rimi
4. Hetkel töötab program väga aeglaselt, kui otsingusõna annab väga palju vasteid (näiteks \"juust\") \--\> Programmi optimeerimine kiiremaks kammimiseks (k.a. eri poodide kammimiste paraleliseerimine)

5. Mõelda välja, kuidas tulemusi paremini otsida või esitada! Hetkel
annavad poodide otsingud liiga palju tulemusi:
   - Mõned otsingusõnad annavad väga palju tulemusi, mis pole tegelt õiged (n. "juust" annab tulemusi ka juustehoolduvahenditele)
   - Isegi kui tulemusi on mõistlikus koguses (n. 50) on nimede järgi väga raske leida just neid tooteid, mille kohta on infot vaja (näiteks otsid "aptamil", et leida 0-6 kuu lastele sobivat piimapulbrit, siis tuleb suur valik erinevaid Aptamili piimapulbreid, mis on erinevas vansutes lastele)
   - Kui täpsustada otsingut (n. "aptamil 800 g"), et otsida vaid 800 grammiseid Aptamili tooteid, siis tulevad kõik tooted, milles on mõni koostisosa 800 grammises koguses.


