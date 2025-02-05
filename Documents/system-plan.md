# Rendszerterv

## A rendszer célja
A rendszer célja, hogy a cég sok felhasználói fiókkal rendelkező alkalmazottai könnyen, gyorsan, de biztonságosan kezelhessék bizalmas belépési adataikat. Ennek érdekében egy felhasználóhoz kötött asztali alkalmazást készítünk, melyben titkosítva eltárolhatóak ezek a bizalmas adatok, valamint egyszerűen elő is hívhatóak, mégpedig úgy, hogy a képernyőn nem jelennek meg kényes adatok egyszerű szövegként, csupán vágólapra kerülnek. Ezek után a felhasználó felelőssége a vágólap kiűrítése, hogy ne lehessen máshova is kimásolni a jelszavát.  
Továbbá a program képes lesz meghatározott paraméterek mentén biztonságos jelszót generálni az időszakos kötelező jelszócserék megkönnyítése érdekében. A generált jelszavak eltárolása a programban a felhasználó felelősségi körébe tartozik.

## Projekt terv
A projekt létrehozásához 3 szoftverfejlesztő áll rendelkezésre, illetve 8 munkahét. A 3 fejlesztő közös felelőssége a határidőre való átadás és a hibamentes működés.

## Üzleti folyamatok modellje


## Követelmények
|ID|Modul|Kifejtés|
|--|-----|--------|
|K01|Átlátható|Könnyen kezelhető rendszer
|K02|Felhasználóbarát megjelenés|Grafikus felület nyomógombokkal. Átlátható, egyértelmű menüpontok
|K03|Időhatékonyság|Parancsok gyors végrehajtása
|K04|Rendelkezésre állás|Fontos jelszavak kerülnek tárolásra, melyek lehetséges, hogy kizárólag ebben a programban lesznek elmentve. Nem megengedhető, hogy egy dolgozó a program elérhetetlensége miatt ne férhessen hozzá egy fiókjához
|K05|Bizalmasság|A munkakörnyezet nem biztosítja, hogy a dolgozók ne láthassanak rá egymás kijelzőjére. A jelszavak ne kerüljenek kiírásra a képernyőn
|K06|Biztonság|A tárolt jelszavakhoz csak az azokhoz jogosult felhasználó férhet hozzá

## Funkcionális terv
![]()

[comment]: <> (TODO UML diagram)

## Fizikai környezet
A fejlesztés Java nyelven valósul meg Windows operációs rendszerre, illetve különböző Linux disztribúciókra.

## Absztrakt domain modell
A Java program az MVC paradigmát követi. 

[comment]: <> (TODO kiegészítés)
    
## Architekturális terv
A program külön telepítendő minden egyes gépre és nincsenek összeköttetésben. Túlterhelés történhet a memória oldaláról. Ha memóriahiány lép fel, azt a szoftver nem tudja kezelni. Ekkor a program leáll. Ezt csak az erőforráshasználat megfelelő beosztásával lehet kiküszöbölni, ami a programnak nem része, így a felhasználó felelőssége. Probléma esetén a gép újraindítása vagy a feleslegesen futó alkalmazások leállítása segíthet. Problémát okozhat még az adatbázis oldal is. Az adatbázis egy előre egyeztetett fix mérettel rendelkezik majd, így ennél nagyobb mennyiségű jelszó eltárolására nincs, majd lehetőség. Ebben az esetben a felhasználónak lehetősége van korábbi, már nem használt jelszavak törlésésre. Vagy igény esetén a cég kérése vállaljuk a korlátok bővítését az igények növekedésének megfelelően verziófrissítésekkel. Minden felhasználó csak az általa regisztrált fiókban tárolt jelszavakat érheti el. A fiókok létrehozása és menedzselése pedig a cég informatikai szakemberének a feladata.

## Adatbázis terv


## Implementációs terv


## Tesztterv
A tesztelés legfőbb célja, hogy kizárjuk annak esélyét, hogy a felhasználó nem a megfelelő jelszót kapja vissza a programtól, ezzel lassítva vagy akadályozva a munkát, esetlegesen kárt okozva a cégnek. Tehát a tesztesetekben legfőképp az adatbázisból való helyes lekérés és dekódolás helyessége kerül vizsgálatra.

## Telepítési terv
Az elkészült alkalmazás egy *.jar* állományból lesz futtatható, ehhez a cég közlése alapján rendelkezésre áll minden számítógépen a *Java Development Kit* legfrissebb verziója, így az egyedüli feladat a *.jar* állomány elhelyezése rajtuk.

## Karbantartási terv
Az esetleges hibajavítások, vagy későbbi igények szerinti funkcionális újítások szintén *.jar* állomány útján jutnak el az alkalmazottak számítógépeire.
