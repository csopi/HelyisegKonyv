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

### 3. projektek:
1. Mik ezek a projektek? Nézzünk egy-két példát:
	* egyszerű esettel kezdem, családi ház: első lépésként létrehozzuk a projektet, megadjuk a projekt nevének például azt, hogy **"Családi ház, 8200 Veszprém, Egyik u. 1."**. Ez a családi ház 2 szintes, tehát a szinteket adjuk meg ezek után, például úgy mint földszint és tetőtér. Ezek után már nincsen más dolgom mint az egyes szintek alá "befűzzük" a helyiségeket, amit a 3. pontban részleteztem. Készen is van a projekt, igazából ez egy hierarchikus fa szerkezet. A gyökér a projekt, azaz a családi ház, ebből elágazik két ág, ezek a szintek, majd ezeken az ágakon mint a levelek helyezkednek el a helyiségek.
	* másik példaként irodaházat mutatok be: ez esetben is a projektnek adok egy nevet, **"Iroda épület, 8200 Veszprém, Másik u. 123."**. Ezek után megadom a szinteket, a pinceszinttől a 4. emeletig, összesen 6 szintet. Ezek után a szintekhez adom az ott elhelyezkedő helyiségeket.
	* harmadik példaként egy nagyon bonyolult épületet vázolok fel, ábra nélkül: képzeljünk el egy olyan épületet, például szállodát ahol még szintenként is funkciók szerint tovább bontjuk a funkciók szerint az épületet. Ekkor a hierarchikus fa szerkezet is sokkal több szintes lesz, jóval bonyolultabb lesz, de a levelek ebben az esetben is a helyiségek.
2. A projekt létrehozása után a nevére kattintva jutunk a projekt összefoglaló oldalra. Itt lehet kialakítani a hierarchia szinteket, amit az első pontban részleteztem.
3. Itt az összefoglaló oldalon látható az egész alkalmazás célja: **a szerkezetek és az anyagok végső összesítése**. Az adatok gombnyomásra exportálhatóak.
4. A helyiségeket összefoglaló, a helyiségek előtt található hierarchia szinteket megjelenítő gombokra kattintva lehet az egyes helyiségek tulajdonságait és szerkezeteit megadni. Ezek az alábbiak:
	* alapterülete - ez alap esetben kalkulált adat a szélesség * hosszúság adatokból, felülírható
	* szélessége
	* hosszúsága
	* belmagassága
A helyiségekhez szerkezetet a helyiség sorában lévő + gombra kattintva lehet megadni. a szerkezet megadás szabályai:
a falak betűrendben vannak megjelölve. A tervet ahogyan szemből nézzük, az az értelmezési szabály, hogy az **a** jelű falszakasz a felső, a **b** jelű a jobb oldali, a **c** jelű az alsó és a **d** jelű a bal oldali falszakasz. (Lásd a mellékelt alaprajzon) Tehát az óramutató haladási irányában vesszük sorra a falakat. A csatolt rajz szerint a nappali 11 m-es homlokzati fala az **a** jelű, a **b** jelű a WC és fürdőszoba irányába eső fal, a **c** jelű a két szoba és az előszoba felé eső fal, és végül a **d** jelű a 4 m-es, balra eső homlokzati határoló fal. 
A megadható adatok:
	* a falszerkezet típusa
	* ha nem homlokzati határoló fal, akkor melyik helyiség helyezkedik el a túloldalon. Ezt belső falak esetén kell megadni, hogy a fal ne legyen kétszer számolva
	* a fal hossza: ez egyenlő az alapadatoknál megadottal, de felülírható, ekkor az alapadat is felülíródik
	* a fal magassága: ez egyenlő az alapadatoknál megadottal, de felülírható, ekkor az alapadat is felülíródik
	* mivel belső méretekkel számolunk, ezért a fal bal és jobb oldalán elhelyezkedő csatlakozó falszerkezeteket kell ezek után megadni. Erre azért van szükség, hogy a fal által letakart, vagy sarokban elhelyezkedő szerkezetekkel is számolni lehessen.
	* a fal alatt lévő szerkezetet kell megadni, pl. alapozás, vagy koszorú
	* a fal felett lévő szerkezetet kell megadni, pl. koszorú
	* a fal felett lévő szerkezetet kell megadni, pl. koszorú
	* az aljzat típusa a következő pont
	* a födém típusa következik
	*	 majd a homlokzati nyílászárók megadása következik, annak a falnak a megadásával ahol elhelyezkednek. Erre azért van szükség, hogy automatikusan kivonódjon a felületük a falból.
	* a belső nyílászárókat kell ezek után megadni, azzal kiegészítve, hogy melyik falban helyezkednek el + melyik helyiséggel birtokolják közösen ezt a nyílászárót
	* ezek után még extra szerkezeteket is megadhatunk, ilyenek bármikor előfordulhatnak, ezért van ez a lehetőség

	Ez a pont ebben a kialakításban eléggé bonyolult, gondolkozom az egyszerűsítésen. Várom a javaslatokat. 

A helyiségekhez már megadott szerkezetek megtekintése: a helyiség nevét viselő gombra kattintva megtekinthető.
További helyiség a + gombra kattintva vihető fel.
Az oldalon alul helyezkedik el a szintek szerkezetinek és anyagainak összesítője.

Visszalépni a projekthez az oldal tetején a kék színű projekt névre kattintva lehet. 

### 4. egyeb megjegyzések:
Az alkalmazás mobil eszközön is használható kialakításban készült.


## Készítik:
Balogh István és még remélem sokan mások!