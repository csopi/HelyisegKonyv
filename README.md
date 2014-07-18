# Helyiségkönyv alkalmazás
Helyiség könyvet a költségvetés kiírók, az építőiparban költségvetéssel dolgozók szoktak készíteni. A célja az, hogy az egyes meglévő vagy tervezett alaprajzi helyiségek szükséges munkáit, azok mennyiségeit könnyen kezelni, naprakészen tartani tudják, egyszerűsítve ezzel munkájukat. Ezekből, azaz az egyes helyiségek mennyiségeiből pedig egyszerűen kimutatásokat, összesítéseket tudnak készíteni. Ebből készül majd a költségvetés, de az egy következő fázis.

Jó lenne egy alkalmazás, ami kezeli a helyiségeket, a tervezett munkákat, és ezen munkák mennyiségeit + összesítést készít.

## Az alkalmazás:
### 1. anyag:
1. Alapoktól kezdem a felépítés kialakítását, az atomi alkotó résztől, tehát az anyagtól. Hogy érthetőbb legyen mit értek anyagon:
például ilyen 1 db kisméretű tégla, 1 m3 víz, 1 db 120 * 60 cm-es ablak, 1 fm szegélyléc. Az egyszerűség kedvéért a keverékeket is anyagnak veszem, így a beton is ide kerülhet.
2. Tehát szükségünk lesz az anyagok tárolására, névvel, mennyiségi egységgel.
3. Itt, az anyagok alatt természetesen megvan az a lehetőség, hogy új anyagot lehessen felvinni.

### 2. szerkezet:
1. Egy nagyon lényeges alkotó eleme az alkalmazásnak a szerkezet. Minden egyes szerkezet **anyagokból** áll. Például: 1 m2 10 cm vastag válaszfal az alábbi alkotó elemekből -anyagokból- áll:

* 2 réteg xy cég diszperziós festéke
* 1 réteg xy cég glettjével glettelés
* 13 kg xy cég gépi vakolata
* 8 db xy cég 10 N + F téglája
* 8,48 kg xy cég falazóhabarcsa
* 13 kg xy cég gépi vakolata
* 1 réteg xy cég glettjével glettelés
* 2 réteg xy cég diszperziós festéke
	(egyenlőre a munkával nem foglalkozom)
	
2. Kell egy olyan menüpont, ahol előre elkészített szerkezetek lesznek, amiből a felhasználó válogathat, mire lesz szüksége a projekthez. Amire szüksége lesz, azt bejelölheti.
3. Itt, a szerkezetek alatt természetesen megvan az a lehetőség, hogy új szerkezeteket lehessen az anyagokból összeállítani (a + jelre kattintva).

### 3. helyiségek:
##### Alapadatok rögzítése:
..1. a helyiség neve
..2. alapterülete - ez alap esetben kalkulált adat a szélesség * hosszúság adatokból, felülírható
..3. szélessége
..4. hosszúsága
..5. belmagassága

##### Szerkezetek megadás a helyiségekhez:
A falak betűrendben vannak megjelölve. A tervet ahogyan szemből nézzük, az az értelmezési szabály, hogy az **a** jelű falszakasz a felső, a **b** jelű a jobb oldali, a **c** jelű az alsó és a **d** jelű a bal oldali falszakasz. (Lásd a mellékelt alaprajzon) Tehát az óramutató haladási irányában vesszük sorra a falakat. A csatolt rajz szerint a nappali 11 m-es homlokzati fala az **a** jelű, a **b** jelű a WC és fürdőszoba irányába eső fal, a **c** jelű a két szoba és az előszoba felé eső fal, és végül a **d** jelű a 4 m-es, balra eső homlokzati határoló fal. 
A megadható adatok:
..1. a falszerkezet típusa
..2. ha nem homlokzati határoló fal, akkor melyik helyiség helyezkedik el a túloldalon. Ezt belső falak esetén kell megadni, hogy a fal ne legyen kétszer számolva
..3. a fal hossza: ez egyenlő az alapadatoknál megadottal, de felülírható, ekkor az alapadat is felülíródik
..4. a fal magassága: ez egyenlő az alapadatoknál megadottal, de felülírható, ekkor az alapadat is felülíródik
..5. mivel belső méretekkel számolunk, ezért a fal bal és jobb oldalán elhelyezkedő csatlakozó falszerkezeteket kell ezek után megadni. Erre azért van szükség, hogy a fal által letakart, vagy sarokban elhelyezkedő szerkezetekkel is számolni lehessen.
..6. a fal alatt lévő szerkezetet kell megadni, pl. alapozás, vagy koszorú
..7. a fal felett lévő szerkezetet kell megadni, pl. koszorú
..8. a fal felett lévő szerkezetet kell megadni, pl. koszorú
..9. az aljzat típusa a következő pont
..10. a födém típusa következik
..11. majd a homlokzati nyílászárók megadása következik, annak a falnak a megadásával ahol elhelyezkednek. Erre azért van szükség, hogy automatikusan kivonódjon a felületük a falból.
..12. a belső nyílászárókat kell ezek után megadni, azzal kiegészítve, hogy melyik falban helyezkednek el + melyik helyiséggel birtokolják közösen ezt a nyílászárót
..13. ezek után még extra szerkezeteket is megadhatunk, ilyenek bármikor előfordulhatnak, ezért van ez a lehetőség

Ez a pont ebben a kialakításban eléggé bonyolult, gondolkozom az egyszerűsítésen. Várom a javaslatokat. 


##### A helyiségekhez már megadott szerkezetek megtekintése: a helyiség nevét viselő gombra kattintva megtekinthető

##### További helyiség a + gombra kattintva vihető fel.


## Készítik:
Balogh István és még remélem sokan mások!