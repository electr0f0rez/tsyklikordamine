# tsyklikordamine
```
// 1. külalised sünnipäeval

/* dowhile
küsi kasutajalt tema eesnime, tsükkel peab toimima niikaua kuni kasutaja on sisestanud midagi, et sisestus tühi "" ei oleks.
*/

Console.WriteLine("Tere kasutaja palun sisesta oma eesnimi");
string nimi = "";
do
{
    Console.WriteLine("Sinu nimi on:");
    nimi = Console.ReadLine();
} while (nimi == "");


/* while
siis küsi kasutajalt tema sünnikuupäeva kolme while tsükliga, kõigepealt päev, arvuna, siis kuu, nimena, ning siis aasta, arvuna
päeva küsimise juures tuleb jälgida et kuupäev oleks vahemikus 1-31,
kuu küsimise juures peab uuesti küsima, kui nimetus ei esine programmis (kas switch-case, if-elseif, või .Contains() abiga)
aasta juures ei tohi olla sünniaasta 19ndas sajandis (18xx) ega tulevikus. (tekib ka vahemik)
*/

Console.WriteLine("Sisesta oma sünnikuupäev päev?");
int sünnikuupäev = 0;
while (sünnikuupäev > 31 || sünnikuupäev < 1) ;
{
    Console.WriteLine("PAlun sisesta õige kuupaäev vahemikus 1-31");
    sünnikuupäev = int.Parse(Console.ReadLine());
}

Console.WriteLine("Sisesta ka oma sünnikuu:");
string sünnikuu = "";
while (sünnikuu == "") ;
{
    Console.WriteLine("Sisesta õige kuu:");
    sünnikuu = Console.ReadLine();
    switch (sünnikuu)
    {
        case "detsember":
            Console.WriteLine("Oled sisestanud 12.nda kuu - detsembri");
            break;
        default:
            Console.WriteLine("Ei tunne sellist sünnikuud");
            sünnikuu = "";
            break;
    }
}
