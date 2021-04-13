# Tietokannat

4. SELECT * 
FROM Kurssisuoritus

5. SELECT kurssi 
FROM Kurssisuoritus

6. SELECT DISTINCT kurssi 
FROM Kurssisuoritus

7. SELECT * 
FROM Opiskelija 
WHERE nimi = 'Anna'

8. SELECT * 
FROM Kurssisuoritus 
WHERE Kurssisuoritus.opiskelija = 'Pihla'

9. SELECT * 
FROM Opiskelija 
WHERE pääaine NOT LIKE 'tiede'

10. SELECT Kurssi.nimi, Kurssisuoritus.päivämäärä, Kurssisuoritus.arvosana 
FROM Kurssisuoritus, Kurssi 
WHERE Kurssi.kurssitunnus=Kurssisuoritus.kurssi

11. SELECT Opiskelija.nimi, Kurssisuoritus.päivämäärä, Kurssisuoritus.arvosana 
FROM Kurssisuoritus, Kurssi, Opiskelija 
WHERE Kurssi.kurssitunnus=Kurssisuoritus.kurssi

12. SELECT Kurssi.nimi AS kurssi, Kurssitehtävä.tehtävä AS tehtävä 
FROM Kurssi, Kurssitehtävä 
WHERE Kurssi.kurssitunnus = Kurssitehtävä.Kurssi

13. SELECT Kurssi.nimi AS kurssi, Tehtävä.nimi AS tehtävä
FROM Kurssi, Tehtävä, Kurssitehtävä, Opiskelija, Tehtäväsuoritus
WHERE Opiskelija.nimi = 'Anna'
AND Kurssi.kurssitunnus = Kurssitehtävä.kurssi
AND Tehtävä.tunnus = Kurssitehtävä.tehtävä
AND Opiskelija.opiskelijanumero = Tehtäväsuoritus.opiskelija
AND Kurssitehtävä.tunnus = Tehtäväsuoritus.tehtävä
